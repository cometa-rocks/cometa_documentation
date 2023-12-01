<img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png" width="600px"/>

# Setting up Co.meta login with MFA (Muti Factor Authentication) 

## 1. MFA with OTP (One Time Password)

### OTP (One Time Password)
> A one-time password (OTP), also known as a one-time PIN, one-time authorization code (OTAC) or dynamic password, is a password that is valid for only one login session or transaction, on a computer system or other digital device.
><br>
><br>
> OTP generation algorithms make use of pseudorandomness to generate a shared key.
><br> 
><br> 
><b>Source: [Wikipedia](https://en.wikipedia.org/wiki/One-time_password) </b>

### Prepare MFA with GitLab
GitLab Link -> https://git.amvara.de/
><strong>Step 1:</strong> Login to your Gitlab Account 

><strong>Step 2:</strong> Click "Profile Icon" > "Preferences" <br>
><br><img src="img/mfa_screens/preferences.jpg" width="200px"/> <br>

><strong>Step 3:</strong> Click "Account" <br>
><br><img src="img/mfa_screens/AccountButton.jpg" width="200px"/><br>

><strong>Step 4:</strong> Click "Enable Two Factor Authentication" <br>
><br><img src="img/mfa_screens/EnableMFA.jpg" width="700px"/><br>

><strong>Step 5:</strong> Enter "YOUR_CURRENT_PASSWORD" and "VERIFICATION_CODE", then click "Register with two-factor app"  <br>
><br><img src="img/mfa_screens/CodeSetup.jpg" width="800px"/><br>
><br><strong>1<sup>st</sup> Way: To Get Verfication Code</strong>
>> 1. Scan the displayed QR code in any authenticator app, such as [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2), [Microsoft Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator) etc<br>
>> 2. You will see your GitLab account listed in the authenticator app.<br>
>> 3. Now, in the authenticator app, navigate to your account and retrieve the OTP.<br><br><i> Note: OTP will be valid for 60 seconds</i>
> 
><strong>2<sup>nd</sup> Way: To Get Verification Code : Manually</strong><a id="MANUAL_OTP"></a>
>> 1. Use pyAuth library to generate OTPs – see: https://github.com/pyauth/pyotp
>>> Note: 
>>> 1. A machine with Python installed can run this code with the required library [pyotp](https://github.com/pyauth/pyotp)
>>> 2. Please install pyotp to run this code using the following command  
>>>><i>$pip install pyotp</i><br>
>> <pre>import pyotp
>> token = "YOUR CODE .... .... .... .... .... ...." # i.e 'HHHH LLLL KKKK JJJJ LLLL DDDD' or ABCDEFGHIJKLMNOPQRSTUVW
>> token = token.replace(" ","")
>> totp = pyotp.TOTP(token)
>> otp = totp.now()
>> print("OTP : ", otp)</pre>
>> 2. Enter your token, run this code, and you will receive the OTP.

><strong>Step 6:</strong> Click 'Download Codes' and store them in a secure location. This will complete your MFA setup successfully<br>
><br><img src="img/mfa_screens/CodesScreen.jpg" width="700px"/><br>


### Go to your Co.meta login page

><strong>Step 1:</strong> Fill Captcha

><strong>Step 2:</strong> Select Login with Gitlab

><strong>Step 3:</strong> Enter your "Gitlab_UserID"

><strong>Step 4:</strong> Enter your "Gitlab_Password"

><strong>Step 5:</strong> Click Sign In

><strong>Step 6:</strong> Get OTP(Verification Code)  
>
>> 1. Get OTP (Verification Code) from your Authenticator App" <br>
>> Or<br>
>> 2. From your pyotp library (Python script): Perform the same steps as in [5.2 Get Verification Code: Manually](#MANUAL_OTP)

><strong>Step 7:</strong> Enter OTP

><strong>Step 8:</strong> Your will be logged into Co.meta in with MFA.
