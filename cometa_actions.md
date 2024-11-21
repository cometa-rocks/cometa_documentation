<img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png" width="600px"/>


# Co.meta steps table of contents

Co.meta offers versatile and easy to use steps like "Goto URL {URL}" or "Move mouse to {selector} and click". Below is a list of grouped actions by topic.

1. [Browser actions](#browser-actions)
2. [API actions](#api-actions)
3. [AI - actions](#ai-actions)
4. [Conditional - actions](#conditional-actions)
5. [Validation - actions](#validation-actions)
6. [CSS selectors actions](#css-selectors-actions)
7. [Feature actions](#feature-actions)
8. [Mouse actions](#mouse-actions)
9. [Keyboard actions](#keyboard-actions)
10. [IBM actions](#ibm-actions)
11. [IBM Cognos QueryStudio actions](#ibm-cognos-querystudio-actions)
12. [Editing Excel Files](#editing-excel-files)
13. [Uploading and Downloading files](#uploading-and-downloading-files)
14. [Other actions](#other-actions)
15. [Action Examples](#action-examples)
16. [Support](#support)

<br/>

# <span class="gold">Co.</span>meta steps / actions

Actions or steps are the build blocks from where your tell Co.meta what you want to automate. You have actions for clicking, browsing, screen sizing, downloading, can send keys and so on and so on.

We have grouped the different actions and the first one is "Browser actions".

The first steps in your testplan will probably be *Goto "{URL}"* - make sure to leave the quotes and replace anything else. Do not worry about escaping your quotes. Co.meta does that for you.

A very versatile step is *Run Javascript function "{function}"* - function can be anything you can execute as Javscript inside a browser. It can be just one command or a complete snippet. This brings you low-code.

If you have suggestions or needs for a step / actions that you would rather implement in python, then please download the Co.meta repo and have a look actions.py for the code of any step that was implemented here.

### Browser actions

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

### API actions

<br>You can use this JSON as an example to understand API actions. Please delete or disable the first step shown as an example and import this JSON to understand how to use API actions. 
<br>
```
[{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Make an API call with \"GET\" to \"https://petstore.swagger.io/v2/pet/59462342\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Make an API call with \"GET\" to \"https://petstore.swagger.io/v2/pet/59462342\" with \"params:param1=value1;param2=value2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".request.path\" to \"match\" \"\"/v2/pet/59462342?param1=value1&param2=value2\"\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Make an API call with \"GET\" to \"https://petstore.swagger.io/v2/pet/59462342\" with \"params:param1=value1;param2=value2\" and \"headers:header1=value1;header2=value2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.tags[0].name == \"string\"\" to \"contain\" \"false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.category.id == 0\" to \"match\" \"true\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.photoUrls | length > 0\" to \"match\" \"true\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Save last API Call property \".response.content.name\" to \"petName\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert \"$petName\" to be same as \"\"doggie\"\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.status_code\" to \"match\" \"200\"","step_type":"normal","continue_on_failure":false,"timeout":60}]
```
<br>
<br>
<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Make an API call with "{method}" to "{endpoint}" with "params:{parameters}" and "headers:{headers}"</td>
        <td>Create API step using this action where, the <code>method</code> is HTTP method (<code>GET, POST, PUT</code> or <code>DELETE</code>, etc), the endpoint is your API to be called (i.e.<code>https://petstore.swagger.io/v2/pet/59462342</code>)
        <br>
        <br>
        <b>Optionally</b> you can set query parameters and headers using the format <code>Key=Value</code>, with semicolons <code>;</code> used to separate key-value pairs (e.g., <code>Key1=value1;Key2=value2</code>)
        <br>
        <br>The Request and Response data from the last API call will be stored in memory, which can be accessed using the steps below
        </td>
        <td>
        <br><br><b>Example 1</b>
        <br> <code>Make an API call with "GET" to "https://petstore.swagger.io/v2/pet/59462342"</code>
        <br><br><b>Example 2</b>
        <br> <code>Make an API call with "GET" to "https://petstore.swagger.io/v2/pet/59462342" with "params:param1=value1;param2=value2"</code>
        <br><br><b>Example 3</b>
        <br> <code>Make an API call with "GET" to "https://petstore.swagger.io/v2/pet/59462342" with "params:param1=value1;param2=value2" and "headers:header1=value1;header2=value2"</code>
        </td>
    </tr>
    <tr>
        <td>Assert last API Call property "{jq_pattern}" to "{condition}" "{value}"</td>
        <td>
        Assert api request and response data using JQ patterns.  Please refer [JQ Documentation](https://jqlang.github.io/jq/manual/) 
        <br><br> jq_pattern is a JSON path that can also be combined with conditions to perform assertions, as shown in the given examples
        <br><br> The <code>condition</code> parameter can take either <code>match</code>  or <code>contain</code>  as a value to assert the JSON
        <br><br> <code>value</code> is the content with which we want to match
        <br><br><b>Note:</b> While comparing string remember to wrap string with ""
        </td>
        <td>
            <b>Example 1</b> Validate request data
            <br><code>Assert last API Call property ".request.path" to "match" ""/v2/pet/59462342?param1=value1&param2=value2""</code>
            <br><br><b>Example 2</b> Validate response data
            <br><code>Assert last API Call property ".response.content.tags[0].name" to "match" ""string""</code>
            <br><br><b>Example 3</b> Validate response data with JQ patterns
            <br><code>Assert last API Call property ".response.content.tags[0].name == "string"" to "match" "true"</code>
            <br><br><b>Example 4</b> Validate response data with JQ patterns
            <br><code>Assert last API Call property ".response.content.category.id == 0" to "contain" "true"</code>
            <br><br><b>Example 5</b> Validate response data with JQ patterns
            <br><code>Assert last API Call property ".response.content.photoUrls | length > 0" to "match" "true"</code>
            <br><br><b>Example 6</b> Validate response status code
            <br><code>Assert last API Call property ".response.status_code" to "match" "200"</code>
        </td>
    </tr>
    <tr>
        <td>Save last API Call property "{jq_pattern}" to "{environment_variable}"</td>
        <td>
        The last API request and response data can be saved into an environment variable using this action, which can then be used as a value for other steps or for performing assertions when required 
        </td>
        <td>
        <b>Example 1</b>
        <br> <code>Save last API Call property ".response.content.name" to "petName"</code>
        <br>
        <br>Then, use the saved data in other steps.
        <br> <code>Assert "$petName" to be same as ""doggie""</code>
        <br>
        </td>
    </tr>

</table>

### AI actions

<table> 
	<tr> 
		<th>Action</th> 
		<th>Description</th> 
		<th>Example</th> 
	</tr> 
	<tr> 
		<td>Validate current screen to contain "{object_name}" with "{options}"</td> 
		<td>Validates whether the current screen contains a specified object.<br><br> Additional options can be provided to refine the validation.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Validate current screen to contain "Car"</code><br>
			<b>Example 2 (refine validation):</b><br>
				<code>Validate current screen to contain "Car" with "color:red"</code>
		</td> 
	</tr> 
	<tr> 
		<td> Get list of visible objects in the current screen and store in "{variable}" with "{options}"</td> 
		<td>Retrieves the list of visible objects on the current screen and stores it in a specified variable. <br><br>Additional options can refine the list.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Get list of visible objects in the current screen and store in "myObjects"</code><br>
			<b>Example 2 (refine validation):</b><br>
				<code>Get list of visible objects in the current screen and store in "myObjects" with "visible_only"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Get information based on "{user_message_to_ai}" and store in "{variable}" with "{options}"</td> 
		<td>This step allows you to send a specific request or instruction to the AI, along with images or other data for analysis. The AI's response will be stored in a specified variable.<br><br>Optionally, you can modify how the result is processed by using the "Output JSON" option.</td> 
		<td>
			<b>Example 1:</b><br>
			<code>Get information based on "[{\"content\": \"Get the visible car color\", \"images\": [\"screenshot1\"]}]" and store in "chart_analysis" with "Output JSON"</code><br>
			<b>Example 2:</b><br>
			<code>Get information based on "[{'content': 'Identify all buttons on the screen', 'images': ['ui_screenshot']}}]" and store in "button_list" with "Output JSON"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Get screenshot and store in the variable "{variable_name}"</td> 
		<td>This step captures a screenshot of the current screen and stores it in the specified variable.</td> 		<td>
			<b>Example 1:</b><br>
				<code>Get screenshot and store in the variable "current_screen"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Show me variable "{variable_name}" value for "{seconds}" seconds</td> 
		<td>Displays the value of a specified variable for a certain number of seconds.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Show me variable "myVariable" value for "5" seconds</code>
		</td> 
	</tr> 
	<tr> 
		<td>Assert variable "{variable_name}" using jq_pattern "{jq_pattern}" to "{condition}" "{value}"</td> 
		<td>This step asserts that a value within a stored variable matches or contains a specified value using a JQ pattern. It is useful for validating JSON-like data structures stored in variables.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Assert variable "api_response" using jq_pattern ".status" to "match" "success"</code><br>
			<b>Example 2:</b><br>
				<code>Assert variable "api_response" using jq_pattern ".message" to "contain" "completed successfully"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Assert variable "{variable_name}" to "{condition}" "{value}"</td> 
		<td>Asserts the value of a variable directly using a condition (match or contain).</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Assert variable "status_code" to "match" "200"</code><br>
			<b>Example 2:</b><br>
  				<code>Assert variable "response_message" to "contain" "Operation completed"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Get information based on """{user_message_to_ai}""" and store in the "{variable}" with "{option}"</td> 
		<td>
			Uses AI to analyze the input provided in the format of a user message, processes the information, 
			and stores the result in the specified variable. 
			An optional parameter `option` can modify the output format (e.g., convert to JSON).
		</td> 
		<td>
			<b>Example 1:</b><br>
			<code>Get information based on """[{ "content": "Describe the image" }]""" and store in the "analysis_result" with "Output JSON"</code><br>
			<b>Example 2:</b><br>
			<code>Get information based on """[{ "content": "Summarize the data" }]""" and store in the "summary_variable"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Get information based on """{prompt}""" from current screen and store in the "{variable}" with "{option}"</td> 
		<td>
			Captures the current screen, analyzes it based on the given `prompt`, and stores the result in the specified variable.
			An optional parameter `option` can be used to process the result, such as converting it to JSON.
		</td> 
		<td>
			<b>Example 1:</b><br>
			<code>Get information based on """Extract all text in the image""" from current screen and store in the "text_output" with "Output JSON"</code><br>
			<b>Example 2:</b><br>
			<code>Get information based on """Identify objects in the image""" from current screen and store in the "object_list"</code>
		</td> 
	</tr>
</table>

### Conditional actions<a id="CSS_AC"></a>

<table> 
	<tr> 
		<th>Action</th> 
		<th>Description</th> 
		<th>Example</th> 
	</tr> 
	<tr> 
		<td>If "{value1}" "{condition}" "{value2}"</td> 
		<td>Checks if `value1` is exactly equal to `value2`.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$is_visible" "equals" "True"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" is not equal to "value2".</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$variable_1" "not equals" "$variable_2"</code><br>
			<b>Example 2:</b><br>
				<code>If "$variable_1" "not equals" "Pink"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" contains the substring "value2".</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$message" "contains" "success"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" does not contain the substring "value2".</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$message" "not contains" "error"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" is greater than or equal to "value2" (numeric comparison).</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$response_time" ">=" "200"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" is less than or equal to "value2" (numeric comparison).</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$response_time" "<=" "500"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" is equal to "value2" (numeric comparison).</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$score" "=="` "100"</code>
		</td> 
	</tr> 
	<tr> 
		<td></td> 
		<td>Checks if "value1" is not equal to "value2" (numeric comparison).</td> 
		<td>
			<b>Example 1:</b><br>
				<code>If "$score" "!=" "50"</td> 
	</tr>
	<tr> 
		<td>Else</td> 
		<td>Specifies the alternative case when `$is_visible` is not `True`.</td> 
		<td>Else.</td> 
	</tr> 
	<tr> 
		<td>End If</td> 
		<td>Closes the conditional block started by `If`.</td> 
		<td>End If.</td> 
	</tr> 
</table>

### Validation actions<a id="CSS_AC"></a>

<table>
	<tr> 
		<th>Action</th> 
		<th>Description</th> 
		<th>Example</th> 
	</tr> 
	<tr> 
		<td>Validate if "{selector}" present in the browser in "{time}" seconds and save result in "{variable}"</td> 
		<td>Checks if the specified selector is present in the browser within the given time and saves the result to a variable.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Validate if "//h1[contains(text(),'Explore projects')]" present in the browser in "15" seconds and save result in "is_visible"</code>
		</td> 
	</tr> 
	<tr> 
		<td>Validate if "{selector}" appeared in the browser in "{time}" seconds and save result in "{variable}"</td> 
		<td>Checks if the specified selector is visible in the browser within the given time and saves the result to a variable.</td>
		<td>
			<b>Example 1:</b><br>
				<code>Validate if "//h1[contains(text(),'Explore projects')]" appeared in the browser in "15" seconds and save result in "is_visible"</code>
		</td> 
	</tr> 
</table>

### CSS selectors actions<a id="CSS_AC"></a>

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
        <td>Save "{value}" to environment variable "{variable_name}"</td>
        <td>save string value to environment variable, environment variable value has a maximum value of 255 characters</td>
        <td>
        This step has multiple use cases, like setting static value or save parsed data from other steps like Javascript function.</br>
        Examples:</br>
        <ol>
            <li>
            Settings static value</br>
            <code>Save "my_email_address@cometa.rocks" to environment variable "myEmail"</code></br>
            or</br>
            <code>
            Save "my_email_address@cometa.rocks" to environment variable "UserName"</br>
            Run feature with name "FindByUserName" (which uses variable $UserName)</br>
            Save "my_second_email_address@cometa.rocks" to environment variable "UserName"</br>
            Run feature with name "FindByUserName" (which uses variable $UserName)
            </code>
            </li>
            <li>
            Parsing value from Javascript function</br>
            <code>
            Run Javascript function "return "$totalScore".replace(/[^0-9]+/, '');"</br>
            Save "%js_return" to environment variable "totalScoreWithOutText"</br>
            Assert "$expectedTotalScore" to be same as "$totalScoreWithOutText"
            </code>
            </li>
        </ol>
        </td>
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
        <td>I use selector "{number}" and select option "{index}" for Cognos prompt page</td>
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
    <tr>
        <td>Loop "{x}" times starting at "{index}" and do  /  End loop</td>
        <td>Starts a loop cycle, repeating inside defined actions as many times as indicated in "x" starting from as indicated in "index"</td>
        <td>
            <br><strong>Step 1:</strong> StartBrowser and call URL "https://datatables.net/"
            <br><strong>Step 2:</strong> Loop "5" times starting at "1" and do
		    <br><strong>Step 3:</strong> click on element with xpath "//tr[contains(@class, "even") or contains(@class, "odd")][%index]/td[1]"
            <br><strong>Step 4:</strong> I sleep "1" seconds
            <br><strong>Step 5:</strong> End Loop
            <br>
            <br>Will loop over first 5 <strong>tr</strong> elements with class <strong>"even"</strong> or <strong>"odd"</strong> and click first occurrence of <strong>td</strong> for each of them
            <br>_________________________________________________________
            <br>
            <br>
            <br><strong>Step 1:</strong> StartBrowser and call URL "https://google.com/"
            <br><strong>Step 2:</strong> I move mouse to "//div/button[2]" and click
		    <br><strong>Step 3:</strong> I move mouse to "//input" and click
            <br><strong>Step 4:</strong> Loop "5" times starting at "1" and do
            <br><strong>Step 5:</strong> Send keys " : Index %index : "
            <br><strong>Step 6:</strong> End Loop
            <br>
            <br>Will open google and introduce in search input <strong>: index 1 :  : index 2 :  : index 3 :  : index 4 :  : index 5 :</strong>
            <br>_________________________________________________________
        <td>
    </tr>
</table>

### Feature actions<a id="FEATURE_AC"></a>

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

### Mouse actions<a id="MOUSE_AC"></a>

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
        <td>Downloads a file, the downloaded file is assigned to feature_result and step_result (linktext can be a text, css_selector or xpath). The downloaded file is saved in the file systems at behave/Downloads/{feature-run-id}/remove-filename.suffix. To be able to test on generic filenames, that get random generated Id's, Cometa saves a copy of the file to last_downloaded_file.suffix maintaining the suffix of the original filename.
        </td>
        <td></td>
    </tr>
    <tr>
        <td>Drag "{element_selector}" and drop it in "{destination_selector}"</td>
        <td>Drag an element and drop it to the destination element</td>
        <td></td>
    </tr>
        <tr>
        <td>Scroll to the last position of the desired element identified by "{xpath}" with maximum number of scrolls "{MaxScrolls}" and maximum time of "{MaxTimeOfLife}"</td>
        <td>Scroll to element with "{xpath}" repeatedly until it finds last position. This feature is useful when searching for an element that is not initially loaded and requires multiple dynamic loads.</td>
        <td>
            <br/>Scroll to the last position of the desired element identified by "//ol/li[last()]" with maximum number of scrolls "50" and maximum time of "120"
        </td>
    </tr>
        <tr>
        <td>Scroll to element with "{selector}" in lazy loaded table "{scrollable_element_selector}"</td>
        <td>This step scrolls to a selector contained in a lazy loaded table which only shows up to few elements and the rest of them are dynamically loaded. For example AG-Grid tables.</td>
        <td></td>
    </tr>
</table>

### Keyboard actions<a id="KEYBOARD_AC"></a>

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
        <td style="vertical-align:top">Press the following set of keys "{keySet}"</td>
        <td>Presses a set of key sent by the user as a parameter. If the keys are separated by '+', press them simultaneously. If they are separated by ';', start pressing the keys once the previous set is released. The key combination won't work if the browser state is modified (create new tab, close browser...).
        <br><p>
        <br><p>
        Here is the complete list of Special Keys that can be used in Cometa via Selenium Webdriver:
        <table>
        <tr>
            <td>ADD</td>	<td>ALT</td>	<td>ARROW_DOWN</td>
        </tr>
        <tr>
            <td>ARROW_LEFT</td>	<td>	ARROW_RIGHT</td>	<td>	ARROW_UP</td>
        </tr>
        <tr>
            <td>BACKSPACE</td>	<td>	BACK_SPACE</td>	<td>	CANCEL</td>
        </tr>
        <tr>
            <td>CLEAR</td>	<td>	COMMAND</td>	<td>	CONTROL</td>
        </tr>
        <tr>
            <td>DECIMAL</td>	<td>	DELETE</td>	<td>	DIVIDE</td>
        </tr>
        <tr>
            <td>DOWN</td>	<td>	END</td>	<td>	ENTER</td>
        </tr>
        <tr>
            <td>EQUALS</td>	<td>	ESCAPE</td>	<td>	F1</td>
        </tr>
        <tr>
            <td>F10</td>	<td>	F11</td>	<td>	F12</td>
        </tr>
        <tr>
            <td>F2</td>	<td>	F3</td>	<td>	F4</td>
        </tr>
        <tr>
            <td>F5</td>	<td>	F6</td>	<td>	F7</td>
        </tr>
        <tr>
            <td>F8</td>	<td>	F9</td>	<td>	HELP</td>
        </tr>
        <tr>
            <td>HOME</td>	<td>	INSERT</td>	<td>	LEFT</td>
        </tr>
        <tr>
            <td>LEFT_ALT</td>	<td>	LEFT_CONTROL</td>	<td>	LEFT_SHIFT</td>
        </tr>
        <tr>
            <td>META</td>	<td>	MULTIPLY</td>	<td>	NULL</td>
        </tr>
        <tr>
            <td>NUMPAD0</td>	<td>	NUMPAD1</td>	<td>	NUMPAD2</td>
        </tr>
        <tr>
            <td>NUMPAD3</td>	<td>	NUMPAD4</td>	<td>	NUMPAD5</td>
        </tr>
        <tr>
            <td>NUMPAD6</td>	<td>	NUMPAD7</td>	<td>	NUMPAD8</td>
        </tr>
        <tr>
            <td>NUMPAD9</td>	<td>	PAGE_DOWN</td>	<td>	PAGE_UP</td>
        </tr>
        <tr>
            <td>PAUSE</td>	<td>	RETURN</td>	<td>	RIGHT</td>
        </tr>
        <tr>
            <td>SEMICOLON</td>	<td>	SEPARATOR</td>	<td>	SHIFT</td>
        </tr>
        <tr>
            <td>SPACE</td>	<td>	SUBTRACT</td>	<td>	TAB</td>
        </tr>
        </table>
        </td>
        <td style="vertical-align:top">Press the following set of keys "shift+alt+f;shift+alt+a"</td>
    </tr>
</table>

### IBM actions<a id="IBM_AC"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Test IBM Cognos Cube Dimension to contain all values from list variable "{variable_name}" use prefix "{prefix}" and suffix "{suffix}"</td>
        <td>Compares a Report Cube's content to a list saved in variable.<br/>
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
        <td>Navigates to the selected folder. If folders are nested use ";" to separate items.</td>
        <td>I can go to IBM Cognos folder "Enterprise Basic;
        Business Reports;02 Monthly Reports"</td>
    </tr>
    <tr>
        <td>I can test current IBM Cognos folder using parameters "{parameters}"</td>
        <td>Tests the folder the user is currently in with the inputted parameters. Parameters is a pair of "key1|key2|key3:values;", where each key is the name a prompt parameters and the corresponding value. Multiple keys can be tied to one value like this: p_PERIOD|p_REPORTINGPERIOD|p_PER:2025-01</td>
        <td></td>
    </tr>
</table>

### IBM Cognos QueryStudio actions<a id="QUERYSTUDIO_AC"></a>

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

### Editing Excel Files<a id="EDITEXCEL_AC"></a>

Cometa uses [openpyXL library](https://openpyxl.readthedocs.io/en/stable/) for working with Excel files. This library is powerful, when it comes to handling with Excel, it can transform Excel lists in Crosstabs, set formatting and many more. Cometa only uses Edit and Assert value for now. Feel free add functionality you need. 

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Edit "{excelfile}" and set "{value}" to "{cell}"</td>
        <td>Opens the excel file and sets a value to a cell. </td>
        <td>Example: <code>Edit "Downloads/myexcel.xlsx" and set "Cometa was here" to "C3"</code></td>
    </tr>
    <tr>
        <td>Open "{excelfile}" and assert "{value}" is in cell "{cell}"</td>
        <td>Opens the excel file and asserts that value is found in cell. </td>
        <td>Example: <code>Open "Downloads/file_example_XLSX_1000.xlsx" and assert "COMETA" is in cell "A2"</code></td>
    </tr>
    <tr>
        <td>Open "{excelfile}" and set environment variable "{variable_name}" with value from cell "{cell}"</td>
        <td>Opens the excel file reads value found in cell and saves that value to a Cometa environment variable. </td>
        <td>Example: <code>Open "Downloads/file_example_XLSX_1000.xlsx" and set environment variable "EXCEL" with value from cell "E2"</code>. This will result in the environment variable EXCEL to contain the value "United States".</td>
    </tr>
    <tr>
        <td>Open Excel from "{file}" and test that cells "{excel_range}" contain "{values}" options "{match_type}"</td>
        <td>
            Opens Excel or CSV file and asserts the values in the cell range specified.
            <br><br>
            Cell range can be any number of range as long as it cell length is not grater than the values length. If we don't know how many items there are in the values we can use a range like <code>A12:A</code> this will take <code>A12</code> as a starting cell and calculate the rows based on the items in values. This only works vertically (rows) so range like <code>A12:C</code> won't work. Other possible ranges can be: <code>A12:500</code> or even <code>A12:C13</code>, this last one will assert the value in the following order: <code>A12 => B12 => C12 => A13 => B13 => C13</code>.
            <br><br>
            Values are content that will be asserted and should be separated by semicolons (;).
            <br><br>
            Match type can be one of the followings:
            <li><code>match exact</code>: Will fail the step if any of the assertions are failed. For e.g.: A12 should contain "Hi!" but contains "Hello!".</li>
            <li><code>match partial</code>: Will pass the step if any of the assertions are passed. For e.g.: A12 should contain "Hi!", contains "Hello!" but A13 should contain "Bye" and matches to cell value "Bye". Overall step passes.</li>
            <li><code>match any</code>: WIP</li>
            <li><code>match x number of times</code>: WIP</li>
            <br><br>
            Generates an CSV file containing all the details about the assertions and why if might have failed.
        </td>
        <td>
            Examples:
            <br><br>
            <code>Open Excel from "Downloads/last_downloaded_file.xlsx" and test that cells "A1:A" contain "Arslan;Ralf;Tornike" options "match exact"</code>
            <br><br>
            <code>Open Excel from "Downloads/last_downloaded_file.csv" and test that cells "A20" contain "500" options "match exact"</code>
            <br><br>
            <code>Open Excel from "Downloads/last_downloaded_file.csv" and test that cells "A20:C20" contain "2019;2020;2021" options "match partial"</code>
        </td>
    </tr>
</table>

<details>
    <summary>Here is a test example for further demonstration: </summary>

  <pre>
  [{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"# download an excel file","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://file-examples.com/index.php/sample-documents-download/sample-xls-download/\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ download file from given link in HTML ################","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Download a file by clicking on \"(//a[contains(@href,'_1000.xls')])[2]\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":false,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Run feature with name \"WAIT-LOOP\" before continuing","step_type":"subfeature","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"# open that excel file","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Goto URL \"https://products.aspose.app/cells/es/viewer\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Upload a file by clicking on \".uploadFileInput\" using file \"Downloads/file_example_XLSX_1000.xlsx\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"I sleep \"10\" seconds","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"# edit the excel file","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":false,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Run feature with name \"WAIT-LOOP\" before continuing","step_type":"subfeature","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Edit \"Downloads/file_example_XLSX_1000.xlsx\" and set \"COMETA\" to \"A2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Edit \"Downloads/file_example_XLSX_1000.xlsx\" and set \"was\" to \"B2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Edit \"Downloads/file_example_XLSX_1000.xlsx\" and set \"here\" to \"C2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"# Reopen the excel file to see the changes","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Goto URL \"https://products.aspose.app/cells/es/viewer\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Upload a file by clicking on \".uploadFileInput\" using file \"uploads/file_example_XLSX_1000.xlsx\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"I sleep \"10\" seconds","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"# Assert that a certain cell has a certain value","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Open \"Downloads/file_example_XLSX_1000.xlsx\" and assert \"COMETA\" is in cell \"A2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":false,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"I sleep \"10\" seconds","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Open \"Downloads/file_example_XLSX_1000.xlsx\" and set environment variable \"EXCEL\" with value from cell \"E2\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"I sleep \"10\" seconds","step_type":"normal","continue_on_failure":false,"timeout":60}]
  </pre>
</details>
<br>

### Uploading and Downloading files<a id="FILES"></a>

<table>
    <tr>
        <th>Action</th>
        <th>Description</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>Upload a file by clicking on "{selector}" using file "{filename}"</td>
        <td>Uploads a file to an input selector</td>
        <td>Upload a file by clicking on "//input[@id="upload-button"]" using file "uploads/dummy.png;uploads/dummy.mp4" ... you can upload multiple file by separating them by a semicolon. The semicolon is being replaced by a carriage return in Cometa.</td>
    </tr>
    <tr>
        <td>Download a file by clicking on "{linktext}"</td>
        <td>This will download the file in the linktext to the Downloads folders of the headless browser.</td>
        <td>If you are downloading a generic file, you can use `last_downloaded_file.{same suffix}` to access files that have ID's automatically generated.</td>
    </tr>
    <tr>
        <td>Attach the "{filename}" from Downloads folder to the current execution results</td>
        <td>This will attach the file found in Downloads-folder to the current execution.</td>
        <td>This is useful, if you want to examine the file in your test execution instead of your application. The filename should just be the filename. Cometa will automatically at the correct folder to the file to be downloaded from your feature results, as this is depending on the result execution number, which also goes directly into the download link.</td>
    </tr>    
</table>

### Other actions<a id=#OTHER_AC></a>
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
        <td>Switches to a iframe tag inside the document within the specified ID. It is also possible to switch to an iframe based on its index, e.g., 1 or 2 ...</td>
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
        <td>Wait "{timeout}" seconds for "{selector}" to appear and disappear using option "{option}"</td>
        <td>This step waits for the selector to appear within the given timeout (in seconds) and then wait the step timeout to disappear. The available options are 'do not fail if not visible' or 'fail if never visible'
        <br><br>
        <b> If the selector does not appear within the specified timeout, and the selected option is:</b><br/>
            <b>1.</b> <code>"do not fail if not visible"</code> then the step will not fail, and it will skip the wait for it to disappear<br/>
            <b>2.</b> <code>"fail if never visible"</code> then step will fail<br/>
            <b>3.</b> <code>"reload page after appearing"</code> then the page is reloaded 0.5 seconds after the selector appear<br/>
            <b>4.</b> <code>"reload page while waiting to disappear"</code> then the page is reloaded every minute while waiting to disappear.<br/>
        <br/>Useful when testing loading, notification pop-ups, selector that appears and disappears after reloading or selector that appear and disappears within specific time<br/>
        <br/><b>Note </b> This step checks for the presence and visibility of the selector on the screen. If the selector is present in the DOM but hidden due to CSS properties, the step will fail if selected option is <code>'fail if never visible'</code>
        <br/>
        <br/>
        <br><a href="#example-of-wait-timeout-seconds-for-selector-to-appear-and-disappear-using-option-option">Try using this example</a>
        </td>
        <td>
        <b>Examples 1</b> The spinner appears within 1 second and disappears within 40 seconds. Create step with a timeout of 2 seconds and a step timeout of 60 seconds, using the option 'do not fail if not visible', the step will run for 41 seconds with success
        <br><code>Wait "2" seconds for ".remove-element .loader" to appear and disappear using option "do not fail if not visible"</code>
        <br>
        <br>
        <b>Examples 2</b> The spinner appears within 1 second and disappears within 13 seconds. Create step with a timeout of 2 seconds and a step timeout of 60 seconds, using the option 'do not fail if not visible', the step will run for 14 seconds with success
        <br><code>Wait "2" seconds for ".hide-element .loader" to appear and disappear using option "do not fail if not visible"</code>
        <br>
        <br>
        <b>Examples 3</b> The spinner never appears and step timeout of 2 seconds and a step timeout of 60 seconds, using the option 'do not fail if not visible', the step will run for 2 seconds with success
        <br><code>Wait "2" seconds for ".hide-element .loader" to appear and disappear using option "do not fail if not visible"</code>
        <br>
        <br>
        <b>Examples 4</b> The spinner appears within 10 seconds and disappears within 15 seconds. Create step with a timeout of 2 seconds and a step timeout of 60 seconds, using the option 'do not fail if not visible', the step will run for 2 seconds with success
        <br><code>Wait "2" seconds for ".hide-element .loader" to appear and disappear using option "do not fail if not visible"</code>
        <br>
        <br>
        <b>Examples 5</b> The spinner appears within 10 seconds and disappears within 15 seconds. Create step with a timeout of 2 seconds and a step timeout of 60 seconds, using the option 'fail if never visible', the step will run for 2 seconds and fail
        <br><code>Wait "2" seconds for ".hide-element .loader" to appear and disappear using option "fail if never visible"</code>
        <br>        
        <br> 
        <b>Examples 6</b> The selector appears within 20 seconds and disappears after 10 minute and to check if disappeared page reloading is required, Create step with a timeout of 21 seconds and a step timeout of 605 seconds (10*60 + 5 sec extra), using options 'reload page while waiting to disappear;fail if never visible', the step will run for around 605 seconds and it will pass.
        <br> <b>Note : </b> we have combined the two options <code>reload page while waiting to disappear</code> and <code>fail if never visible</code>, You can also combine it with <code>do not fail if not visible</code>.<br>
        <br><code>Wait "21" seconds for ".selector" to appear and disappear using option "reload page while waiting to disappear;fail if never visible"</code>
        <br>        
        <br>
        <b>Examples 7</b> The selector appears within 20 seconds and disappears when page reloaded, Create step with a timeout of 21 seconds and a step timeout of 25 seconds (20 + 5 sec extra), using options 'reload page after appearing;do not fail if not visible', the step will run for around 25 seconds and it will pass.
        <br> <b>Note : </b> we have combined the two options <code>reload page after appearing</code> and <code>do not fail if not visible</code>, You can also combine it with <code>fail if never visible</code><br>
        <br><code>Wait "21" seconds for ".selector" to appear and disappear using option "reload page after appearing;do not fail if not visible"</code>
        <br>        
        <br>
        <b>Examples 8</b> If <code>#Load_in_15_Secs</code> is a selector that appears within 15 seconds and disappears in the next 20 seconds. In this case, the step should be:
        <br><code>Wait "15" seconds for "#Load_in_15_Secs" to appear and disappear using option "do not fail if not visible"</code>
        <br> And set a 35 second or more in step timeout because to complete the execution of this step will require <code>15 + 20 = 35</code> seconds.
        <br><b>Note:</b> Even if the above step selector does not appear the step will not fail because the selected option is <code>'do not fail if not visible'</code>
        <br>
        <br>
        <b>Examples 9</b> If <code>#Load_in_20_Secs</code> is a selector that appears within 20 seconds and disappears in the next 300 seconds, In this case, the step should be:
        <br><code>Wait "20" seconds for "#Load_in_20_Secs" to appear and disappear using option "fail if never visible"</code>
        <br> And set a 320 second or more step timeout because to complete the execution of this step will require <code>20 + 300 = 320</code> seconds.
        <br><b>Note </b>If the above step selector does not appear step will fail because selected option is <code>'fail if never visible'</code>
        <br>
        <br><b>Examples 2</b>
        <br><code>Wait "22" seconds for "#Load_in_20_Secs" to appear and disappear using option "fail if never visible"</code>
        </td></tr>
        <tr>
          <td><strong>Wait until "{selector}" is loaded</strong><br>
          Useful as an alternative to the "wait until I can see something on page" step if you want to dynamically wait for an element to appear.<br/>
        </td>
        <td>then wait until "//div[@class='div_class_name']" is loaded</td>
    </tr>
    <tr>
        <td>I can do a OIDC auth with username "{username}" and "{password}"</td>
        <td>Do a login using OIDC Authentication, and please use variables to mask sensitive values like passwords.</td>
        <td>
            <b>Example 1</b>
            <strong>Step 1:</strong> Select Action -> <code>I can do a OIDC auth with username "{username}" and
            "{password}"</code>
            <br><strong>Step 2:</strong> Enter -> "Test_User"
            <br><strong>Step 3:</strong> Enter -> "Test_Password"
            <b>Example 2 Save password with encryption </b>
            <strong>Step 1:</strong> Select Action -> <code>I can do a OIDC auth with username "{username}" and "{password}"</code>
            <br><strong>Step 2:</strong> Enter -> "Test_User"
            <br><strong>Step 3:</strong> "Save your password in environment variables with encryption.
            <br><strong>Step 4:</strong> Enter <code>"$myPasswordVariableName"</code>
            <h4>Using an unencrypted password poses a security risk and should be avoided. It is recommended to use Example 2.</h4>
        </td>
    </tr>
    <tr>
        <td>Run Javascript function "{function}"</td>
        <td>Run a JavaScript function in the current browser context, if some value is returned from the function it will be saved as %js_return which can later be used in co.meta.</td>
        <td>
        <code>
        Run Javascript function "return "$myCometaVariable".replace(/[^0-9]+/, "");" <br />
        Assert "$expectedTotalScore" to be same as "%js_return"
        </code>
        </td>
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
    <tr>
        <td>Edit "{excelfile}" and set "{value}" to "{cell}"</td>
        <td>Updates excel file cell with new value.</td>
        <td>
            <br><strong>Step 1:</strong> StartBrowser and call URL "https://file-examples.com/index.php/sample-documents-download/sample-xls-download/"
            <br><strong>Step 2:</strong> Download a file by clicking on "(//td[text()="1000 rows"]/parent::tr//a)[2]"
		    <br><strong>Step 3:</strong> Edit "Downloads/file_example_XLSX_1000.xlsx" and set "50" to "F2"
            <br><strong>Step 4:</strong> Goto URL "https://products.aspose.app/cells/es/viewer"
            <br><strong>Step 5:</strong> Upload a file by clicking on ".uploadFileInput" using file "uploads/file_example_XLSX_1000.xlsx"
            <br>
            <br> This will download an excel file with dummy data. Dummy file will be downloaded to <code>Downloads/</code>, we will edit the file inside <code>Downloads/</code> and update it's content. Once excel file is updated it will be save to <code>uploads/</code> folder (for now, it might change in the future). Finally we view the edited file in an online excel viewer.
            <br>
        </td>
    </tr>
    <tr>
        <td>Create one-time password of "{x}" digits using pairing-key "{value}" and save it to encrypted variable "{variable_name}"</td>
        <td>
            It generates an OTP for Multi-Factor authentication and stores it in the provided <i>variable_name</i> 
            <br><br>See detailed documentation on <a href="./MFA_Authentication_using_cometa.md" target="_blank">Automation of Multi Factor Authentication with Cometa</a>
        </td>
        <td>
            <h4>Example</h4>
            <strong>Step 1:</strong> Select Action -> Create one-time password of "{x}" digits using pairing-key "{value}" and save it to encrypted variable "{variable_name}"
            <br><strong>Step 2:</strong> Enter {x} -> "8" <i>Length of OTP, | Default : 6, Options are [6, 7, 8]</i>    
            <br><strong>Step 3:</strong> Enter {value} -> "HVVH FUSO XXXX HLH7 FQKE JU2L ZZEU E2XV"
            <br><strong>Step 4:</strong> Enter {variable_name} -> "myOTPVariableName"
            <h4>Note: The stored OTP value will be encrypted, and it expires in 30 seconds.</h4>
        </td>
    </tr>
</table>

### Action Examples
You can import the below examples to create features and understand Cometa steps.

#### Example of <code>Wait "{timeout}" seconds for "{selector}" to appear and disappear using option "{option}"</code><a id="Appear_and_Disappear">
```
[{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://prod.cometa.rocks/loader_testing.html?appearTimeout=1&disappearTimeout=40&startWithLoader=false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"Wait \"2\" seconds for \".remove-element .loader\" to appear and disappear using option \"do not fail if not visible\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://prod.cometa.rocks/loader_testing.html?appearTimeout=1&disappearTimeout=13&startWithLoader=false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"Wait \"2\" seconds for \".hide-element .loader\" to appear and disappear using option \"do not fail if not visible\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://prod.cometa.rocks/loader_testing.html?appearTimeout=1000&disappearTimeout=13&startWithLoader=false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"Wait \"2\" seconds for \".hide-element .loader\" to appear and disappear using option \"do not fail if not visible\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://prod.cometa.rocks/loader_testing.html?appearTimeout=10&disappearTimeout=15&startWithLoader=false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"Wait \"2\" seconds for \".hide-element .loader\" to appear and disappear using option \"do not fail if not visible\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"StartBrowser and call URL \"https://prod.cometa.rocks/loader_testing.html?appearTimeout=10&disappearTimeout=15&startWithLoader=false\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":true,"step_keyword":"Given","compare":false,"step_content":"Wait \"2\" seconds for \".hide-element .loader\" to appear and disappear using option \"fail if never visible\"","step_type":"normal","continue_on_failure":false,"timeout":60}]
```

### Support<a id="SUPPORT"></a>
For further questions or issues, please contact us at our email <tec_dev@cometa.rocks> or via Discord https://discord.gg/e3uBKHhKW5
