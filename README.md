# SeniorVu Front End Exercise

# Your Mission

Hello Developer! For this exercise we'd like you to carve out 2 hours and create a single page app
(SPA) using the [SeniorVu SDK](https://github.com/SeniorVu/seniorvu-sdk) and the front-end framework of your choice.

> Hey this is important! We hope you can spend about two hours on this project. If you can finish faster -- great!
> If not, limit yourself and don't spend much longer than 2 hours MAX. Explain any extra work you would do in a
> SOLUTION.md file.

# Your Tasks

* Make a fork of this repo (if you don't have a github account you'll have to create one).
* The home page of your app should show a list senior living communities from our API, using the SDK.
  You decide how you want to order the communities and how they are displayed.
* Be creative with this. We want to see a functional site that uses the SDK. When in doubt, make an executive decision.
  Functionality is more important than the look and feel. If you finish early, feel free to polish it up.
* A user should be able to click on a community in the list. When a community is clicked, the page shows some details about the community (name, address, company name, etc).
* Once finished, send link to your github repo fork to the SeniorVu representative you've been in contact with.

# Overview

* This repo contains a basic [Vue 2](https://vuejs.org/) app as a starting point. To see it, do:
  * `npm install`
  * `npm run serve`
  * Open http://localhost:8080/ in your browser (or whatever url the dev server spits out)
* If you feel more comfortable with another framework (React, Angular, etc) feel free to scrap our skeleton and roll
  your own. We know starting from scratch will take longer so just do what you can functionality-wise in 2 hours.

# Some Tips

* Assume you only need to support latest Chrome on desktop.
* Check the output from the SDK's API request and choose what data you think is pertinent for a list of senior living
  communities.
* We want to see you demonstrate competence with a JavaScript framework. If you like something other than the big 3
  that's great. VanillaJS is great too, but not for this project.

# Using the SDK

* The SDK is a very simple wrapper around our API. It uses method chaining to build a request path, and then a verb method
  executes it, returning as promise; i.e. `seniorvu.communities(123).get()` runs `GET /api/communities/123`
* You will not need an API key to access the public communities endpoint.
* Results from the API are paginated. You can use `limit` and `offset` to control output, if you want
  (`seniorvu.communities().get({ offset: 10, limit: 10 })`)
* See https://api.seniorvu.com/docs/api/#!/Communities/get_api_communities for more details on the communities endpoint.
* Fetching communities in ES6 can be done like so:

```js
const SeniorVu = require('seniorvu-sdk').default;
const seniorvu = new SeniorVu();
const communities = await seniorvu.communities().get();
```