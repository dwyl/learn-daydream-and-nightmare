<!-- # Learn Daydream & Nightmare -->

Just when you thought the internet couldn't get any _more_ awesome,
you discover that you've got "***web super powers***"!!

## _Why_?

Testing a web page/site/app to _confirm_ that it is working as _expected_
_used_ to be difficult and _slow_.
So most web developers/designers did not bother with _automated_ testing.
Instead _most_ people do (_manual_) "click though" or "visual regression" testing.
It turns out us [humans can literally be blind](https://en.wikipedia.org/wiki/Change_blindness) to spotting changes during manual testing.

## _What_?

This guide is _an introduction to_ "***web super powers***"
_for **complete beginners**_.<br />
_Unusually_ for a [dwyl "learn" tutorial](https://github.com/search?q=org%3Adwyl+learn)
we will be focussing on learning **_two_ tools**
in the next **20-30 minutes**. <br />
(_We usually try and learn/teach **one** thing at a time,
  but in this case the tools go together like electricity and a **lightbulb**_!)

### Daydream

Daydream is an _extension_ for the Google Chrome web browser that allows
you to record your actions into a script you can re-play!

+ Google Chrome Extension store: https://github.com/segmentio/daydream#google-chrome
+ GitHub: https://github.com/segmentio/daydream


### Nightmare.js

<!-- ![nightmare logo](https://cloud.githubusercontent.com/assets/194400/23049531/a0c1372a-f4b4-11e6-96a6-a38637f245a4.png) -->

Nightmare.js is a JavaScript library that
lets you automate browser interaction! <br />
Anything that a _human_ can do in a web browser can be automated by writing
a small Nightmare.js script.

+ Website: http://nightmarejs.org (_which **really** does not do it justice!_)
+ GitHub: https://github.com/segmentio/nightmare


#### Not Covered

_Awkwardly_, Google _recently_ decided
to call their Virtual Reality (VR) project "_Daydream_" ...
see: [google.com/**daydream**](https://vr.google.com/daydream),
this tutorial is ***not*** for building a "VR" app ...
but if anyone _asks_ us we will gladly write a "guide to building VR apps"!

## _Who_?

It is a "_cliché_" to say that your product/service is "_for **everyone**_"
and instead we should "_focus_" on a _specific_ "***target user***" ... <br />
So, here goes: **Daydream** is _useful_ ***only*** to people that use web browsers
and want to ***learn how to automate tasks*** <br />
so they can ***get more done in less time***.
***Everyone*** `else` should stick with their _existing_ activities. <br />
_There_, a nice _specific_ "***target user***"
for this tutorial; _better_...? :stuck_out_tongue_winking_eye:

Nightmare is _probably_ only useful to the people _making_ the web site/app
because it's more "_cody_" ... <br />
but as you will (_hopefully_) see by the end
of 30 mins of learning "***web super powers***",
the code is quite simple!


### Are You _`New`_ To Testing?

While _this_ tutorial has ***no pre-requisites***
(_other than a computer & Chrome web browser_),
we have written an _introductory_ step-by-step guide
to help _anyone_ learn "***Test Driven Development***" (**TDD**)
see: [github.com/dwyl/**learn-tdd**](https://github.com/dwyl/learn-tdd)

### What about _Automated_ Testing?

**Automated** testing refers to testing automated user interactions. Daydream and Nightmare automate the usual clicks and behaviours that a human would perform, so you don't have to!

## _How_?

The _reason_ we have organized the tutorial with Daydream _first_
is that you don't _need_ to know Nightmare.js to use Daydream,
and it can be used by people without "coding" experience.

### Daydream walkthrough

- [**Add Daydream to your Chrome extensions**](https://chrome.google.com/webstore/detail/daydream/oajnmbophdhdobfpalhkfgahchpcoali).

  You should now have a camera icon in the top right corner of your browser.

![image](https://cloud.githubusercontent.com/assets/16775804/24111767/6f6f2512-0d8f-11e7-93db-c6976bfb8d9e.png)

- **Pick a user journey that you want to test.**

  Start small. We'll start with the following journey:

  **Navigate to this tutorial > click the gif link at the top in the tutorial description > arrive at a gif with the hashtag 'nightmare'**

  This is what it will look like:

  ![demo](https://cloud.githubusercontent.com/assets/16775804/24203856/be1985e2-0f0e-11e7-8ff3-ab62df8f8cc9.gif)

- To start your test click on the camera symbol. It will turn green to show it has started.

- Start in a blank tab and navigate to your url in the browser address bar (pasting it in is easiest).

![image](https://cloud.githubusercontent.com/assets/16775804/24113367/7df1feca-0d94-11e7-99f4-26775eb9f2ee.png)

- Next navigate just as you normally would, following the path that you want the test to take. So for this test you would click on the giphy link in the tutorial description.

![image](https://cloud.githubusercontent.com/assets/16775804/24113044/57cb6eb2-0d93-11e7-8973-bc82cfbe7519.png)

- This takes you to the giphy page which is where we want to end this test. To do this, stop the recording by clicking on the green camera symbol. It will now turn black again to show that it has ceased recording. There will be a blue notification there which tells you that you've recorded a script.

![image](https://cloud.githubusercontent.com/assets/16775804/24113514/f279fdf6-0d94-11e7-82d9-2d55e40c8405.png)

- To see the script (the bit of code you'll need to use in your project for the test), click on the camera symbol. Now copy this code and paste it into a blank file in your project.

### Turning the Daydream script into a Nightmare test

Daydream does a lot of the hard work of writing a Nightmare test for us. However, we do still need to add to the code it gives us in order to write a fully functioning test. The Daydream code does the following:

1. Set up your code to run Nightmare tests
2. Write the code that tracks the user's journey throughout the code (ie. going to a given url, clicking on a button)

![image](https://cloud.githubusercontent.com/assets/16775804/24255398/4d9567a8-0fdd-11e7-9888-0d33f330adf0.png)

If you're non-technical you should be able to make sense of the commands in part 2 (on the screenshot) as they resemble common user actions such as clicking on a page or taking a screenshot. The text within the parentheses is an indication of what these commands are applying to ie. what html/css element is being clicked on.

Now that you have your test set up and the journey you want it follow, you need to add what it is you're going to test this journey against. In other words, how can the computer be sure that the page it's landed on is the right one it should have? What parts of the page do you want to make sure look the way they should? Let's use our example to flesh this out.

Daydream has already provided some basics for this next step as shown in part 3. It's handling errors for you and is going to log the result. However first you need to define what 'result' is. This is done using the `.evaluate` method which should come before `.end`.

**Here's the evaluate method for our gif example:**

![image](https://cloud.githubusercontent.com/assets/16775804/24258286/29b7140a-0fe5-11e7-846c-3fcd91c31373.png)

`.evaluate` should take a function, whatever this function returns is then channeled into `.then` as your `result`. In the example above the `.evaluate` method is checking what the url of the page is that the test ends on. In this example we're expecting the test to end on the url for the gif. At the moment the `.then` method is simply going to log what `.evaluate` returns. To make our tests more user friendly we can alter this to help us determine whether the result should make our test pass or fail, like so:

![image](https://cloud.githubusercontent.com/assets/16775804/24258634/4bba47a6-0fe6-11e7-8229-80ec0e8934b6.png)

Now our `.then` is taking the url that the test ended on (result )and is checking if it matches the url we were expecting from giphy.com. If the two match it will log that the test has passed. If the two do not match then it will log that the test has failed and tell the user what url the test was expecting and then the url that it actually received.

The test is ready, let's run it and see what happens! Type `node ` followed by the file path into the command line and press enter. This is what we get back:

![image](https://cloud.githubusercontent.com/assets/16775804/24258959/35096c7a-0fe7-11e7-92a3-c659dcc64846.png)

**We've successfully created our first automated test!**

### Commands to add

- screenshot (and viewing screenshots)
- click
- go to
- green camera bug
- Ways to get info from the dom ie. html/css elements

### How to Disable a Chrome Extension when Not In Use

+ In your Chrome Browser, visit: chrome://extensions/
