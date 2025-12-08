# Cometa Frontend - FOSS Disclosure

This document identifies all Free and Open-Source Software (FOSS) components used in the **Cometa Scheduler Docker Image**, including the base OS image, system utilities, Python interpreter, and Python libraries installed via `requirements.txt`.

## **GROUP 1 — Angular Framework (Google LLC)**

### Libraries included:
`@angular/animations @angular/cdk @angular/compiler @angular/forms @angular/material @angular/platform-browser @angular/platform-browser-dynamic @angular/router @angular/service-worker @angular/common @angular/core @angular/language-service @angular-devkit/build-angular @angular/cli @angular/compiler-cli`

### ✔ All from Google  
### ✔ All licensed under **MIT License**

---

### **ENTRY — Angular Framework (Group)**

| Field | Value |
| --- | --- |
| **FOSS Component Name** | Angular Framework (multiple packages listed below) |
| **Component Versions** | 15.2.x (per package) |
| **Included Packages** | See list above |
| **License** | MIT License |
| **Copyright** | © 2010–2023 Google LLC |
| **License Text** | Included in Annex |
| **Source Code Location** | https://github.com/angular/angular |
| **Source of Supply** | https://www.npmjs.com/ |
| **Reference Date** | (Your retrieval date) |

---

## **GROUP 2 — NGXS State Management (NGXS Organization)**

### Libraries included:
`@ngxs/store @ngxs/storage-plugin @ngxs/form-plugin @ngxs/devtools-plugin @ngxs-labs/select-snapshot @ngxs-labs/immer-adapter`

### ✔ License: **MIT License**

---

### **ENTRY — NGXS Framework (Group)**

| Field | Value |
| --- | --- |
| **FOSS Component Name** | NGXS State Management Framework |
| **Component Versions** | 3.7.x – 3.8.x / @ngxs-labs 3.x–4.x |
| **License** | MIT License |
| **Copyright** | © NGXS Authors |
| **License Text** | Included in Annex |
| **Source Code Location** | https://github.com/ngxs/store |
| **Supply** | npm registry |
| **Reference Date** | (Your retrieval date) |

---

## **GROUP 3 — ngx-translate (Translation Framework)**

### Libraries included:
`@ngx-translate/core @ngx-translate/http-loader`

### ✔ License: **MIT License**

---

### **ENTRY — ngx-translate Framework (Group)**

| Field | Value |
| --- | --- |
| **FOSS Component Name** | ngx-translate (Core + HTTP Loader) |
| **Versions** | core: ^14.0.0, loader: ^6.0.0 |
| **License** | MIT License |
| **Source Code** | https://github.com/ngx-translate |
| **Supply** | npm registry |
| **Reference Date** | (Your retrieval date) |

---

## **GROUP 4 — @ng-matero (Material Extensions)**

### Libraries included:
`@ng-matero/extensions`

### ✔ License: **MIT License**

---

### **ENTRY — ng-matero Extensions**

| Field | Value |
| --- | --- |
| **Component Name** | @ng-matero/extensions |
| **Version** | 15.5.0 |
| **License** | MIT License |
| **Source Code** | https://github.com/ng-matero/extensions |
| **Supply** | npm |
| **Reference Date** | – |

---

## **GROUP 5 — @ngneat Projects**

### Libraries included:
`@ngneat/until-destroy`

### ✔ License: **MIT License**

---

### **ENTRY — @ngneat/until-destroy**

| Field | Value |
| --- | --- |
| **Component Name** | @ngneat/until-destroy |
| **Version** | 8.0.4 |
| **License** | MIT License |
| **Source Code** | https://github.com/ngneat/until-destroy |
| **Supply** | npm |

---

## **GROUP 6 — Angular UI Extensions (MIT License)**

### Libraries included:
`@ng-select/ng-select @perfectmemory/ngx-contextmenu ngx-clipboard ngx-json-viewer ngx-network-error angular-svg-round-progressbar highcharts-angular`

### ✔ All MIT (highcharts itself not included here)

---

### **ENTRY — Angular UI Extensions (MIT Group)**

| Field | Value |
| --- | --- |
| **FOSS Component Name** | Angular UI Extensions (multiple packages) |
| **License** | MIT License |
| **Source** | GitHub + npm registry |
| **Reference Date** | – |

---

## **GROUP 7 — Highcharts (Non-MIT License)**

### Libraries included:
`highcharts highcharts-angular`

### ✔ highcharts-angular → MIT  
### ❌ highcharts → **Proprietary License**

---

### **ENTRY — Highcharts**

| Field | Value |
| --- | --- |
| **Component Name** | Highcharts |
| **Version** | ^11.0.1 |
| **License** | Highcharts Proprietary License |
| **Copyright** | © Highsoft AS |
| **Source Code** | https://github.com/highcharts/highcharts |
| **Supply** | https://www.highcharts.com |
| **Reference Date** | – |

---

## **GROUP 8 — General Utility Libraries (All MIT)**

### Included:
`lodash.keyby compare-versions memo-decorator nested-property immer cron-parser date-fns d3 ajv-keywords tslib zone.js`

---

### **ENTRY — General Utility Libraries**

| Field | Value |
| --- | --- |
| **Component Name** | JavaScript Utility Libraries (MIT group) |
| **License** | MIT License |
| **Source** | Various GitHub repos |
| **Supply** | npm |

---

## **GROUP 9 — Development Tools (MIT License)**

Included:  
`eslint prettier ts-node typescript karma jasmine-core jasmine-spec-reporter rxjs @types/*`

---

### **ENTRY — Development Tooling**

| Field | Value |
| --- | --- |
| **Component Name** | Frontend Development Tooling |
| **License** | MIT |
| **Scope** | devDependencies |
| **Source** | npm registry |

---

## **GROUP 10 — Snyk CLI (Apache 2.0)**

Included: `snyk`

---

### **ENTRY — Snyk**

| Field | Value |
| --- | --- |
| **Component Name** | Snyk CLI |
| **License** | Apache License 2.0 |
| **Source** | https://github.com/snyk/snyk |
| **Supply** | npm registry |

---

## **GROUP 11 — npm (Artistic License 2.0)**

Included: `npm install`

---

### **ENTRY — npm**

| Field | Value |
| --- | --- |
| **Component Name** | npm |
| **License** | Artistic License 2.0 |
| **Source** | https://github.com/npm/cli |
| **Supply** | npm registry |

---

## **GROUP 12 — Amvara Proprietary Component**

Included: `ngx-amvara-toolbox`

---

### **ENTRY — Amvara Proprietary Component**

| Field | Value |
| --- | --- |
| **Component Name** | ngx-amvara-toolbox |
| **License** | Proprietary (Amvara-owned, non-FOSS) |
| **Supply** | Internal |



# Cometa Frontend – Dockerfile FOSS Disclosure

This lists all Free & Open-Source Software (FOSS) used indirectly through Docker base images and APT-installed packages in the **Cometa Frontend** Docker build.  

---

# GROUP 1 — Node.js (OpenJS Foundation)

## Components:
- `node:18`
- `node:20`

## License:
- **Node.js:** MIT License  
- **Debian base image:** Includes components licensed under MIT, BSD, GPL, Apache 2.0, etc.
---

## ENTRY — Node.js Base Images

| Field | Value |
|------|-------|
| **FOSS Component Name** | Node.js Base Image (node:18, node:20) |
| **Versions** | 18.x, 20.x |
| **License** | MIT License (Node.js); Debian contains multiple FOSS licenses |
| **Copyright** | © Joyent / Node.js contributors |
| **License Text** | Included in Annex |
| **Source Code Location** | https://github.com/nodejs/node |
| **Source of Supply** | https://hub.docker.com/_/node |
| **Reference Date** | (Date of dependency retrieval) |

---

# GROUP 2 — Apache HTTP Server (Apache Software Foundation)

## Components:
- `httpd:2.4.64`

## License:
- **Apache License 2.0**

## Source:
- https://httpd.apache.org  
- https://hub.docker.com/_/httpd

---

## ENTRY — Apache HTTP Server

| Field | Value |
|------|-------|
| **FOSS Component Name** | Apache HTTP Server (httpd:2.4.64) |
| **Version** | 2.4.64 |
| **License** | Apache License 2.0 |
| **Copyright** | © The Apache Software Foundation |
| **License Text** | Included in Annex |
| **Source Code Location** | https://github.com/apache/httpd |
| **Source of Supply** | https://hub.docker.com/_/httpd |
| **Reference Date** | (Date of dependency retrieval) |

---

# GROUP 3 — Debian GNU/Linux System Packages (Various Licenses)

Installed via `apt-get`:

```
git
apache2
libapache2-mod-auth-openidc
libcjose0
libjansson4
libcurl4
zlib1g
libssl1.1
libapache2-mod-security2
curl
vim
iputils-ping
telnet
```

## Licenses Included:
- **MIT License**
- **Apache License 2.0**
- **GPLv2**
- **BSD License**
- **zlib License**
- **OpenSSL Dual License**

## Repository:
- https://deb.debian.org/

---

## ENTRY — Debian System Packages (Group)

| Field | Value |
|------|-------|
| **FOSS Component Name** | Debian GNU/Linux System Packages |
| **Included Packages** | See list above |
| **Licenses** | MIT, Apache 2.0, BSD, GPLv2, zlib, OpenSSL |
| **Copyright** | Various contributors |
| **License Text** | Included in Annex |
| **Source Code Location** | https://salsa.debian.org |
| **Source of Supply** | Debian APT Repository |
| **Reference Date** | (Date of dependency retrieval) |

---

# GROUP 4 — Appium Inspector (Apache License 2.0)

## Components:
- Cloned from: `https://github.com/AMVARA-CONSULTING/appium-inspector`

## License:
- **Apache License 2.0**

---

## ENTRY — Appium Inspector

| Field | Value |
|------|-------|
| **FOSS Component Name** | Appium Inspector |
| **Version** | Latest Git commit at build time |
| **License** | Apache License 2.0 |
| **Copyright** | © Appium Contributors |
| **License Text** | Included in Annex |
| **Source Code Location** | https://github.com/AMVARA-CONSULTING/appium-inspector |
| **Source of Supply** | GitHub |
| **Reference Date** | (Date of dependency retrieval) |

---

# GROUP 5 — Cometa Proprietary Components (Not FOSS)

## Components:
```
start_server.sh
apache2/conf/*.conf
apache2/metadata/*
apache2/modules/
```

## License:
- **Proprietary — Cometa Rocks S.L.**
- Not subject to FOSS disclosure.

---

## ENTRY — Cometa Internal Components

| Field | Value |
|------|-------|
| **Component Name** | Cometa Proprietary Scripts & Configurations |
| **License** | Proprietary (Not Open Source) |
| **Copyright** | © COMETA ROCKS S.L. |
| **Source Code Location** | Internal to product |
| **Source of Supply** | Packaged in Docker build |
| **Reference Date** | – |

---

# END OF DOCUMENT
