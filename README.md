# targetprocess-api

[![Build Status](https://travis-ci.org/go-on-blog/targetprocess-api.svg?branch=master)](https://travis-ci.org/go-on-blog/targetprocess-api)
[![Coverage](https://codecov.io/gh/go-on-blog/targetprocess-api/branch/master/graph/badge.svg)](https://codecov.io/gh/go-on-blog/targetprocess-api)
[![Known Vulnerabilities](https://snyk.io/test/github/go-on-blog/targetprocess-api/badge.svg?targetFile=package.json)](https://snyk.io/test/github/go-on-blog/targetprocess-api?targetFile=package.json)

## Sample usage

    const factory = require("targetprocess-api");
    const tp = factory(config);

    tp.create("Projects", {Name: "My Project"})
        .then(function (entity) {
            // ...
        });

    tp.retrieve("UserStories").take(10).get()
        .then(function (items) {
            // ...
        });

    tp.update("Bugs", {Id: 3, Name: "My bug"});

    tp.remove("Releases", 12);
    
