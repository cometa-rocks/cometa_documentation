<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# Enable MFA in Amvara GitLab account

Two-factor authentication (2FA) is a crucial feature to bolster the security of your Amvara GitLab account. By implementing 2FA, an additional layer of protection is added, ensuring that unauthorized access is significantly more challenging. To access your Amvara GitLab account, potential intruders would need not only your username and password but also the second factor of authentication.

[Amvara GitLab](https://git.amvara.de/) supports the One-Time Password (OTP) method as a second factor of authentication:

Click [Amvara GitLab link](https://git.amvara.de/) to create or login to your account.
<br>
<br>

### Steps to setup 2FA 

**Step 1:** Login to your [Amvara GitLab](https://git.amvara.de/) account 

**Step 2:** Click "Profile Icon" > "Preferences" <br>
<br><img src="
https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/preferences.jpg" width="200px"/> <br>

**Step 3:** Click "Account" <br>
<br><img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/AccountButton.jpg" width="200px"/><br>

**Step 4:** Click "Enable Two Factor Authentication" <br>
<br><img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/EnableMFA.jpg" width="700px"/><br>

**Step 5:** Enter "YOUR_CURRENT_PASSWORD" and "VERIFICATION_CODE", then click "Register with two-factor app". Next get your first verification code to setup MFA <br>
    
> Note: Do not use this step if you are going to use secret key for automation using Cometa. Instead, use the <a target="_blank" href="https://github.com/cometa-rocks/cometa_documentation/blob/test/MFA_Authentication_using_cometa.md#:~:text=Get%20verification%20code"> Get verification code </a>. After that complete [Step 6](#STEP-6).
    
#### Setup your authenticator app

* Scan the displayed QR code with any authenticator app, such as [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2), [Microsoft Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator) etc<br>
* You will see your GitLab account listed in the authenticator app.<br>
* Now, in the authenticator app, navigate to your account and retrieve the OTP. <br>

<img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/CodeSetup.jpg" width="800px"/>
<br>
<br>

**Step 6:**<a id="STEP-6"><a> Click 'Download Codes' and store them in a secure location. This will complete your MFA setup successfully<br>
<br><img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/CodesScreen.jpg" width="700px"/><br>
