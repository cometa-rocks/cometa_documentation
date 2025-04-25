<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

<h1>FAQ & Common Questions</h1>

<h2>General Framework and Functionality</h2>

<b>1. How to generate random IDs, names, emails, or any digits in the framework</b><br> 
Create a string of random ```{x}``` numbers and save to ```{variable_name}```  
Anything missing can easily be added.

<b> 2. Is it possible to store XPath in a local variables on a per-feature basis?</b><br>
Yes

<b> 3. Is it possible to store all common XPaths of the entire application in a global variable?</b><br>
Yes - limited department wide. If you create a department, which is common to everybody (e.g. DEFAULT/PUBLIC), then you can share between all users/departments.<br>

<b> 4. Is it possible to create all common methods in a global feature file to call inside any feature?</b><br>
Yes. Cometa will detect endless loops like: include f1, which includes F2, F2 includes F3, which includes F1 <- results in feature not to be able to be saved.<br>

<b> 5. How to run only smoke test cases when having multiple smoke and regression feature files in a folder</b><br>
See https://www.youtube.com/watch?v=So_I8CjoRPI - Minute around 5:00<br>

<b> 6. Is it possible to write custom logic in this framework?</b><br>
There is a step dedicated to running custom JS methods <br>
```Run Javascript function "{function}"```
<br>
Add your steps here: https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/actions.py
<br>
See how special steps for testing "IBM Cognos" are grouped here: https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/tools/cognos.py

<b> 7. Is it possible to directly move to any dependent feature files?</b><br>
Need to implent

<b> 8. How to run all test feature files using a CI/CD pipeline like Jenkins or GitLab after deployment</b><br>
Cometa offers REST API. Anything you can do from the frontend, you can to in the pipeline.
<br>
E.g. click on "..." of a folder and run all tests inside.
<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/runAllFeatures.png)

<b> 9. Executing smoke and regression test cases feature-wise?</b><br>
See https://www.youtube.com/watch?v=So_I8CjoRPI - Minute around 5:00

<b> 10. How to integrate scripts into a CI/CD pipeline? For example, if a new build is deployed on a testing server, how will it trigger the script and email the report to the required recipient</b><br>

<h2> Database Testing</h2>

<b> Database Testing feature showcase: https://youtu.be/uGRXoUh3aFA</b>

<b> 11. How to connect to our database server using the framework</b><br>
Please watch the video on Database Testing linked above.

<b> 12. How to read, write, update, and delete data using the framework</b><br>
Please watch the video on Database Testing linked above.

<b> 13. How to retrieve data from the database</b><br>
You can assert on the result using JQ.

<b> 14. How to perform database testing</b><br>
Please watch the video on Database Testing linked above.

<h2> Mobile and Performance Testing</h2>

<b> Mobile testing feature showcase: "mobile video here"</b><br>

<b> Load testing feature showcase: https://youtu.be/hWAyx6iBbU4</b><br>


<b> 15. Is it possible to create a mobile department? and what are its related functionalities?</b><br>
Cometa currently does not feature mobile exclusive departments.<br>
Please watch the video on Mobile Testing linked above.

<b> 16. How to perform performance testing (load, stress) using the framework</b><br>
Please watch the video on Load Testing linked above.

<b> 17. How to do non-functional testing like load or stress.</b><br>
Please watch the video on Load Testing linked above.

<h2>Cloud Execution</h2>

<b> 18. Is it possible to run code in the cloud?</b><br>
Cometa can be used as SaaS or be installed on-premises or on-cloud.<br>
Cometa Team can install as well as maintain where ever you want.<br>
Sharing Features between installations per copy and import - without transportation of variables.<br>

<h2>String Methods in the Framework</h2>

<h3>Cometa uses JQ for everything related to string and json object manipulation please follow this manual and the examples below in case of doubts: https://jqlang.org/manual/</h3> <br>
<details>
  <summary><h3>Cometa test in json format used in the following questions</h3></summary>
  [{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Make an API call with \"GET\" to \"https://api.restful-api.dev/objects\"","step_action":"Make an API call with \"{method}\" to \"{endpoint}\" with \"params:{parameters}\" and \"headers:{headers}\" and \"body:{body}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares 2 objects ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data == {\"color\":\"Cloudy White\", \"capacity\":\"128 GB\"}\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares 2 strings ignoring case of input ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | ascii_downcase == \"cloudy white\"\" to \"match\" \"true\"","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks length  ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | length == 12\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks if input contains Indicated Letter ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | index(\"C\") != null\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step tests matching number -> cast to string to regex ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[3].data.price | tostring |test(\"^[0-9]+\\\\.[0-9]+$\") == true\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step replaces substring with another substring ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | gsub(\"White\" ; \"Blue\") == \"Cloudy Blue\"\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step extracts a portion of a string using indexes ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | .[2:8] == \"oudy W\"\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares two strings lexicographically replace with '==', '>' and '<' ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color > .response.content.[0].data.capacity\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks for a specific character in a specific index ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | explode | .[7] | [.] | implode == \"W\"\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60}]
</details><br>

<b>19. How to verify if two strings are exactly the same in the framework</b><br>
With action ```Assert last API call```, using JQ, we can compare strings such as:
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/stringCompare.png)
<br>
In this example we compare the color of an object and check if the output is true


<b> 20. What is the difference between equals and == when comparing strings?</b><br>
As of now there is no equals() filter in JQ, ```==``` is used to compare both strings and objects alike.
<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/stringAndObjectComparison.png)


<b> 21. How to compare two strings while ignoring their case in the framework</b><br>
Adding ```| ascii_downcase``` as a filter, will handle input string as lowercase
<br>
For example:
<br>
 ``` 'response.content.[0].data.color | ascii_downcase == "cloudy white"' ``` 
<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/caseInsensitive.png)


<b> 22. Can equalsIgnoreCase be used to compare strings with special characters?</b><br>
There is no ```equalsIgnoreCase``` method in jq. However, ```ascii_downcase``` will only affect characters that have a lowercse counterpart in ASCII.<br>
For example ```Hello@//(())??*¿¿ | ascii_downcase``` will only affect the first 'H'
For non ASCII characters like unicode, preprocessing the string will be the best solution. 

<b> 23. How to check if a string contains a specific substring in the framework</b><br>
Using ```index(<substring>)```.<br>
This will return the starting index of the substring if found, else it will return ```null```<br>
We can check the existence of a substring by using: <br>
```Assert last API Call property ".response.content.[0].data.color | index("C") != null" to "match" "true" ```<br>
 Being the input "```Cloudy White```", the return should be ```0 != null = true```.

<b> 24. What does the contains method return if the substring is not found?</b><br>
See above

<b> 25. How to verify if a string starts with a specific prefix in the framework</b><br>
```Assert last API Call property ".response.content.[0].data.color | index("C") == 0" to "match" "true"``` <br>
This example checks if ```C``` prefix is found as a substring in index ```0```.

<b> 26. What happens if the prefix is longer than the string itself?</b><br>
```index()``` returns ```null```

<b> 27. How to check if a string ends with a specific suffix in the framework</b><br>
For this usecase, use ```endswith(<suffix>)```. Returning a boolean whether it finds it or not.

<b> 28. Can endsWith be used with an empty string?</b><br>
Yes, it can. Unless the substring is an empty string, it will return ```false```.

<b> 29. How to verify if a string is empty in the framework</b><br>
Use ```length``` method
<br>
Example:
<br>
```Assert last API Call property ".response.content.[0].data.color | length == 0" to "match" "true"``` 

<b> 30. What is the difference between isEmpty and checking if the string is null?</b><br>
jq does not have a ```isEmpty``` method, however checking with ```==``` can be used to check if the string is ```""``` empty or ```null```

<b> 31. How to determine the length of a string in the framework</b><br>
Use ```length``` method
<br>
Example:
<br>
```Assert last API Call property ".response.content.[0].data.color | length == 0" to "match" "true" ```

<b> 32. What does the length method return for an empty string?</b><br>
```0```

<b> 33. How to check if a string matches a specific regular expression in the framework</b><br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/regularExpression.png)<br>
In this example we use a regular expression to check if the input is a price number followed by a '.' followed by cents<br>
Also added ```tostring``` to parse the price as a ```string```.


<b> 34. Can matches be used to validate email addresses or phone numbers?</b><br>
Yes, to validate an email use the same logic of regular expressions displayed in JQ Manual<br>
Example for Email:  ```^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$```
<br>
Example for Phone (Spanish format 9 digit): ```^[0-9]{9}$```

<b> 35. How to replace a specific character or substring in a string in the framework</b><br>
use ```gsub()``` method<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/replaceString.png)



<b> 36. What happens if the substring to be replaced is not found?</b><br>
```gsub()``` returns the original string, unmodified

<b> 37. How to replace all occurrences of a substring or pattern in a string in the framework</b><br>
```gsub()``` also replaces all occurrences it finds of the first argument, with the second

<b> 38. What is the difference between replace and replaceAll?</b><br>
These methods are not available in JQ, ```gsub()``` provides all the tools necessary for string manipulation.

<b> 39. How to convert a string to lowercase in the framework</b><br>
```ascii_downcase```

<b> 40. Does toLowerCase modify the original string?</b><br>
No, jq functions are immutable; they return new values.

<b> 41. How to convert a string to uppercase in the framework</b><br>
```ascii_upcase```

<b> 42. Can toUpperCase handle non-English characters?</b><br>
```ascii_upcase``` and ```ascii_downcase``` work only for ASCII characters. Other Unicode cases require external handling

<b> 43. How to remove leading and trailing whitespace from a string in the framework</b><br>
Use ```ltrimstr(string)``` and ```rtrimstr(string)``` <br>
Both functions output the input without the prefix/suffix indicated as argument, if it exists.

<b> 44. Does trim remove spaces between words in a string?</b><br>
The above methods only remove leading and trailing strings

<b> 45. How to extract a portion of a string in the framework</b><br>
Use ```.[x:y]```
<br>
Example: Given ```Assert last API Call property ".response.content.[0].data.color | .[2:8] == "oudy W"" to "match" "true"```

<b> 46. What happens if the start or end index is out of bounds?</b><br>
When indexes are out of bounds, ```.[x,y]``` <br>
If index goes beyond the max length, index is treated as max length<br>
if index is negative, it will count from the end
Example: Cloudy White<br>
```[0:9999]``` -> ```Cloudy White```<br>
```[99:9999]``` -> ```""```<br>
```[-4:11]``` -> ```hit```<br>
```[1:-4]``` -> ```loudy W```<br>

<b> 47. How to compare two strings lexicographically in the framework</b><br>
Use ```==```, ```>```, ```<``` for lexicographical comparison<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/lexicographicComparison.png)

<b> 48. What does a negative, zero, or positive return value from compareTo indicate?</b><br>
jq doesn't have ```compareTo```, but lexicographic comparison is done using ```<```, ```>```, and ```==```.


<b> 49. How to compare two strings lexicographically while ignoring case in the framework</b><br>
Convert both to lowercase using ```ascii_downcase``` before comparison.

<b> 50. What is the difference between compareTo and compareToIgnoreCase?</b><br>
See #48 and #49

<b> 51. How to find the index of a specific character or substring in a string in the framework</b><br>
use ```index()```, it will return the index of the character / first character in the substring

<b> 52. What does indexOf return if the character or substring is not found?</b><br> 
index returns ```null``` if not found.

<b> 53. How to find the last occurrence of a specific character or substring in a string in the framework</b><br>
Use ```rindex(string)```

<b> 54. What is the difference between indexOf and lastIndexOf?</b><br>
```indexOf``` and ```lastIndexoff``` while not present in jq index and rindex will do the same.<br>
```index(string)``` finds the first match, ```rindex(string)``` finds the last.

<b> 55. How to retrieve a character at a specific index in a string in the framework</b><br>
with ```explode``` and ```implode```<br>
```explode```: creates an array with the string's codepoint number of each character.
```implode```: reverses the explode
So in the following example, we get "Cloudy White"
after explosion -> ```[67,108,111,117,100,121,32,87,104,105,116,101]``` 
select index ```7``` -> ```87```
Insert it into a single element array ```[87]```, this is because implode requires an array, hence adding ```[.]```
Finally we ```implode```, reversing ```[87]``` into -> ```W```<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/extractCharacter.png)

<b> 56. What happens if the index is out of bounds?</b><br>
Returns ```null``` if the index is out of range.

<b> 57. How to split a string into an array based on a delimiter in the framework</b><br>
We use ```split()``` method

<b> 58. What happens if the delimiter is not found in the string?</b><br>
```split()``` returns an array with the original string as the only element, if delimiter is not found.

<h2>User Roles and Administration</h2>

<b> 59. My user role is ANALYSIS. Is it okay for me to lead my project, or is it possible to have project/department-wise admin roles?</b><br>
Cometa comes with a lot of capabilities, which can be assigned to a role:<br>
![img](https://github.com/cometa-rocks/cometa_documentation/blob/main/img/rolePermissions.png)
In the screenshot you can see that "Access to Edit a department" can be given to a certain role like "Department Admin" to add or delete users.

<b> 60. How can we assign and manage project/department-wise admin roles?</b><br>
See above.

<h2>Data Driven Testing</h2>

<b> 61. Can we write data on Excel sheet(If excel used on Data driven).</b><br>
Yes, use step: Edit ```{file}``` and set ```{value}``` to ```{cell}```<br>

<b> 62. Excel sheet should be Auto-save if we manipulate data after uploading.</b><br>
Excel file is automatically saved and will contain the value set to the cell on next run.

<b> 63. How to do testing in headless mode in Co-Meta?</b><br>
Cometa already runs in headless mode. VNC is available too.

<b> 64. Does cometa feature language selection?</b><br>
Yes, Cometa's language can be changed using environment variables.

<b> 65. Debugging of code?</b><br>
No debugging in code, only with reports.<br>
See feature logs for execution details.

<b> 66. Does cometa feature any kind of reporting?</b><br>
Yes, Cometa features reporting and validations in it.

<b> 67. Does it feature a notification mechanism?</b><br>
Yes, cometa features Webhooks for integration in Messengers.

<b> 68. Issue log?</b><br>
Using cometa fetch console


