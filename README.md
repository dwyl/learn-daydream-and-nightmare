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


### Are You _`New`_ To _Automated_ Testing?

While _this_ tutorial has ***no pre-requisites***
(_other than a computer & Chrome web browser_),
we have written an _introductory_ step-by-step guide
to help _anyone_ learn (_automated_) "***Test Driven Development***" (**TDD**)
see: [github.com/dwyl/**learn-tdd**](https://github.com/dwyl/learn-tdd)


## _How_?

The _reason_ we have organized the tutorial with Daydream _first_
is that you don't _need_ to know Nightmare.js to use Daydream,
and it can be used by people without "coding" experience.

### How to use Daydream

- First of all [add Daydream to your Chrome extensions](https://chrome.google.com/webstore/detail/daydream/oajnmbophdhdobfpalhkfgahchpcoali). You'll know that it's successfully been enabled because you should now have a camera icon in the top right corner of your browser.

![image](https://cloud.githubusercontent.com/assets/16775804/24111767/6f6f2512-0d8f-11e7-93db-c6976bfb8d9e.png)

- Choose a user journey that you want to test.

Start small ie. I want to test that users using this tutorial will reach a gif with the hashtag 'nightmare' when they click on the giphy link in the description at the top of the page.

**From here:**

![image](https://cloud.githubusercontent.com/assets/16775804/24113044/57cb6eb2-0d93-11e7-8973-bc82cfbe7519.png)

**To here:**

![image](https://cloud.githubusercontent.com/assets/16775804/24113092/8c611b36-0d93-11e7-83a2-f207f6da1d41.png)

- Begin recording your actions that demonstrate your chosen user journey. To begin recording a session simply click on the camera symbol. It will turn green when it is recording.

Start by navigating to your url in the browser address bar. You may find pasting the url in is the easiest way.

![image](https://cloud.githubusercontent.com/assets/16775804/24113367/7df1feca-0d94-11e7-99f4-26775eb9f2ee.png)

- Next navigate just as you normally would, following the path that you want the test to take. So for this test you would click on the giphy link in the tutorial description.

![image](https://cloud.githubusercontent.com/assets/16775804/24113044/57cb6eb2-0d93-11e7-8973-bc82cfbe7519.png)

- This takes you to


### How to Disable a Chrome Extension when Not In Use

+ In your Chrome Browser, visit: chrome://extensions/
