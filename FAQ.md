<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETA_Logo_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETA_Logo_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>


<h1>😊 FAQ & Common Question</h1>

  <h2>🚀 General Framework & Cool Functionalities</h2>

  <b>Q: Want random IDs, names, emails, or digits magically popping up in your framework?</b></br>
  A: Easy! Just sprinkle a few characters, toss them into a variable, and voilà—randomness served fresh! 🍕✨
  
![img](img/var_button_cometa.png)

  <b>Q: Can I keep my precious XPath safe and cozy in local variables, feature by feature?    </b></br>
   A: Absolutely! You already spotted that shiny little button—just click and save your XPath treasures! 🎯✨  

 <b>Q: Can I stuff all my app's favorite XPaths into one global variable basket?    </b></br>
   A: Go wild! Just set up a cozy little "department" everyone knows (think: DEFAULT or PUBLIC)—then watch your XPaths happily shared among teammates like fresh office donuts! 🍩🌍  


<b>Q: Can I put all my handy methods into one global feature file and call them anytime, anywhere?    </b></br>
   A: Absolutely! Just keep it tidy—Cometa's smart enough to catch sneaky endless loops like "F1 calls F2, F2 calls F3, F3 calls... uh-oh... back to F1" and will gently tell you, "Nope, can't save that!" 🔄🚫  


<b>Q: Got tons of smoke and regression tests files in a folder—how do I run only those quick-and-easy smoke tests?    </b></br>
   A: Easy-peasy! Watch this short clip (around 5:00) 👉 <a href="https://www.youtube.com/watch?v=So_I8CjoRPI">YouTube magic link</a> and you're good to go! 🎬✨


<b>Q: Can I add my own secret sauce—custom logic—to spice up the framework?    </b></br>
   A: Heck yes! There's even a special step just for your JavaScript magic:     </b></br>
  ✨ Run Javascript function "{function}" ✨    </b></br>
  Want more control? Sprinkle your custom Python steps right <a href="https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/actions.py">here</a>. And if you're feeling fancy, see how IBM Cognos has its own special group of steps right <a href="https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/tools/cognos.py">here</a>. 🎩🐍⚡

 <b>Q: Can I jump straight to any dependent feature files in one click?    </b></br>
   A: Almost there—but hold your horses! 🐎 This one's still baking in the oven. (Stay tuned: implementation coming soon!) 🍪✨  


<b>Q: How can I auto-run ALL my test features with a CI/CD pipeline like Jenkins or GitLab after deployment?    </b></br>
   A: Piece of cake! 🍰 Cometa gives you a tasty REST API—so if you can click it on the frontend (like that handy "..." button to run all tests in a folder), your pipeline can magically do it too. CI/CD for the win! 🚀✨  

![img](img/runAllFeatures.png)

  <b>Q: How do I run smoke and regression tests feature by feature?  </b></br>
  A: Simple! Check out this video around 5:00 and get the step-by-step magic 💥: <a href="https://www.youtube.com/watch?v=So_I8CjoRPI">YouTube link</a>. You'll be running tests like a pro in no time! 🎬🎯


<b> 10. How to integrate scripts into a CI/CD pipeline? For example, if a new build is deployed on a testing server, how will it trigger the script and email the report to the required recipient</b><br>

<h2>Database Testing</h2>

<b>Q: How do I perform database testing?  </b></br>
   A: Watch the Database Testing video! 🎬 <a href="https://youtu.be/uGRXoUh3aFA">Click here for a full walkthrough!</a>  

<b>Q: How do I connect to our database server using the framework?  </b></br>
   A: Check out the magic happening in the Database Testing video 🎥: <a href="https://youtu.be/uGRXoUh3aFA">Watch here for all the details!</a>  

<b>Q: How do I read, write, update, and delete data with the framework?  </b></br>
   A: You guessed it—the Database Testing video has you covered! Head over to this <a href="https://youtu.be/uGRXoUh3aFA">link</a> and follow along. 📹✨  

<b>Q: How do I retrieve data from the database?  </b></br>
   A: Easy! You can assert the results using JQ. 🔍 Get all the details from the video right here: <a href="https://youtu.be/uGRXoUh3aFA">Database Testing</a>.  



<h2>Mobile and Performance Testing</h2>

<b> Mobile testing feature showcase: "mobile video here"</b><br>

<b>Q: How do I perform performance testing (load, stress) using the framework?  </b></br>
   A: Want to test the limits? The Load Testing video shows you how to crush it! 💪 Check it out here: <a href="https://youtu.be/hWAyx6iBbU4">Load Testing</a>.</p>

<b>Q: How do I do non-functional testing, like load or stress?  </b></br>
   A: Non-functional testing? Covered! Watch the Load Testing video for all the juicy details: <a href="https://youtu.be/hWAyx6iBbU4">Click here</a>. 🚀</p>

<h2>Cloud Execution</h2>

<b>Q: Can I run my code somewhere cozy up in the cloud? ☁️  </b></br>
   A: Absolutely! Cometa loves clouds—use it as SaaS or install it yourself on-premises or in the cloud. Better yet, the friendly Cometa Team will gladly set it up and maintain it wherever your heart desires. And if you need to share features between installations, it's just a quick copy-and-import (without transporting variables). Cloud-nine coding, here we come! 🚀🌤️</p>



 <h2>String Methods in the Framework</h2>

<b>Q: How do I handle all my string magic in the framework? 🔮  </b></br>
   A: Cometa’s got your back—JQ is your go-to wizard for strings and JSON object manipulations. Need a quick spellbook? Check out <a href="https://jqlang.org/manual/">the official JQ manual</a> for guidance and examples. Let the string wizardry begin! 🚀</p>

<details>
  <summary><h3>Cometa test in json format used in the following questions</h3></summary>
  [{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Make an API call with \"GET\" to \"https://api.restful-api.dev/objects\"","step_action":"Make an API call with \"{method}\" to \"{endpoint}\" with \"params:{parameters}\" and \"headers:{headers}\" and \"body:{body}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares 2 objects ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data == {\"color\":\"Cloudy White\", \"capacity\":\"128 GB\"}\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares 2 strings ignoring case of input ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | ascii_downcase == \"cloudy white\"\" to \"match\" \"true\"","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks length  ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | length == 12\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks if input contains Indicated Letter ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | index(\"C\") != null\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step tests matching number -> cast to string to regex ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[3].data.price | tostring |test(\"^[0-9]+\\\\.[0-9]+$\") == true\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step replaces substring with another substring ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | gsub(\"White\" ; \"Blue\") == \"Cloudy Blue\"\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step extracts a portion of a string using indexes ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | .[2:8] == \"oudy W\"\" to \"match\" \"true\" ","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step compares two strings lexicographically replace with '==', '>' and '<' ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color > .response.content.[0].data.capacity\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"################ This step checks for a specific character in a specific index ################","step_action":"","step_type":"normal","continue_on_failure":false,"timeout":60},{"enabled":true,"screenshot":false,"step_keyword":"Given","compare":false,"step_content":"Assert last API Call property \".response.content.[0].data.color | explode | .[7] | [.] | implode == \"W\"\" to \"match\" \"true\"","step_action":"Assert last API Call property \"{jq_pattern}\" to \"{condition}\" \"{value}\"","step_type":"normal","continue_on_failure":false,"timeout":60}]
</details><br>

<b>Q: How to check if two strings match exactly?  </b></br>
   A: Easy! Use Cometa’s Assert last API call with JQ. Just like checking if "banana" equals "banana". Simple and sweet! 🍌</p>
   In this example we compare the color of an object and check if the output is true
:
![img](img/stringCompare.png)
<br>


<b>Q: What's the difference between equals and == for strings?  </b></br>
   A: In JQ-land, == is your best (and only) friend—no equals() here. Works perfectly for strings and JSON objects alike!</p>

![img](img/stringAndObjectComparison.png)


<b>Q: Compare strings ignoring case?  </b></br>
   A: Add ascii_downcase. E.g., ```"Cloudy White" | ascii_downcase == "cloudy white"```—case closed! 😎</p>

For example:
<br>
 ``` 'response.content.[0].data.color | ascii_downcase == "cloudy white"' ``` 
<br>
![img](img/caseInsensitive.png)


 <b>Q: Can equalsIgnoreCase handle special characters?  </b></br>
   A: No direct equalsIgnoreCase in JQ, and ascii_downcase only affects ASCII letters (e.g., "Hello@//" → "hello@//"). Special characters need extra care (pre-processing recommended)!</p>
 

  <b>Q: Check if a string contains a substring?  </b></br>
   A: Use index(&lt;substring&gt;). Returns position if found, or null.<br>
  Example: ```"Cloudy" | index("C") != null``` → true. ✔️</p>


  <b>Q: What if contains doesn't find anything?  </b></br>
   A: Returns null.</p>

  <b>Q: Verify a string starts with a prefix?  </b></br>
   A: ```"Cloudy" | index("C") == 0``` means "C" is at the start. 🎯</p>


<b>Q: What if the prefix is longer than the string itself?  </b></br>
   A: Returns null.</p>

  <b>Q: Check if a string ends with a suffix?  </b></br>
   A: ```endswith("suffix")``` → returns true or false. Easy peasy!</p>


 <b>Q: Can you use ```endsWith``` with an empty string?  </b></br>
   A: Sure! An empty string always returns true.</p>


 <b>Q: Verify if a string is empty?  </b></br>
   A: ```"string" | length == 0```. If length is zero, voilà—empty! 🕳️</p>

Example:
<br>
```Assert last API Call property ".response.content.[0].data.color | length == 0" to "match" "true"``` 

<b>Q: Difference between checking empty vs. null in JQ?  </b></br>
   A: No isEmpty() in JQ; simply check ```== "" or == null```. Done!</p>


<b>Q: Determine the length of a string?  </b></br>
   A: ```"yourstring" | length```. Counts characters neatly.</p>


<b>Q: Length for an empty string?  </b></br>
   A: Zero, obviously! ```"" | length == 0```</p>


<b>Q: Check a string with a regex pattern?  </b></br>
   A: Use JQ's test(). Regex magic ✨</p>
![img](img/regularExpression.png)<br>
In this example we use a regular expression to check if the input is a price number followed by a '.' followed by cents<br>
Also added ```tostring``` to parse the price as a ```string```.


 <b>Q: Validate emails or phones?  </b></br>
Example for Email:  ```^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$```
<br>
Example for Phone (Spanish format 9 digit): ```^[0-9]{9}$```

 <b>Q: Replace characters or substrings?  </b></br>
   A: ```gsub("old"; "new")```. Quick swap!</p>
![img](img/replaceString.png)



 <b>Q: What if substring not found in replace?  </b></br>
   A: String remains unchanged.</p>


<b>Q: Replace ALL occurrences?  </b></br>
   A: Again, gsub() handles all replacements gracefully.</p>


<b>Q: Difference between replace and replaceAll?  </b></br>
   A: JQ only needs ```gsub()```—it does it all!</p>


<b>Q: Convert string to lowercase?  </b></br>
   A: ```ascii_downcase```</p>


<b>Q: Does ascii_downcase change the original string?  </b></br>
   A: Nope, JQ functions are immutable—safe and sound.</p>

<b>Q: Convert to uppercase?  </b></br>
   A: ```ascii_upcase``` 🔥</p>


<b>Q: Can ascii_upcase handle non-English chars?  </b></br>
   A: Nope—ASCII chars only. Unicode? Need extra love (external handling).</p>


 <b>Q: Remove leading/trailing whitespace?  </b></br>
   A: Use ```ltrimstr()``` / ```rtrimstr()``` for leading/trailing specific strings.</p>


 <b>Q: Does trim remove spaces between words?  </b></br>
   A: Nope, only start/end of strings. Middle spaces stay cozy.</p>


  <b>Q: Extract substring (slicing)?  </b></br>
   A: ```"Cloudy" | .[2:5]``` → "oud"</p>


<b>Q: What if indexes go out of bounds?  </b></br>
   A: If over max length → empty string; negatives count from end.</p>
Example: Cloudy White<br>
```[0:9999]``` -> ```Cloudy White```<br>
```[99:9999]``` -> ```""```<br>
```[-4:11]``` -> ```hit```<br>
```[1:-4]``` -> ```loudy W```<br>

<b> 47. How to compare two strings lexicographically in the framework</b><br>
Use ```==```, ```>```, ```<``` for lexicographical comparison<br>
![img](img/lexicographicComparison.png)

<b>Q: What does a negative, zero, or positive return value from compareTo indicate?</b><br> 
  A: Trick question! jq laughs in the face of compareTo. Instead, it uses the simpler, friendlier, "I learned this in kindergarten" operators: ```<```, ```>```, and ```==```.</p>

<b>Q: How to compare two strings lexicographically while ignoring case in the framework</b><br> 
  A: Politely force both strings into lowercase submission with ascii_downcase before they argue. Peace achieved.</p>

<b>Q: What is the difference between compareTo and compareToIgnoreCase?</b><br> 
  A: Spoiler alert: one doesn't exist, and the other involves forcing strings to lower their voices.</p>

<b>Q: How to find the index of a specific character or substring in a string in the framework?</b><br> 
  A: Use ```index()``` to pinpoint exactly where your substring is hiding. Think of it as GPS for strings.</p>

<b>Q: What does ```indexOf``` return if the character or substring is not found?</b><br> 
  A: It returns null, jq’s polite way of saying, "I have no idea what you're talking about."</p>

<b>Q: How to find the last occurrence of a specific character or substring in a string in the framework?</b><br> 
  A: Use ```rindex(string)```. Like asking your friend, "Okay seriously, where'd you last see your keys?"</p>

<b>Q: What is the difference between ```indexOf``` and ```lastIndexOf```?</b><br> 
  A: While jq doesn't technically know ```indexOf``` or ```lastIndexOf```, it does have ```index()``` (the first sighting) and ```rindex()``` (the "I swear it was right here last time" sighting).</p>

<b>Q: How to retrieve a character at a specific index in a string in the framework</b><br> 
  A: You'll have to explode your string (don't panic, it's safe), grab the right character by its numeric code, then implode it again to politely reconstruct the chaos.</p>
 Example:<br> "Cloudy White" → explode → [67,108,111,117,100,121,32,87,104,105,116,101] → take index 7 (87) → wrap lovingly in [87] → implode → "W". Ta-da, you've performed string surgery!
![img](img/extractCharacter.png)

<b>Q: What happens if the index is out of bounds?</b><br>
  A: Returns ```null``` if the index is out of range.</p>

<b>Q: How to split a string into an array based on a delimiter in the framework</b><br>
 A: We use ```split()``` method.</p>

<b>Q: What happens if the delimiter is not found in the string?</b><br>
  A: ```split()``` returns an array with the original string as the only element, if delimiter is not found.</p>

<h2>User Roles and Administration</h2>

<b> 59. My user role is ANALYSIS. Is it okay for me to lead my project, or is it possible to have project/department-wise admin roles?</b><br>
Cometa comes with a lot of capabilities, which can be assigned to a role:<br>
![img](img/rolePermissions.png)
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


