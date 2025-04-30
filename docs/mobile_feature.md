<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

# Co.meta mobile feature
1. [Introduction](#introduction)

2. [Start Mobile](#start-mobile)

3. [Landing tree](#landing-tree)

4. [Shared Mobiles](#shared-mobiles)

5. [Live Steps](#live-steps)

6. [Main view](#main-view)

7. [NoVNC & Inspect](#novnc-inspect)

<br/>

### Introduction

Automated tests on mobile devices are crucial for ensuring software quality, efficiency, and consistency. 

They help detect errors quickly, reduce testing time, and are scalable, allowing for testing across multiple device configurations without manual intervention. 

Statistics show that 80% of companies adopting automated testing report increased software quality and shorter delivery times. By implementing a feature that automates these steps with a mobile emulator, you can significantly improve workflow and application reliability.

### Start Mobile

Why is the Start button activated for mobile device containers?

Once manually activated, access to the mobile device is available through the predefined steps provided in the Feature's Step Editor.

These mobile containers can be initialized, paused, and restarted.

Mobile containers can be accessed in two ways:

  * Through the Feature.
  * Through the Landing Tree.

To work with the feature, follow these steps:

Go to the feature of the desired department and click on Modify.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/modify.png" width="400px">

Click on Start Mobile or use the shortcut <strong>shortcut(S)</strong>:

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/information.png" width="900px">

### Landing tree

If working from the Landing Tree is preferred, select the desired department to use the mobile device functionality as follows:

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/tree_mobile_device.png" width="200px" height="300px">

First, select the department and start the desired mobile device.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/Select_department.png" width="400px">

Next, choose the mobile container and start it:

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/start.png" width="400px">
Once started, the emulator can be paused if needed.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/running_to_pause.png" width="400px">
If paused, it can be restarted to resume operation.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/paused_to_restart.png" width="400px">

Note: If the package is not available, upload it through the Upload option in <strong>Edit Feature</strong>, ensuring the package is in APK format.
Additionally, an APK package can be installed on the mobile device.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/upload_apk.png" width="1000px">

Now, go to the Emulator Feature, click on the more_vert (⋮) icon, and select <strong>Modify</strong>. From there, upload the package in APK format to make it available.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/more_vert_emulator.png" width="400px">

Once in the Modify section, four tabs will be displayed: Information, Install APK, Installed APK, and Share Emulator.

Install APK: Allows uploading an APK file for installation.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/dialog_install_apk.png" width="1000px">

Installed APK: Displays a list of already installed APKs.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/dialog_installed_apk.png" width="1000px">

Share Emulator: Provides options to share the emulator instance.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/dialog_share_emulator.png" width="1000px">

Feature Emulator Shared: Shows the emulator in shared mode.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/emulator_shared.png" width="400px">

More information:

To view additional details, click on more options:

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/more_info_mobile_device.png" width="400px">

### Shared Mobiles

To view the mobile devices of other colleagues in the same department, scroll down until reaching "Shared Mobile."

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/shared.png" width="400px">

### Live Steps

Once the steps related to the mobile device are completed, access to the noVNC of the desired mobile will be available.
When reaching the step where the mobile is loaded, the noVNC will become visible, allowing the mobile to be viewed.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/live-steps.png" width="800px">

### Main view

Once all steps are completed, the result will appear as the second icon (a camera).
If there is one mobile, it will display directly; if multiple, a dropdown will allow selection.
Additionally, there is a 'Mobile' column that shows the mobile name.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/result.png" width="1000px">

### NoVNC Inspect

<h4>1. noVNC</h4> 
noVNC enables web-based access to VNC servers via browsers.
<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/novnc.png" width="400px">

<!-- noVNC Functionalities Table -->
<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Remote Device Visualization</td>
      <td>View the device screen in real-time via a web browser, ideal for debugging and monitoring automated tests.</td>
    </tr>
    <tr>
      <td>Remote Device Control</td>
      <td>Interact with the device using the keyboard and mouse to simulate taps, swipes, and other gestures.</td>
    </tr>
    <tr>
      <td>Test Automation Monitoring</td>
      <td>Run Appium automated tests while observing live progress, quickly identifying visual or functional issues.</td>
    </tr>
    <tr>
      <td>Session Recording</td>
      <td>Record interactions during tests or debugging for later review and analysis.</td>
    </tr>
    <tr>
      <td>Screenshot Capturing</td>
      <td>Take screenshots directly from the noVNC interface for comparison or visual testing.</td>
    </tr>
    <tr>
      <td>Multi-User Access</td>
      <td>Allow multiple users to observe or interact with a device simultaneously, ideal for team collaboration.</td>
    </tr>
    <tr>
      <td>Application Debugging</td>
      <td>Test user interactions in real-time across various devices and resolutions to identify design or functionality issues.</td>
    </tr>
    <tr>
      <td>Virtual Device Management</td>
      <td>Monitor and control emulated devices, adjust emulator settings, or restart devices remotely.</td>
    </tr>
    <tr>
      <td>CI/CD Integration</td>
      <td>Observe automated test runs as part of CI/CD pipelines, ensuring devices are active and functional.</td>
    </tr>
  </tbody>
</table>

<h4>2. Inspector</h4> 
Appium Inspector identifies mobile app elements for automated testing.
<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/mobile_feature/inspect.png" width="400px">

<!-- Inspector Functionalities Table -->
<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>UI Element Inspection</td>
      <td>Examine the app structure and element attributes such as ID, XPath, etc.</td>
    </tr>
    <tr>
      <td>Interactive Testing</td>
      <td>Simulate taps, swipes, and text input.</td>
    </tr>
    <tr>
      <td>Test Code Generation</td>
      <td>Generate test code snippets in multiple languages for automated testing.</td>
    </tr>
    <tr>
      <td>Cross-Platform Support</td>
      <td>Inspect both Android and iOS apps with a single tool.</td>
    </tr>
    <tr>
      <td>Appium Server Integration</td>
      <td>Connect to Appium server and execute real-time commands.</td>
    </tr>
    <tr>
      <td>Custom Gestures Validation</td>
      <td>Test custom gestures like zoom or multi-touch.</td>
    </tr>
    <tr>
      <td>Localization Testing</td>
      <td>Verify app behavior in different languages or regions.</td>
    </tr>
    <tr>
      <td>Screenshots and Recording</td>
      <td>Capture screens or record interactions for debugging and analysis.</td>
    </tr>
    <tr>
      <td>Log Monitoring</td>
      <td>View real-time logs for debugging purposes.</td>
    </tr>
    <tr>
      <td>QA Workflow Integration</td>
      <td>Speed up the creation of automation test scripts.</td>
    </tr>
  </tbody>
</table>
