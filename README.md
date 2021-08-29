# cometa - Complete Meta Test Automation

Co.meta stands for **co**mplete **me**ta **t**est **a**utomation. 

Meta (from the Greek μετα-, meta-, meaning "after" or "beyond") is a prefix meaning more comprehensive or transcending. [source Wikipedia](https://en.wikipedia.org/wiki/Meta). 

With Co.meta you can test over system boundaries, you can go to one application, fetch data and save it in variables. Then go to another application and use the data to test against content or use it as search input ...

Co.meta uses a now-code / low-code approach to define test steps. 





## Table of Contents 

- [What is a Testplan / Feature](#whatis_a_testplan)  
- [Your first test](#general) 
- [All about selectors](#selectors) 
- [Integration](#integration) 
- [Data Driven Testing](#datadriventesting) 
- [Want to help?](#wanttohelp) 


<a name="whatis_a_testplan"></a>

## What is a Testplan versus Feature

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

## Your first test 

The first Chapter provides information on steps / actions to be used in your testplan.

A good way to start is, to just [grab our example](feature_example_your_first_testcase.json) and paste it into the cometa using the ``Import Json`` button in the feature editor.


<a name="selectors"></a>

## All about selectors 

In cometa you can use selectors. Cometa automatically tests for ID, tagname, classname, inner HTML, xpath.

Therefor in most cases you do not have to worry about seperating xpath or css selectors. Just use them and cometa will understand what you are looking for.

We have put together a huge summary about selectors and differences between CSS and X-Path. [learn about selectors like CSS and xpath](css-xpath.md). 

<a name="integration"></a>

## Integration with Webhooks

Integration is usefull to get feedback on test results via Webhooks. Any application supporting webhooks can be notified by co.meta at the end of a test execution either on error or always.

The integration is user and department dependent. Each user can have different notifications. If two users use the same webhook, then for each user the webhook will be executed.

<a name="datadriventesting"></a>

## Data Driven Testing (DDT)

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


<a name="wanttohelp"></a>

## You want to help with the development of cometa?

A good starting point is the documentation. When ever you see something that you would describe better or where information is just not there yet. Clone the repo, change or add whatever is needed and send us a pull request.

We will then review and update the master branch.

The cometa community thanks you for you help.

