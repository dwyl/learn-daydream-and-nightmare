<!-- # Learn Daydream & Nightmare -->

Just when you thought the internet couldn't get any _more_ awesome,
you discover that you've got "***web super powers***"!!

## _Why_?

Testing a web page/site/app to _confirm_ that it is working as _expected_
_used_ to be difficult and _slow_.
So most web developers/designers did not bother with _automated_ testing.
Instead _most_ people do (_manual_) "click though" or "visual regression" testing.
It turns out us [humans can literally be blind](https://en.wikipedia.org/wiki/Change_blindness) to spotting changes during manual testing.

Other uses? [Automated testing can help with web scraping too...](https://hackernoon.com/nightmarishly-good-scraping-with-nightmare-js-and-async-await-b7b20a38438f)

## _What_?

This guide is _an introduction to_ "***web super powers***"
_for **complete beginners**_.<br />
_Unusually_ for a [dwyl "learn" tutorial](https://github.com/search?q=org%3Adwyl+learn)
we will be focussing on learning **_two_ tools**
in the next **20-30 minutes**. <br />
(_We usually try and learn/teach **one** thing at a time,
  but in this case the tools go together like electricity :zap: and a **lightbulb**_:bulb:!)

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

_Awkwardly_, Google recently decided
to call their Virtual Reality (VR project "_Daydream_" ...
see [google.com/**daydream**](https://vr.google.com/daydream)),
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
to help _anyone_ [learn "Test Driven Development" (TDD)](https://github.com/dwyl/learn-tdd).

### What about _Automated_ Testing?

**Automated** testing refers to testing automated user interactions. Daydream and Nightmare automate the usual clicks and behaviours that a human would perform, so you don't have to!

## _How_?

The _reason_ we have organized the tutorial with Daydream _first_
is that you don't _need_ to know Nightmare.js to use Daydream,
and it can be used by people without "coding" experience.

### Daydream walkthrough

**This tutorial assumes that you have node installed and [Nightmare installed](https://github.com/segmentio/nightmare) as a dependency**

#### Add Daydream to Chrome

- To begin [**add Daydream to your Chrome extensions**](https://chrome.google.com/webstore/detail/daydream/oajnmbophdhdobfpalhkfgahchpcoali). You should now have a camera icon in the top right corner of your browser.

![image](https://cloud.githubusercontent.com/assets/16775804/24111767/6f6f2512-0d8f-11e7-93db-c6976bfb8d9e.png)

#### Let's get started

- **Pick a user journey that you want to test.** Start small. We'll start with the following journey:

  **From this README > click the giphy link in the tutorial description at the top > arrive at a gif with the hashtag 'nightmare'**

  This is what it will look like:

  ![demo](https://cloud.githubusercontent.com/assets/16775804/24203856/be1985e2-0f0e-11e7-8ff3-ab62df8f8cc9.gif)

- Before starting the recording make sure your browser is on the page you wish to start on. In our case it's this README.

- To start the test click the camera symbol. It will turn green to show it is recording.

![image](https://cloud.githubusercontent.com/assets/16775804/24113367/7df1feca-0d94-11e7-99f4-26775eb9f2ee.png)

- The first action you need the script to record is the url of the page you are on. To do this refresh your page (it will appear as `.goto(www....)` in your finished script).

- Next navigate as you normally would, following the path that you want the test to take. So for this test you would click on the giphy link in the tutorial description.

![image](https://cloud.githubusercontent.com/assets/16775804/24113044/57cb6eb2-0d93-11e7-8973-bc82cfbe7519.png)

- This test is only a short one and so having clicked on the giphy link and having arrived on the giphy #nightmare page we are ready to end the recording.
To do this, stop the recording by clicking on the green camera symbol. It will turn black to show recording has ended. You will see a blue notification which indicates that you've recorded a script:

<div style="text-align:center"><img src ="https://cloud.githubusercontent.com/assets/16775804/24113514/f279fdf6-0d94-11e7-82d9-2d55e40c8405.png" /></div>

- Click this to see the recorded script (the bit of code you'll need to use in your project for the test). Copy and paste this code into a new file in your project.

### Turning the Daydream script into a Nightmare test

Daydream does the hard work of recording our actions into a Nightmare test. However, we still need to add to the code it gives us for our test to work. Let's understand what Daydream has done for us:

**1.** Set up your code to run Nightmare tests

**2.** Written the code that tracks the user's journey throughout the code (ie. going to a given url, clicking on a button)

<div style="text-align:center"><img src ="https://cloud.githubusercontent.com/assets/16775804/24255398/4d9567a8-0fdd-11e7-9888-0d33f330adf0.png" height="300px"/></div>

If you're non-technical try making sense of the commands in part **2** (on the screenshot). They represent common user actions such as clicking on a page or taking a screenshot. The text within the parentheses indicates what these commands apply to ie. what html/css element is being clicked on.

**Time to amend part 3**

Now that you have your test set up and the journey you want it follow, you need to add what it is you're going to test this journey against. In other words, how can the computer be sure that the page it's landed on is the right one? What parts of the page do you want to make sure look the way they should? Let's use our example to flesh this out.

Daydream provides some basics here as shown in part **3**. It's handling errors for you and is going to print the `result`. However before it can print `result` you need to define what `result` is. This is done using the `.evaluate` method which comes before `.end`.

**Here's the evaluate method for our giphy example:**

![image](https://cloud.githubusercontent.com/assets/16775804/24258286/29b7140a-0fe5-11e7-846c-3fcd91c31373.png)

**`.evaluate` takes a function**, whatever this function returns is then channeled into `.then` as your `result`. In our example the `.evaluate` method returns the url of the page that the test ends on. We're expecting `result` to be the giphy url. At the moment the `.then` method is simply going to log what `.evaluate` returns. To make our tests more user friendly we can change this to show whether our test result should be a pass or fail, like so:

![image](https://cloud.githubusercontent.com/assets/16775804/24258634/4bba47a6-0fe6-11e7-8229-80ec0e8934b6.png)

Now our `.then` function receives the url that the test ended on (`result`). It checks if `result` matches the giphy url we expected. If the two match it will log that the test has passed :white_check_mark:. If the two do not match then it will log that the test has failed :x: as well as the expected and recieved urls.

**The test is ready, let's run it and see what happens!** :sparkles:

To run the test type `node ` followed by the file path into the command line and press enter. You should get:

![image](https://cloud.githubusercontent.com/assets/16775804/24258959/35096c7a-0fe7-11e7-92a3-c659dcc64846.png)

:star2: **Congratulations, you've successfully created your first automated test!** :star2:

### Commands to add

- screenshot (and viewing screenshots)
- click
- go to
- Ways to get info from the dom ie. html/css elements
- Change Daydream script screenshot to include screenshot

### How to Disable a Chrome Extension when Not In Use

+ In your Chrome Browser, visit: chrome://extensions/
