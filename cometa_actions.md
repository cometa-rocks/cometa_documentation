<img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png" width="600px"/>


# Co.meta steps table of contents

Co.meta offers versatile and easy to use steps like "Goto URL {URL}" or "Move mouse to {selector} and click". Below is a list of grouped actions by topic.

1. [Browser actions](#browser-actions)
2. [CSS selectors actions](#CSS_AC)
3. [Feature actions](#FEATURE_AC)
4. [Mouse actions](#MOUSE_AC)
5. [Keyboard actions](#KEYBOARD_AC)
6. [IBM actions](#IBM_AC)
7. [IBM Cognos QueryStudio actions](#QUERYSTUDIO_AC)
8. [Editing Excel Files](#EDITEXCEL_AC)
9. [Uploading and Downloading files](#FILES)
10. [Other actions](#OTHER_AC)
11. [Support](#SUPPORT)

<br/>

# <span>Co.</span>meta steps / actions

Actions or steps are the build blocks from where your tell Co.meta what you want to automate. You have actions for clicking, browsing, screen sizing, downloading, can send keys and so on and so on.

We have grouped the different actions and the first one is "Browser actions".

The first steps in your testplan will probably be *Goto "{URL}"* - make sure to leave the quotes and replace anything else. Do not worry about escapeing your quotes. Co.meta does that for you.

A very versatile step is *Run Javascript function "{function}"* - function can be anything you can execute as Javscript inside a browser. It can be just one command or a complete snipplet. This brings you low-code.

If you have suggestions or needs for a step / actions that you would rather implement in python, then please download the Co.meta repo and have a look actions.py for the code of any step that was implemented here.

### Browser actions<a id="browser-actions"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>StartBrowser and call URL "{url}"</td>
        <td>Browse to an URL</td>
        <td></td>
    </tr>
    <tr>
        <td>Goto URL "{url}"</td>
        <td>Browse to an URL</td>
        <td></td>
    </tr>
    <tr>
        <td>Maximize the browser</td>
        <td>Maximizes the browser window</td>
        <td></td>
    </tr>
    <tr>
        <td>I resize the browser to "{x}" x "{y}"</td>
        <td>Resizes the browser window to X and Y, useful for virtual mobile testing</td>
        <td></td>
    </tr>
    <tr>
        <td>I can resize the browser to "{x}" x "{y}"</td>
        <td>Checks if it can resize the browser window to X and Y, useful for virtual mobile testing</td>
        <td></td>
    </tr>
    <tr>
        <td>I can close the window </td>
        <td>Closes the current window</td>
        <td></td>
    </tr>
    <tr>
        <td>Close the browser</td>
        <td>Closes the browser and reverts to latest opened tab/window if available</td>
        <td></td>
    </tr>
    <tr>
        <td>I can close the window</td>
        <td>Closes the current window</td>
        <td></td>
    </tr>
    <tr>
        <td>I can switch to new Window </td>
        <td>Switches to another existing (or just created) Window/Tab (e.g. popup window)</td>
        <td></td>
    </tr>
    <tr>
        <td>I can switch to main Window</td>
        <td>Switches to the main Window/Tab</td>
        <td></td>
    </tr>
    <tr>
        <td>I switch to default content </td>
        <td>Changes the testing context to the main document in the current Tab/Window, similar to using window.top <br/>
        I can switch back to default content, e.g. if I switched to iFrame before</td>
        <td></td>
    </tr>
    <tr>
        <td>BrowserTitle is "{browserTitle}"</td>
        <td>Checks if the current Tab Title is/contains some sentence</td>
        <td></td>
    </tr>
    <tr>
        <td>Reload page </td>
        <td>Reloads the current page<br/>
        Useful to reset to default settings (e.g. if elements are marked in a different color)</td>
        <td></td>
    </tr>
    <tr>
        <td>Fetch Console.log from Browser and attach it to the feature result.</td>
        <td>Fetches browser console logs and attaches them to the feature results.<br>
         (Note : This step does not work with the Firefox browser. If used, it will result in an error.)
        </td>
        <td></td>
    </tr>
</table>
