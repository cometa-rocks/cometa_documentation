### Prepare MFA in Amvara GitLab account
Amvara GitLab link -> https://git.amvara.de/ 
<br>
<br>
**Step 1:** Login to your Gitlab account 

**Step 2:** Click "Profile Icon" > "Preferences" <br>
<br><img src="img/mfa_screens/preferences.jpg" width="200px"/> <br>

**Step 3:** Click "Account" <br>
<br><img src="img/mfa_screens/AccountButton.jpg" width="200px"/><br>

**Step 4:** Click "Enable Two Factor Authentication" <br>
<br><img src="img/mfa_screens/EnableMFA.jpg" width="700px"/><br>

**Step 5:** Enter "YOUR_CURRENT_PASSWORD" and "VERIFICATION_CODE", then click "Register with two-factor app"<br>
Get your varification code/OTP by following <a href=""> this step </a>
 
Get your first verification code to setup MFA <br>
    Note: Do not use this step if you are going to use secret key for automation using Cometa.      

**Setup your Authenticator apps**

* Scan the displayed QR code in any authenticator app, such as [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2), [Microsoft Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator) etc<br>
* You will see your GitLab account listed in the authenticator app.<br>
* Now, in the authenticator app, navigate to your account and retrieve the OTP. <br>

<img src="img/mfa_screens/CodeSetup.jpg" width="800px"/>

**Step 6:** Click 'Download Codes' and store them in a secure location. This will complete your MFA setup successfully<br>
<br><img src="img/mfa_screens/CodesScreen.jpg" width="700px"/><br>
