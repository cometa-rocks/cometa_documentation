<img src="img/cometa.png" width="600px"/>

# Co.meta steps table of contents

Co.meta offers versatile and easy to use steps like "Goto URL {URL}" or "Move mouse to {selector} and click". Below is a list of grouped actions by topic.

1. [Browser actions](#BROWSER_AC)
1. [CSS selectors actions](#CSS_AC)
1. [Feature actions](#FEATURE_AC)
1. [Mouse actions](#MOUSE_AC)
1. [Keyboard actions](#KEYBOARD_AC)
1. [IBM actions](#IBM_AC)
1. [IBM Cognos QueryStudio actions](#QUERYSTUDIO_AC)
1. [Other actions](#OTHER_AC)
1. [Support](#SUPPORT)

<br/>

# <span class="gold">Co.</span>meta steps / actions

Actions or steps are the build blocks from where your tell Co.meta what you want to automate. You have actions for clicking, browsing, screen sizing, downloading, can send keys and so on and so on.

We have grouped the different actions and the first one is "Browser actions".

The first steps in your testplan will probably be *Goto "{URL}"* - make sure to leave the quotes and replace anything else. Do not worry about escapeing your quotes. Co.meta does that for you.

A very versatile step is *Run Javascript function "{function}"* - function can be anything you can execute as Javscript inside a browser. It can be just one command or a complete snipplet. This brings you low-code.

If you have suggestions or needs for a step / actions that you would rather implement in python, then please download the Co.meta repo and have a look actions.py for the code of any step that was implemented here.

### Browser actions<a name="BROWSER_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>StartBrowser and call URL "(url)"</td>
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
</table>

### CSS selectors actions<a name="CSS_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>I move mouse to "{css_selector}" and
click</td>
        <td>Moves the mouse to the css selector and click</td>
        <td>when I Move mouse to "[id="ibis-contract-search:ibis-contractstates"]" and click</td>
    </tr>
    <tr>
        <td>I move mouse over "{css_selector}"</td>
        <td>Moves the mouse to the center of css selector</td>
        <td>when I move mouse over "[id="ibis-fvn:ibis-contractcontext-selected"]"</td>
    </tr>
    <tr>
        <td>Focus on element with "{css_selector}"</td>
        <td>Focus on element using a CSS selector</td>
        <td>when I Focus on element with "[id="ibis-fvn:ibis-contractsearch"]"</td>
    </tr>
    <tr>
        <td>I can click on element with css selector "{css_selector}"</td>
        <td>Checks if it can click on an element using a CSS Selector</td>
        <td>then I can click on element with css selector "[id="ibis-fvn:ibis-searchcontract"]"</td>
    </tr>
    <tr>
        <td>I can see element with css selector "{css_selector}"</td>
        <td>Checks if it can see an element using a CSS Selector</td>
        <td>then I can see element with css selector "[id="ibis-fvn:ibis-searchcontract"]"</td>
    </tr>
    <tr>
        <td>Check if "{css_selector}" contains "{value}" in "{css_property}"</td>
        <td>Checks if an element contains a given text inside a css-property like background-image, fontSize, etc.</td>
        <td>Check if "[id="navbar"]" contains "#f00" in "background-color"</td>
    </tr>
    <tr>
        <td>Check if "{css_selector}" contains "{value}" in JS property "{js_property}"</td>
        <td>Checks if an element contains a given text inside a js-property like innerText. <br/>Use "caseInsensitive:" to ignore the spelling of the value.</td>
        <td>Check if "[id="ibis-welcometext"]" contains "$SAW_User" in JS property "innerText" <br/>Check if "td.pf > table.tb > tbody > tr > td:nth-child(1) > span:nth-child(1)" contains "caseInsensitive:$SAW_username" in JS property "innerText"</td>
    </tr>
    <tr>
        <td>Scroll to element with css selector "{selector}"</td>
        <td>Scroll to an element using a CSS Selector</td>
        <td></td>
    </tr>
    <tr>
        <td>There is no coincidence with css selector "{selector}"</td>
        <td>Checks if an element doesn't exist using a CSS Selector</td>
        <td></td>
    </tr>
    <tr>
        <td>Save selector "{css_selector}" value to environment variable "{variable_name}"</td>
        <td>save css-selector's property value if available else gets selector's innerText and saves it as an environment variable, environment variable value has a maximum value of 255 characters</td>
        <td>Save selector "#ibis-fhn:ibis-center-id_label" value to environment variable "center"</td>
    </tr>
    <tr>
        <td>Save list values in selector "{css_selector}" and save them to variable "{variable_name}"</td>
        <td>Same as above but for several values which are saved as a list separated by semicolon.<br/>Use "unique:" to remove duplicates from the saved list.<br/> Note: Cannot save content like < span >< /span >(empty)</td>
        <td>Save list values in selector "[id*=ibis-center-id_items] li" and save them to variable "IBIS_CenterList" <br/>Save list values in selector " id="ibis-system-jobs\:ibistab-panel\:table-container\:ibis-system-mec-jobstable_data"] tr:nth-child(n) td:nth-child(2)" and save them to variable "unique:IBIS_MEC"</td>
    </tr>
    <tr>
        <td>Set value "{text}" on "{selector}"</td>
        <td>Set a value on an element, normally used for inputs</td>
        <td></td>
    </tr>
    <tr>
        <td>Scroll to "{amount}"px on element "{selector}"</td>
        <td>Scrolls to a given amount of pixels in the Y axis inside a specific element using a CSS selector</td>
        <td></td>
    </tr>
    <tr>
        <td>I use selector "{number}" and select option "{index}" for Cognos promptpage</td>
        <td>Selects an option defined with index from selector index defined with number.<br/>Index and number start from 0 for first element.</td>
        <td></td>
    </tr>
    <tr>
        <td>I can select option "{option_value}" for "{css_selector}"</td>
        <td>Selects an option value in a select input using a CSS Selector</td>
        <td>I can select option "$centerID" for "[name="p_pt_Center"]" (feature #336)</td>
    </tr>
    <tr>
        <td>I use selector "{css_selector}" and select option "{value}"</td>
        <td>Selects an option value or index for a given select element using a CSS Selector or an index.<br/>{css_selector} variable allows for the following prefixes: index:|value: <br/>{value} variable allows for the following prefixes: index:|value:|contains: <br/>Example: I use selector "index:2" and select option "contains:Financial" <br/>Index starts from 1 for first element.</td>
        <td>I use selector "[name="p_pt_Center"]" ...<br/> I use selector "index:2" and ...<br/>I use selector "[name="p_pt_Center"]" and select option "$centerID"<br/> I use selector "[name="p_pt_Center"]" and select option "index:3"<br/> I use selector "[name="p_pt_Center"]" and select option "contains:Financial"</td>
    </tr>
    <tr>
        <td>Test list of "{css_selector}" elements to contain all or partial values from list variable "{variable_name}" use prefix "{prefix}" and suffix "{suffix}"</td>
        <td>Compares any content of a css selector (e.g. table, dropdown options) to a list saved in variable. <br/>Several variable lists can be combined, separated by "|" (pipe). <br/>Note: Cannot test content like < span >< /span > (empty). Or list like " ;a;b;c; ;e;f"</td>
        <td>1 list:<br/> Test list of "{css selector}" elements to contain all or partial values from list variable "IBIS_MEC" use prefix " " and suffix " "<br/>
        2 lists: <br/>Test list of "table[class="ls"]>tbody>tr:nth-child(n+3)>td [cid="11"]>span" elements to contain all or partial values from list variable "ENL_VINs|RIT_VINs" use prefix " " and suffix " "</td>
    </tr>
</table>

### Feature actions<a name="FEATURE_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Schedule Job "{feature_name}" using parameters "{parameters}" and crontab pattern "{schedule}"</td>
        <td>Schedule a job that runs a feature with specific key:value parameters separated by semi-colon (;) and crontab patterned schedules like "* * * * *" schedule can use < today > and < tomorrow > which are replaced dynamically</td>
        <td></td>
    </tr>
    <tr>
        <td>Delete schedule that executed this feature</td>
        <td>Removes the schedule that executed this feature y executed manually the step is ignored</td>
        <td></td>
    </tr>
    <tr>
        <td>Run feature with id "{feature_id}" before continuing</td>
        <td>Runs another feature using it's ID in the same context, useful to import common steps in multiple features</td>
        <td></td>
    </tr>
    <tr>
        <td>Run feature with name "{feature_name}" before continuing</td>
        <td>Runs another feature using it's name in the same context, useful to import common steps in multiple features</td>
        <td></td>
    </tr>
</table>

### Mouse actions<a name="MOUSE_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Scroll to "{amount}"px</td>
        <td>Scrolls the page to a given amount of pixels in the Y axis</td>
        <td></td>
    </tr>
    <tr>
        <td>I can click on button "{button_name}"</td>
        <td>Checks if can click in a button with the specified name attribute text</td>
        <td></td>
    </tr>
    <tr>
        <td>I can click on button with title "{button_title}"</td>
        <td>Checks if can click in a button with the specified title attribute text</td>
        <td></td>
    </tr>
    <tr>
        <td>I select option "{option_value}"</td>
        <td>Selects an option value in a select input</td>
        <td></td>
    </tr>
    <tr>
        <td>I click on element with classname "{classname}"</td>
        <td>Tries to click on an element with the specified class</td>
        <td></td>
    </tr>
    <tr>
        <td>Scroll the opened folder to the bottom</td>
        <td>Scroll the opened folder to the bottom</td>
        <td></td>
    </tr>
    <tr>
        <td>click on element with xpath "{xpath}"</td>
        <td>Click on element using an XPath Selector</td>
        <td></td>
    </tr>
    <tr>
        <td>I can Control Click at "{element}" </td>
        <td>Do a Ctrl + Click using a CSS Selector</td>
        <td></td>
    </tr>
    <tr>
        <td>Download a file by clicking on "{linktext}"</td>
        <td>Download a file, watch which file is downloaded and assign them to feature_result and step_result (linktext can be a text, css_selector or even xpath)</td>
        <td></td>
    </tr>
</table>

### Keyboard actions<a name="KEYBOARD_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Send keys "{keys}"</td>
        <td>Send any keys, this simulates the keys pressed by the keyboard</td>
        <td></td>
    </tr>
    <tr>
        <td>Press Enter</td>
        <td>Press the Enter key</td>
        <td></td>
    </tr>
    <tr>
        <td>I can do a basic auth with username "{username}" and "{password}"</td>
        <td>Do a login using Basic Auth credentials, please use variables to mask sensitive values like passwords</td>
        <td></td>
    </tr>
    <tr>
        <td>Press the following set of keys "{keySet}"</td>
        <td>Presses a set of key sent by the user as a parameter. If the keys are separated by '+', press them simultaneosly. If they are separated by ';', start pressing the keys once the previous set is released. The key combination won't work if the browser state is modified (create new tab, close browser...), </td>
        <td>Press the following set of keys "shift+alt+f+shift+alt+a"</td>
    </tr>
</table>

### IBM actions<a name="IBM_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Test IBM Cognos Cube Dimension to contain all values from list variable "{variable_name}" use prefix "{prefix}" and suffix "{suffix}"</td>
        <td>Compares a Report Cube's content to a listsaved in variable.<br/>
        Works for dimension with > 50 members (members can be searched)</td>
        <td>Test IBM Cognos Cube Dimension to contain all values from list variable "IBIS_CenterList" use prefix "IBIS-" and suffix " "</td>
    </tr>
    <tr>
        <td>I can test current IBM Cognos folder</td>
        <td>Tests the folder the user is currently in</td>
        <td>Runs a test on anything in the current folder.</td>
    </tr>
    <tr>
        <td>I can go to IBM Cognos folder "{folder_name}"</td>
        <td>Goes to the inputted folder</td>
        <td>I can go to IBM Cognos folder "Enterprise Basic;
        Business Reports;02 Monthly Reports"</td>
    </tr>
    <tr>
        <td>I can test current IBM Cognos folder using parameters "{parameters}"</td>
        <td>Tests the folder the user is currently in with the inputted parameters. Paraters is a pair of "key1|key2|key3:values;", where each key is the name a prompt parameters and the correspondig value. Multiple keys can be tied to one value like this: p_PERIOD|p_REPORTINGPERIOD|p_PER:2025-01</td>
        <td></td>
    </tr>
</table>

### IBM Cognos QueryStudio actions<a name="QUERYSTUDIO_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>I can sort QueryStudio table column with "{column_name}"</td>
        <td>Sort a QueryStudio table by a given column name</td>
        <td></td>
    </tr>
    <tr>
        <td>I can add an column with "{column_name}" to QueryStudio table </td>
        <td>Add a column name in a QueryStudio table</td>
        <td></td>
    </tr>
    <tr>
        <td>I can add an filter with "{filter_name}" to QueryStudio table</td>
        <td>Add a filter name to a QueryStudio table</td>
        <td></td>
    </tr>
    <tr>
        <td>I can add an filter to column "{column_name}" with "{filter_value}" to QueryStudio table</td>
        <td>Add a filter name with a value to a QueryStudio table</td>
        <td></td>
    </tr>
    <tr>
        <td>I can set not to the filter "{filter_text}"</td>
        <td>Negate a filter name</td>
        <td></td>
    </tr>
    <tr>
        <td>I can remove the filter "{filter_text}" </td>
        <td>Remove a filter name from a QueryStudio table</td>
        <td></td>
    </tr>
    <tr>
        <td>I can delete QueryStudio table column with "{column_name}" </td>
        <td>Remove a column name from a QueryStudio table</td>
        <td></td>
    </tr>
    <tr>
        <td>I can cut QueryStudio table column with "{column_name}" and paste it before column with "{column_name_2}"</td>
        <td>Moves a column name before another column name</td>
        <td></td>
    </tr>
</table>

### Other actions<a name="OTHER_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>A set of environments </td>
        <td>Sets a comma separated list of environments</td>
        <td></td>
    </tr>
    <tr>
        <td>Environment "{env}"</td>
        <td>Set Environment ID</td>
        <td></td>
    </tr>
    <tr>
        <td>I can test the folder "{foldername}"</td>
        <td>Test if can access to a folder relative to the root directory of the URL specified</td>
        <td></td>
    </tr>
    <tr>
        <td>I can see "{something}" on page</td>
        <td>Checks if the current source code contains something, is case sensitive!</td>
        <td></td>
    </tr>
    <tr>
        <td>I can see a link with "{linktext}"</td>
        <td>Checks if the current source code contains a link with the desired text, is case sensitive!</td>
        <td></td>
    </tr>
    <tr>
        <td>I can switch to iFrame with id "{iframe_id}"</td>
        <td>Switches to a iframe tag inside the document within the specified ID</td>
        <td></td>
    </tr>
    <tr>
        <td>I can switch to iFrame with name "{iframe_name}"</td>
        <td>Switches to an iframe tag inside the document within the specified name</td>
        <td></td>
    </tr>
    <tr>
        <td>I can see a link with "{linktext}" in iframe</td>
        <td>Check if the source code in the previously selected iframe contains a link with text something</td>
        <td></td>
    </tr>
    <tr>
        <td>I can see "{something}"</td>
        <td>Checks if the source code contains some text (it is case sensitive!)</td>
        <td></td>
    </tr>
    <tr>
        <td>I sleep "{sleeptime}" seconds<br/>
        I can sleep "{sleeptime}" seconds</td>
        <td>Sleeps for X seconds<br/>
        Helps to take screenshots properly until next action is done</td>
        <td></td>
    </tr>
    <tr>
        <td>Wait until I can see "{something}" on page</td>
        <td>Wait until I can see something (text/content) on the page.<br/>
        Useful when sleep or loading times are unknown<br/>
        Timeout after 60s.</td>
        <td>then wait until I can see "< span id="ibisscreen-id" >cm002< /span >" on page</td>
    </tr>
    <tr>
        <td>I can do a OIDC auth with username "{username}" and "{password}"</td>
        <td>Do a login using OIDC Authentication, please use variables to mask sensitive values like passwords</td>
        <td></td>
    </tr>
    <tr>
        <td>Run Javascript function "{function}"</td>
        <td>Run a JavaScript function in the current browser context</td>
        <td></td>
    </tr>
    <tr>
        <td>Throw an error with "{message}" and leave</td>
        <td>Throws an error with a custom message and stops feature execution</td>
        <td></td>
    </tr>
    <tr>
        <td>#{comment}</td>
        <td>Insert custom comments in testplans </td>
        <td>given #"here the comment starts"</td>
    </tr>
</table>

### Support<a name="SUPPORT"></a>
For further questions or issues, please contact us at our email <tec_dev@cometa.rocks> or via Discord https://discord.gg/e3uBKHhKW5
