---
layout: post
title: "iOS5 Doesn't Support bind()!?"
tags: javascript mobile
published: true
date: 2012-08-20 21:30
---

Yup.   

After hours of frustration trying to figure out what possibly went wrong, it turns
out that iOS5's version of Safari does not support 
[bind()](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Function/bind#Browser_compatibility).

This crucial part of the EcmaScript 5 standard. What a shame. I totally thought
I could use this feature in all modern browsers.   

According to [this guy's table](http://davidbcalhoun.com/2011/new-mobile-safari-stuff-in-ios5-position-fixed-overflow-scroll-new-input-type-support-web-workers-ecmascript-5)
it's the *only* ES5 feature that mobile safari doesn't support.

Figuring out this bug was no small feat considering the lack of dev tools for iOS safari.
