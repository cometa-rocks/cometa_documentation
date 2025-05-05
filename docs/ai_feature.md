<img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png" width="600px"/>


# Co.meta steps table of contents

Co.meta offers versatile and easy to use steps like "Goto URL {URL}" or "Move mouse to {selector} and click". Below is a list of grouped actions by topic.

1. [AI - actions](#ai-actions)


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
		<td>Get information from current screen based on "{prompt}" and store in "{variable}" with "{option}"</td> 
		<td>Analyzes the current screen based on the given prompt and stores the result in a specified variable. Optionally, the result can be formatted in JSON using the "Output JSON" option.</td> 
		<td>
			<b>Example 1:</b><br>
				<code>Get information from current screen based on "[{\"content\": \"Extract visible text\"}]" and store in "extracted_text"</code><br>
			<b>Example 2:</b><br>
				<code>Get information from current screen based on "[{\"content\": \"Identify all input fields\"}]" and store in "input_list" with "Output JSON"</code>
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
</table>
