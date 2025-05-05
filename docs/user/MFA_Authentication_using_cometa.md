<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# Automation of Muti Factor Authentication with Cometa
Multi factor authentication which are done by One time password, those can be automated using Cometa 

## 1. MFA and OTP

* **MFA (Multi Factor Authentication)**
    Multi-factor authentication (**MFA**, **two-factor authentication**, or **2FA**, along with similar terms) is an electronic authentication method in which a user is granted access to a website or application only after successfully presenting two or more pieces of evidence (or factors) to an authentication mechanism. 
    <br>
    <br>
    **Source [Wikipedia](https://en.wikipedia.org/wiki/Multi-factor_authentication)** 
    <br>
    <br>
* **OTP (One Time Password)**
    A one-time password (OTP), also known as a one-time PIN, one-time authorization code (OTAC) or dynamic password, is a password that is valid for only one login session or transaction, on a computer system or other digital device.
    <br>
    
    OTP generation algorithms make use of pseudorandomness to generate a shared key.
    <br> 
    <br> 
    <b>Source: [Wikipedia](https://en.wikipedia.org/wiki/One-time_password) </b>
    <br>
    <br>

### Steps of MFA Automation and Prerequisite  

The automation of two-factor authentication with Cometa requires two steps.


* **Step 1: (Prerequisite)** Create an account and obtain the MFA secret key. If you already have an account, you can use that. Next, follow the provided links to set up MFA and obtain the secret key from any one of the multi-factor authentication providers. (This requires at least one MFA setup), **(This requires at least one MFA)**.
            
    **1. Gitlab** <a href="./MFA_Authentication_preparation.md"> Set up Multi-Factor Authentication (MFA) in our GitLab.</a>
        
    **2. Google MFA** Create an account at <a href="https://support.google.com/accounts/answer/27441?hl=en">Google</a> then <a href="https://support.kraken.com/hc/en-us/articles/360001486466-How-to-find-the-setup-key-or-backup-code-for-authenticator-app-2FA"> get a <i>secret key</i>. </a>
      Note: You have the option to choose any other MFA provider based on your needs
    <br>
    <br>
    **Get verification code** Once you are asked to scan the OR code, do not do that. Instead,  get the secret key and follow the steps below:
                
    1. Create a small Python script using the code below.
        <pre>  import pyotp
        # i.e 'HHHH LLLL KKKK JJJJ LLLL DDDD DDDD DDDD' or ABCDEFGHIJKLMNOPQRSTUVWTUVWTUVW
        token = "YOUR CODE .... .... .... .... .... ...." 
        token = token.replace(" ","")
        totp = pyotp.TOTP(token)
        otp = totp.now()
        print("OTP : ", otp)</pre>  

    2. Please install pyotp to run this code using the following command. (A machine with Python installed can run this code with the required library [pyotp](https://github.com/pyauth/pyotp)).
        
        <pre>pip install pyotp</pre>

    3. Replace "YOUR CODE ..." with your token/secret key.
    4. Run the code; you will receive the OTP in the output.       
    <br>

    <i> Note: OTP will be valid for 60 seconds</i>
    <br>
    <br>
        For more information, use the pyAuth library to generate OTPs – see: https://github.com/pyauth/pyotp.
    <br>
    <br>

* **Step 2: Create Test**  Store the <i>secret key</i> in Cometa as a <i>secret variable</i>. Once the authentication token is stored, you can proceed to generate OTP using Cometa by following the next step. 

      Create one-time password of "{x}" digits using pairing-key "{value}" and save it to the encrypted variable "{variable_name}
        
    Refer to the <a target="_blank" href="https://github.com/Cometa-rocks/Cometa_documentation/blob/main/Cometa_actions.md#:~:text=online%20excel%20viewer.-,Create%20one%2Dtime%20password%20of%20%22%7Bx%7D%22%20digits%20using,-pairing%2Dkey%20%22%7Bvalue">Create one-time password using Cometa </a>


    #### For illustration, you can automate the login screen of Cometa to test the functionality of the MFA automation feature

    **Steps to be automated**

    #### Manual Steps of Cometa login 
    * Fill Captcha

    * Select Login with Gitlab

    * Enter your "Gitlab_UserID"

    * Enter your "Gitlab_Password"

    * Click Sign In

    * Get OTP(Verification Code)

    * Enter OTP
    
    * Your will be logged into Cometa with MFA.


    #### Automation steps of MFA in Cometa login.

    * Create a feature in Cometa <br>

    * Provide a feature name and description<br>

    * Please follow the steps, as shown in the screenshot below
    <br>
    <br>
    <img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/MFA_login_test.png" width="700px"/>



