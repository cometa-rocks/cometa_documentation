# Documentation

This is the starting point of Co.meta documentation. 

Co.meta stands for **co**mplete **me**ta **t**est **a**utomation. Meta (from the Greek μετα-, meta-, meaning "after" or "beyond") is a prefix meaning more comprehensive or transcending. [source Wikipedia](https://en.wikipedia.org/wiki/Meta). With Co.meta you can test over systemboundaries, you can go to one application, fetch data and save it in variables. Then go to another application and use the data to test against content or use it as search input ...

Co.meta uses a now-code / low-code approach to define test steps. 

## What is a Testplan / Feature

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


## General Section 

The first Chapter provides information on steps / actions to be used in your testplan.

It is a veery good starting point to [learn about selectors like CSS and xpath](css-xpath.md). 

We will commit documentation as soon as possible. Come back soon. Watch the repo to be notified as soon as we are done.
