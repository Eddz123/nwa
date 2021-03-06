# Node Web Application - Template!

[![Build Status](https://travis-ci.org/bradgarropy/nwa.svg)](https://travis-ci.org/bradgarropy/nwa)
[![NSP Status](https://nodesecurity.io/orgs/brad-garropy/projects/27126b8e-87c8-46a5-bf73-80ea79993e3b/badge)](https://nodesecurity.io/orgs/brad-garropy/projects/27126b8e-87c8-46a5-bf73-80ea79993e3b)

![NWA](https://raw.githubusercontent.com/bradgarropy/nwa/dev/nwa.png)

*This template is a continuation of the [node-only-server](https://github.com/bradgarropy/node-only-server) I created. The goal was to extend that learning experience into an actual template I could use to produce web applications faster. Hope you like it!*

When I set out to build this template, I wanted to mimic a real application environment as much as possible. To that end, I've created a continuous integration workflow for this app using [Travis CI](https://travis-ci.org/) and [Heroku](https://dashboard.heroku.com/). The strategy was to have two branches, [master](https://github.com/bradgarropy/nwa/tree/master) and [dev](https://github.com/bradgarropy/nwa/tree/dev), which are both automatically built and deployed to [Heroku](https://dashboard.heroku.com/) anytime changes are pushed.


## Continuous Integration

Continuous integration is done by linking [Travis CI](https://travis-ci.org/) with this GitHub repository. You can see [here](https://travis-ci.org/bradgarropy/nwa/branches) that I'm building both branches anytime change is committed. My build process is very simple, just run [jshint](http://jshint.com/) and [nsp](https://nodesecurity.io/) to check for basic syntax and security issues.


## Deployment

I decided to go with [Heroku](https://dashboard.heroku.com/) for my cloud hosting platform, as it is **completely free** and offers integration with  [GitHub](https://github.com/) and [Travis CI](https://travis-ci.org/). I configured a "pipeline", which tracks my [master](https://github.com/bradgarropy/nwa/tree/master) and [dev](https://github.com/bradgarropy/nwa/tree/dev) builds, and deploys them if the build succeeds. You can find both environments up and running here:

* [nwa-production](https://nwa-production.herokuapp.com/)
* [nwa-staging](https://nwa-staging.herokuapp.com/)

Each application has its own URL, and I took advantage of the NODE_ENV variable to place a development banner in the staging application.


## Sooo What Is It?

This web application integrates multiple technologies to deliver a base set of features required of a web server.


### Technologies

* [Express](https://expressjs.com/) web server
* [MongoDB](https://www.mongodb.com/) database
    * Hosted by [mLab](https://mlab.com/)
    * Using [mongoose](http://mongoosejs.com/) ODM
* [pug](https://pugjs.org/api/getting-started.html) HTML templates
* [Bootstrap](http://getbootstrap.com/) styles
* [Passport](http://passportjs.org/) authentication


### Features

* User Management
    * Database Schema
    * Registration
    * Login
    * Logout
    * Profile Update
    * Password Change
    * Password Reset
* Flash Messages
    * Success
    * Info
    * Warning
    * Error
    * Danger
* Secure
    * Loads secrets from .env file
    * Uses secure HTTP headers


## Usage

First, clone the repository.

```
git clone https://github.com/bradgarropy/nwa.git
```

Next, install the dependencies.

```
npm install
```

Then, start the web server.

```
npm start
```

Finally, navigate to the site.

```
localhost:3000
```
