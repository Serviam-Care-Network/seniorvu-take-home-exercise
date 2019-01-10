# SeniorVu Front End Project

# Your Mission

Hey Developer. Welcome! Your mission, should you choose to accept it, is to carve out 2 hours and create a single page app
(SPA) using the [SeniorVu SDK](https://github.com/softvu/seniorvu-sdk).

> Hey this is important! We hope you can spend about two hours on this project. If you can finish faster -- great!
> If not, limit yourself and don't spend much longer than 2 hours MAX. Explain any extra work you would do in a
> SOLUTION.md file.

# Your Tasks

* The home page of your app shows a list communities from our api, using the SDK. You decide how you want to order the communities and how they are displayed.
* Be creative with this. We want to see a functional site that uses the sdk. When in doubt, make an executive decision.
  Functionality is more important than the look and feel. If you finish early, feel free to polish it up.
* A user should be able to click on a community in the list. When a community is clicked, the page shows details about the community.
* Once finished, send your solution files or a link to a github repo to brian.hann@seniorvu.com

# Overview

* This repo contains a basic Vue 2 app as a starting point. To see it, do:
  1. `npm install`
  2. `npm run serve`
  3. Open http://localhost:8080/ in your browser (or whatever url the dev server spits out)
* If you feel more comfortable with another framework (React, Angular, etc) feel free to scrap our skeleton and roll
  your own.

# Some Tips

* Assume you only need to support desktop users on Chrome.
* Check the output from the API request and choose what data you think is pertinent for a list of senior living
  communities.
* We want to see you demonstrate competence with a JavaScript framework. If you like something other than the big 3
  that's great. VanillaJS is great too, but not for this project.

# Using the SDK

* The SDK is a very simply wrapper around our API. It uses method chaining to build a request path, and then a verb method
  executes it, returning as promise; i.e. `seniorvu.communities(123).get()` runs `GET /api/communities/123`
* You will not need an API key to access the public communities endpoint. Fetching communities in ES6 can be done like so:

```js
const SeniorVu = require('seniorvu-sdk');
const seniorvu = new SeniorVu();
const communities = await seniorvu.communities().get();
```