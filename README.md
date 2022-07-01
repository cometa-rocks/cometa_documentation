

<div style="vertical-align:center; width:100%;"><img alt="# cometa - Complete Meta Test Automation" src="img/logos/COMETAROCKS_LogoEslog_Y_W.png"></div>

Cometa was developed to help QA, Developers and Administrators to easily repeat testing with a no-code/low-code approach using an on-prem or cloud platform.  

Cometa stands for **co**mplete **me**ta **t**est **a**utomation. 

Meta (from the Greek μετα-, meta-, meaning "after" or "beyond") is a prefix meaning more comprehensive or transcending. [source Wikipedia](https://en.wikipedia.org/wiki/Meta). 

With Cometa you can test over system boundaries, you can go to one application, fetch data and save it in variables. Then go to another application and use the data to test against content or use it as search input ...

Cometa uses a now-code / low-code approach to define test steps and executes them using behave (in a behaviour driven way) against selenium webdriver which grabs virtual or real browsers from selenium hub. The results from the execution (timing, steps execution logs, screenshots, video) are stored in the filesystem and referenced in database. The results can be consumed via REST API or easily in your browsers with Cometa's User Interface build with Angular. 

Cometa is available on-cloud and on-prem.

Find the offical cometa.rocks homepage [here](https://cometa.rocks/)

You are looking at the Cometa Community Edition (CE) [licensed](#license) under AGPLv3. See [Cometa Versions](#cometaversions) to understand the difference from the Enterprise Edition (EE).

# Table of Contents 

- [Cometa Versions](#cometaversions)
- [Cometa History](#cometahistory)

All about testing
- [Cometa Overview - 5W1H](#cometamindmap)
- [What is a Testplan / Feature](#whatis_a_testplan)  
- [Your first test](#general) 
- [All about cometa steps](#allaboutsteps)
- [All about selectors](#selectors) 
- [Data Driven Testing](#datadriventesting) 
- [Execute](#execute-javascript)
- [Compare values](#compare-selector-values)
- [Create sub-feature](#create-sub-feature)
- [Up- and Downloading Files](#up-and-download)
- [Questions](questions.md)

All about integration
- [Integration with Webhooks](#integration) 
- [Integration with Git](#integrationgit) 
- [REST API](#restapi) 
- [Security](#security) 
- [Housekeeping](#housekeeping)

Last but not least
- [Want to help?](#wanttohelp) 
- [Need support/help?](#needhelp) 
- [Design and Logos](#design) 
- [License](#license) 

<a name="cometaversions"></a>

# Cometa Versions

Cometa comes in various flavours:

**Community Edition** 

The public github repo is at [github.com/cometa-rocks/cometa](https://github.com/cometa-rocks/cometa/). The community Edition does not include enterprise features and in general lags behind the leading enterprise repo. 

Cometa Community edition is licensed under AGPLv3. See the [license details](#license).


**Enterprise Edition**

The internal repo is on our [gitlab server](https://git.amvara.de/amvara/cometa). Please let [us know](mailto:enterpriseaccess@cometa.rocks), if you want access there. 

To use the Enterprise Edition you need an Enterprise License. The Enterprise Edition will be patched and updated continously. It integerates into our CI/CD process. It contains features like `run on kubernetes` and `execute special teststeps for commercial products like IBM Cognos, SAP, Service-Now, Hubspot, .. ` 


**Cloud Edition Freemium**

A hosted by us version is ready for you to use. You get 90 minutes per month of free usage. Execution is limited to one browser emulator  per testcase.
The freemium plan can be updated to a paid plan any time. The paid plan starts at 7€/month, which include 5€ subscription and 2€ for an extra of 60 minutes testing. The paid plans include parallel browser testing. 

**Cloud Edition Enterprise**

You don't want to bind human resources on servers setup and maintenance? We can plan, build and run your enterprise cloud version on completly separated machines on premises or on cloud.  

<a name="cometahistory"></a>

# Cometa History

Development started around 2014-2015, when Daimler AG, Germany asked for an agile process of testing financial enterprise reporting web applications. Since then cometa has come a long way. 

| Year | What was done |
| :---: | :--- |
| 2014 | First Proof-of-Concept (Poc) |
| 2016 | Starting Development of Version 0.1 of Cometa |
| 2018 | Cometa goes into Production |
| 2019 | Second PoC |
| 2020 | Development + Enhancement of pre-built steps to be more inteligent and robust |
| 2021 | Chaining of Execution via automated scheduling, development of New Landing (beta), starting promotion in Testing Communities, Cometa Rocks S.L. established to backup the further development and promotion, Inauguration of public repo on github |
| 2022 | New customers signup for Enterprise Grade testing |


<a name="cometamindmap"></a>

# Cometa Overview - 5W1H

To get a highlevel overview in mindmap format - find the "5W's" and "1H" ... [What, When, Where, Why, Who, & How about Cometa - here](https://www.xmind.net/m/U8BJXc).


<a name="whatis_a_testplan"></a>

# What is a Testplan versus Feature

A testplan or feature consists of general information, browser selection, and the steps / actions that should be executed one after the other. 

So what is the difference between a Testplan and a Feature?

When we speak of something that we want to test - what do we mean?  Do we want to test a Login or a menu functionality? Do we want to test a navigation path?
Is that a feature of our application? Or is that a testplan.

So, to get things right:

* A feature in our world is a building block. We want to test a feature (one single behaviour) on mobile and on desktop. That means: can we click on every element of menu and is the result as expected? That is a feature. We call the feature "menu"
* Several features will then be grouped into a testplan. So testing an application consists of: test menu, test upload, test searching and test backend.

So testing a whole application consists of testing many features on different devices. That is a testplan.

With Co.meta you can include anything everywhere. A Login feature maybe always necesarry and from there your test different sections of your applications.
Co.meta does not have a hierarchy. You can run anything anywhere else.

This being said, it is your part to structure your tests and working with Co.meta will help you reuse anything anywhere else. Whenever you encounter something that you did before - just include it.

Some how Co.meta is like wikipedia, anything depends, may depend or may be singular.

A common hierachy we enconter is:
```
| Call some URL (DEV/STAGE/PROD)
|-- From there do the login (but this login is used anywhere else)
   |-- On Stage test using parameters xzy
   |-- On Prod test using parameters xyz
```

So, we end up tying parameters and URLS to environments.

Is this still a feature or a testplan? It is complex, where anything depends on how you want to use it and how you structure it. Co.meta provides you the possibilities. At the end it is you, to structure everything in a way that is good for your application.

<a name="general"></a>

# Your first test 

The first Chapter provides information on steps / actions to be used in your testplan.

A good way to start is, to just [grab our example](feature_example_your_first_testcase.json) and paste it into the cometa using the ``Import Json`` button in the feature editor.


<a name="allaboutsteps"></a>

# All about Cometa steps

Cometa comes with over 70 predefined steps like "Goto {URL}", "Wait until I can see {something} on page". 

See the detailed documentation on every possible steps group by mouse-actions, keyboard actions, selector option ...  
[documentation of steps](cometa_actions.md). 

You want to see the code running below? See [actions.py](https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/actions.py)

<a name="selectors"></a>

# All about selectors 

In cometa you can use selectors. Cometa automatically tests for ID, tagname, classname, inner HTML, xpath.

Therefor in most cases you do not have to worry about seperating xpath or css selectors. Just use them and cometa will understand what you are looking for.

Q: How do I select a button? 
A: Use the step `"I move mouse to {selector} and click"`. Replace "{selector}" with a xpath selector "//button[.='Text seen on button']" or using css e.g. button:nth-of-type(1)
A: Use the step `I can click on button "{button_name}"`. Where button name translates into the text of the button or any attribut with that text.

We have put together a huge summary about selectors and differences between CSS and X-Path. [learn about selectors like CSS and xpath](css-xpath.md). 


<a name="datadriventesting"></a>

# Data Driven Testing (DDT)

Cometa can store content from selectors in variables, which then can be use in any other step ... to compare, send keys, wait for ... .

A general use case is: go to application A, read the products from selector xyz and store that into variable $foo. Goto application B and test selector zyx to contain values from $foo. 

Steps to use for this:
```
Save selector "//h3[1]" value to environment variable "SEARCHRESULTS"
Save list values in selector "{css_selector}" and save them to variable "{variable_name}"
```

Variables can then be used in any other step just like this:

```
Send keys "$SEARCHTERM"
```

Variables depend on the environment set in your feature. So you can store different variables for your DEV, INTEGRATION, STAGE and PROD environment. 


Another use case for illustration could be: Search result validation
* goto google and search for `cometa rocks`
* save the value from the first search result to variable `VARIABLE_SEARCHRESULT` (note: this is without the $-sign!!)
* goto bing and search for `$VARIABLE_SEARCHRESULT` (note: here we use the variable with the $-sign)

See this [JSON File](feature_example_your_first_testcase.json) as a starting point.

Another use case is: Order validation
* Goto application A, order a product, save the order confirmation number to variable XYZ
* Goto application Backend, select new orders list and search for order number XYZ 


<a name="execute-javascript"></a>

# Execute your own Javascript

Use the step: `Run Javascript function "{function}"`
   
Replace "{function}" with "alert('foo')" to get a first understanding. Inside the "" you can place anything you'd like and that is valid JavaScript. You do not have to care about escaping a _"_ ... cometa does that for you. 

<a name="compare-selector-values"></a>

# Compare the values of two selectors over system boundaries

You want to compare two selectors to match between System A and System B.

This steps does the magic for you:
`Test list of "{css_selector}" elements to contain "{all_or_partial}" values from list variable "{variable_names}" use prefix "{prefix}" and suffix "{suffix}"`

```
List A: Featured;Price: Low to High;Price: High to Low;Avg. Customer Review;Newest Arrivals
List B: Featured;Price> Low to High;Price> High to Low;Avg. Customer Review;Newest Arrivals
```

The ":" and ">" in the middle cannot be handled by the Prefix/Suffix from cometa.

Solution:
Use the `"Execute Java-Script"` beforehand and get the formatting right. 

* Get the value from the selector via Javascript.
* In the same function, split it and write it to the DOM.
* Use a next step in cometa to fetch your updated selector to a variable.
* And then compare.

Another Example: "Assert for a string to have a certain format, e.g. the string is longer then 5 characters"

Use `Run Javascript "{function}"` as step and assert with javascript on the format, e.g. the following code checks that the string is longer then 5 characters: `Run Javascript function "
if ( !"$MYORDERNUMBER".length>5 ) throw "Found an Error: Order Number is not greater than zero""` 

<a name="create-sub-feature"></a>

# Create a sub-features

Sub-features are cool for include repeating tasks in other steps.

So, for example let's assume you will always have to log-on to your System before testing.

Then you would create a feature "Logon System XYZ" and include this feature in all you other features using the step `"Run feature with {name or id} before continue"`

<a name="up-and-download"></a>
# Upload and Download Files

For **Uploading** use the step `Upload a file by clicking on "{selector}" using file "{filename}"`.

`selector` is the xpath, id or css selector of the input field to be used.

`filename` is the path of the upload file in the headless browsers home-directory. 

Inside the home directory of the virtual browsers there are two folders "Downloads" and "uploads". In Downloads all downloaded files from any testcase can be found in a subfolder with the feature-ID. 

Files in the uploads folder can only be provided by sys administration. The files must be copied to `<cometainstallation>/backend/behave/uploads/`. 

The following dummy files are located in the uploads folder: dummy.mp4, dummy.pdf, dummy.png, dummy.txt and dummy.xlsx 

In general Selenium is not able to use or control the upload window which normal pops up, when we click on "Upload something". 

Question: So how do we upload something, if we cannot control the window which is responsible for this? 

Answer: We select the `input field` in HTML where the file should be stored and send the upload filename via send_keys() into that item. 

Question: My input field is hidden. So I cannot select it. What now?

Answer: Make it visible with javascript by setting the correct attributes like `display:inline`.

For **Downloading** use the step `Download a file by clicking on "{linktext}"` ... downloads a file, watch which file is downloaded and assign them to feature_result and step_result, linktext can be a text, css_selector or even xpath

The downloaded file can be re-used for uploading somewhere else.


<a name="integration"></a>


# Integration with Webhooks

Integration is usefull to get feedback on test results via Webhooks. Any application supporting webhooks can be notified by co.meta at the end of a test execution either on error or always.

The integration is user and department dependent. Each user can have different notifications. If two users use the same webhook, then for each user the webhook will be executed.

<a name="integrationgit"></a>

# Integration with Gitlab / Github

To integerate cometa into you CI/CD pipeline the REST API is your friend. You can trigger anything that you would do from the UI via REST API. It is easy and straight forward.

See [`integration with gitlab`](https://github.com/cometa-rocks/cometa/blob/master/scripts/integration-with-gitlab.sh) as an example. Depending on your authentication provider and URL endpoints, you have to adapt the variables and URL endpoints in the script.

<a name="restapi"></a>

# REST API
   
Cometa REST API is Django based. See the [REST API](/REST-API.md) for details.


<a name="housekeeping"></a>

# Housekeeping

Cometa produces a lot of videos and images. Cometa does housekeeping every night and removes all images and videos from executions older than 60 days (default).

The housekeeping time frame can be set per department.

To save a cometa execution result for legal documentation reason, just select "save this run". This will mark the result as save and it disappear from the standard view. Select "view saved runs" to view your saved results.

Saved results will not be touched by the housekeeping.

<a name="security"></a>

# Security

Cometa is secured via [OIDC](https://en.wikipedia.org/wiki/OpenID). OIDC is state of the art enterprise security that connects and integrates with the  authentication provider of your choice. 

The Freemium and Cloud Version of cometa uses google-oAuth and gitlab oAuth as option to select from.

If you would like to integrate with other authentication providers, please let us know or contribute. We would be happy to accept your pull request.

<a name="wanttohelp"></a>

# You want to help with the development of cometa?

A good starting point is the documentation. When ever you see something that you would describe better or where information is just not there yet. Clone the repo, change or add whatever is needed and send us a pull request.

We will then review and update the master branch.

The cometa community thanks you for you help.

<a name="needhelp"></a>

# You are stuck and need some help?

We are here to help you. Please contact us at our email <tec_dev@cometa.rocks> or via Discord https://discord.gg/e3uBKHhKW5  

<a name="design"></a>

# Design

You may use the cometa.rocks logo as long as you respect the layout in any publication. Let us know of your publication, so that we can backlink to it.

## Fonts

Cometa uses Comfortaa as primary font and Montserrat as secondary.

## Color

Orange: #f4b829
Black: #191919
## Logos

 <img style="background-color:white" src="img/logos/COMETA_Logo_Y_B.png">

 <img src="img/logos/COMETA_Logo_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETA_LogoEslog_Y_B.png">

 <img src="img/logos/COMETA_LogoEslog_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETAROCKS_Logo_Y_B.png">

 <img src="img/logos/COMETAROCKS_Logo_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETAROCKS_LogoEslog_Y_B.png">

 <img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png">

<a name="license"></a>

# License
   
Cometa.Rocks is licensed under AGPLv3 - see details in `LICENSE`(https://github.com/cometa-rocks/cometa_documentation/blob/main/LICENSE)
