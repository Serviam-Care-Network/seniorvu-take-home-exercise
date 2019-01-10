# SeniorVu Front End Project

# Your Mission

Hey Developer. Welcome! Your mission, should you choose to accept it, is to carve out 2 hours and create a single page app
(SPA) using the [SeniorVu SDK](https://github.com/softvu/seniorvu-sdk).

> Hey this is important! We hope you can spend about two hours on this project. If you can finish faster -- great!
> If not, limit yourself and don't spend much longer than 2 hours MAX. Explain any extra work you would do when you send
> us your result.

# Your Tasks

* Be creative with this. We want to see a functional site that uses the sdk. When in doubt, make an executive decision.
  Functionality is more important than the look and feel. If you finish early, feel free to polish it up.
* The home page of your app shows a list communities. You decide how you want to order the communities and how they are displayed.
* A user should be able to click on a comomunity in the list. When a community is clicked, the page shows details about the community.
* Once finished, send your solution files or a link to a github repo to brian.hann@seniorvu.com

# Some Tips

* We've provided a lot of code for you to get up and running fast. We encourage you to use it if you think it will help but feel free to roll your own.
* We use Vue internally but if you're more comfortable with another framework (Angular, React, etc) go ahead and use that.
* Assume you only need to support Chrome.

# Using the SDK

You will not need an API key to access the public communities endpoint. Fetching communities in ES6 can be done like so:

```js
const SeniorVu = require('seniorvu-sdk');
const seniorvu = new SeniorVu();
const communities = await seniorvu.communities().get();
```