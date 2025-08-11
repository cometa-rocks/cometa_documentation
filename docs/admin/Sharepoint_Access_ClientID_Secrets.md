# Microsoft Graph app (client credentials) with access to a **specific** SharePoint site

This guide shows how to get your **tenant_id**, **client_id**, and **client_secret**, assign **Microsoft Graph** permissions, and (critically) scope those permissions to **one SharePoint site** using **Sites.Selected** — so the app can **read and write** files only in that site (not tenant-wide).

---

## At a glance

- **tenant_id** (Directory ID): your Microsoft Entra ID tenant GUID.
- **client_id** (Application ID): the GUID of your registered app.
- **client_secret**: a secret generated for that app (store securely).
- **Graph permissions**: use **Application** (app-only) permissions for background services.
- **Scope to one Site**: assign **Sites.Selected** permission, then grant the app **Write** access to the specific Site (either by PnP.PowerShell or Microsoft Graph).

> If you **must** cover all SharePoint content (not recommended), use **Files.ReadWrite.All** (Application). But prefer **Sites.Selected** for least privilege.

---

## Prerequisites

- Azure role that can register apps and (ideally) grant admin consent (e.g., **Cloud Application Administrator** + an **Entra ID admin** for consent, or coordination with one).
- SharePoint Admin or site owner rights to grant site-level app permissions (via PnP or Graph).
- Azure CLI / PowerShell optional, but helpful.

---

## 1) Get your `tenant_id` (Directory ID)

**Azure Portal**  
1. Go to **Azure Portal** → **Microsoft Entra ID**.  
2. **Overview** → copy **Tenant ID** (Directory ID).

**CLI alternatives**  
- **Azure CLI**:  
  ```bash
  az account show --query tenantId -o tsv
  ```
- **PowerShell (Az)**:  
  ```powershell
  Get-AzTenant | Select-Object -ExpandProperty Id
  ```

---

## 2) Create the app and get `client_id`

**Azure Portal**  
1. **Microsoft Entra ID** → **App registrations** → **New registration**.  
2. Name it (e.g., `SharePoint Site RW App`).  
3. **Single tenant** is typical for corp setups; leave Redirect URI empty (not needed for client credentials).  
4. After creation, in **Overview** copy **Application (client) ID** → this is your `client_id`.

> For service-to-service (no user), you’ll use the **client credentials** (app-only) flow.

---

## 3) Create a `client_secret`

**Azure Portal**  
1. In your app: **Certificates & secrets** → **Client secrets** → **New client secret**.  
2. Add a description, choose an expiry (6–12 months is common; set a renewal reminder).  
3. **Copy the secret _Value_ immediately** — it’s only shown once.  
4. Store it securely (e.g., **Azure Key Vault**, GitHub/GitLab/Azure DevOps secret store).

---

## 4) Add Microsoft Graph **Application** permissions

**Azure Portal**  
1. App → **API permissions** → **Add a permission** → **Microsoft Graph**.  
2. Choose **Application permissions** (not Delegated).  
3. Add **Sites.Selected** (recommended least-privilege).  
   - If you cannot use Sites.Selected, add **Files.ReadWrite.All** to cover all sites (tenant‑wide).  
4. Click **Grant admin consent** for your tenant (requires admin).

> Adding **Sites.Selected** alone does **not** grant access to any site until you explicitly grant the app permissions to the **specific** site (next step).

---

## 5) Grant the app access to only the target SharePoint site

You have two mainstream options: **PnP.PowerShell** (simplest) or **Microsoft Graph API** (pure API). Either way, you’ll map the app to the site with **Read** or **Write**.

### Option A — PnP.PowerShell (recommended for admins)

1. Install and import PnP.PowerShell on a machine with access:  
   ```powershell
   Install-Module PnP.PowerShell -Scope CurrentUser
   Import-Module PnP.PowerShell
   ```

2. Connect to the **target site** (replace your tenant and site name):  
   ```powershell
   $siteUrl = "https://contoso.sharepoint.com/sites/TargetSite"
   Connect-PnPOnline -Url $siteUrl -Interactive
   ```

3. Grant the app **Write** permission to the site using its `client_id`:  
   ```powershell
   $appId = "<your client_id GUID>"
   Grant-PnPAzureADAppSitePermission -AppId $appId -Site $siteUrl -Permissions Write -DisplayName "SharePoint Site RW App"
   ```

   - Use `-Permissions Read` if you only need read.
   - Verify:  
     ```powershell
     Get-PnPAzureADAppSitePermission -Site $siteUrl
     ```

### Option B — Microsoft Graph API (app-role assignment at site level)

1. Get the **site ID**:  
   ```bash
   # Using client credentials token (see “Test & verify” for token retrieval)
   # Replace {host} and {site-path}, e.g. contoso.sharepoint.com and sites/TargetSite
   curl -s -H "Authorization: Bearer $TOKEN" \
     "https://graph.microsoft.com/v1.0/sites/{host}:/sites/{site-path}?$select=id,displayName"
   ```

2. Grant **write** permission to the app principal on that site:  
   ```bash
   SITE_ID="<the id from step 1>"
   APP_ID="<your client_id GUID>"
   curl -s -X POST -H "Authorization: Bearer $TOKEN" -H "Content-Type: application/json" \
     -d '{
           "roles": ["write"],
           "grantedToIdentities": [{
             "application": {
               "id": "'"$APP_ID"'",
               "displayName": "SharePoint Site RW App"
             }
           }]
         }' \
     "https://graph.microsoft.com/v1.0/sites/$SITE_ID/permissions"
   ```

   - Use `roles: ["read"]` for read-only.
   - List current permissions:  
     ```bash
     curl -s -H "Authorization: Bearer $TOKEN" \
       "https://graph.microsoft.com/v1.0/sites/$SITE_ID/permissions"
     ```

> After this step, your app with **Sites.Selected** will have the exact permissions on **only that site**.

---

## 6) Test & verify (client credentials flow)

Below are minimal examples to **list files** and **upload** to a document library on the permitted site.

### Get a token (client credentials)

**Bash `curl`** (replace placeholders):  
```bash
TENANT_ID="<tenant_id>"
CLIENT_ID="<client_id>"
CLIENT_SECRET="<client_secret>"

curl -s -X POST "https://login.microsoftonline.com/$TENANT_ID/oauth2/v2.0/token" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET&scope=https%3A%2F%2Fgraph.microsoft.com%2F.default&grant_type=client_credentials"
# parse the JSON 'access_token' into $TOKEN for subsequent calls
```

### Find the site drive (Document Library)

Most team sites use the default **Documents** library. Get the **site ID**, then the default **drive ID**:

```bash
HOST="contoso.sharepoint.com"
SITE_PATH="sites/TargetSite"

# site id
SITE_ID=$(curl -s -H "Authorization: Bearer $TOKEN" \
  "https://graph.microsoft.com/v1.0/sites/$HOST:/$SITE_PATH?`echo '$'`select=id" | jq -r .id)

# default drive (Documents)
DRIVE_ID=$(curl -s -H "Authorization: Bearer $TOKEN" \
  "https://graph.microsoft.com/v1.0/sites/$SITE_ID/drive?`echo '$'`select=id" | jq -r .id)
```

### List files in the root folder

```bash
curl -s -H "Authorization: Bearer $TOKEN" \
  "https://graph.microsoft.com/v1.0/drives/$DRIVE_ID/root/children"
```

### Upload a small file (<=4 MB) to root

```bash
curl -s -X PUT -H "Authorization: Bearer $TOKEN" \
  --data-binary @"./local-file.txt" \
  "https://graph.microsoft.com/v1.0/drives/$DRIVE_ID/root:/local-file.txt:/content"
```

### Upload a large file (>4 MB)

For large files, create an **upload session**:  
```bash
UPLOAD_URL=$(curl -s -X POST -H "Authorization: Bearer $TOKEN" -H "Content-Type: application/json" \
  -d '{"item": {"@microsoft.graph.conflictBehavior":"replace","name":"large.zip"}}' \
  "https://graph.microsoft.com/v1.0/drives/$DRIVE_ID/root:/large.zip:/createUploadSession" | jq -r .uploadUrl)

# Then PUT the bytes in 5–60 MB chunks with Content-Range until complete.
```

---

## Optional: quick Azure CLI bootstrap

> The portal flow is simpler for permissions. CLI can create the app and secret quickly, but you’ll still need to add Graph permissions and grant admin consent.

```bash
# Login
az login

# Create the app
az ad app create --display-name "SharePoint Site RW App"

# Get appId (client_id)
CLIENT_ID=$(az ad app list --display-name "SharePoint Site RW App" --query "[0].appId" -o tsv)

# Create client secret (capture secretText)
az ad app credential reset --id "$CLIENT_ID" --append

# tenant_id
TENANT_ID=$(az account show --query tenantId -o tsv)
echo "TENANT_ID=$TENANT_ID"
echo "CLIENT_ID=$CLIENT_ID"
```

> Next: add **Sites.Selected** (Application) permission in the **portal**, click **Grant admin consent**, then grant site-level permissions via **PnP** or **Graph**.

---

## Troubleshooting

- **403 Forbidden** on Graph calls:
  - Ensure token uses **client credentials** (`scope=https://graph.microsoft.com/.default`).
  - Confirm **admin consent** was granted for **Sites.Selected** (or Files.ReadWrite.All).
  - If using **Sites.Selected**, verify you actually **granted site permission** (PnP or Graph) and that role is **write** when uploading.
- **401 Unauthorized**:
  - Expired/invalid token; get a fresh token.
  - Secret expired or not matching the app.
- **Uploaded but cannot see file**:
  - Verify the **drive/library** and **path**. Default “Documents” is common, but custom libraries have different drives.
- **Multi-tenant app**:
  - If set to multi-tenant, ensure admin consent is granted in **each** tenant that should use the app.

---

## What you have now

- `tenant_id`, `client_id`, `client_secret` for your Graph app.  
- App-only Graph permission **Sites.Selected** (or Files.ReadWrite.All).  
- Site-level **Write** (or Read) permission for the **specific** SharePoint site.  
- Working examples to list and upload files via Microsoft Graph.
