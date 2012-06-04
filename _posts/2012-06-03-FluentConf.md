---
layout: post
title: "O'Reilly FluentConf"
tags: javascript conferences
published: true
date: 2012-06-03 20:00
---

Last week I attended O'Reilly Media's first ever
[FluentConf](http://fluentconf.com/fluent2012) JavaScript conference.
There were a lot of interesting speakers and topics and at times it was hard
to decide which talk to attend. I didn't feel like I learned any new
*mind-blowing* things, but overall it was a good conference and there were some
good bits of info that I left with. Some common themes seemed to be **Mobile**,
**3rd Party Scripts**, **HTML5 Games**, and **NodeJS**.
I won't give an exhaustive account of what occurred, instead here's a giant
brain dump of all the good take-aways and things to research further:


### Performance

- Use the cool
  [Navigation Timing api](https://developer.mozilla.org/en/Navigation_timing)
  for useful client-side perf metrics.

- Always load 3rd party scripts async to prevent
  [Front-End Single Points of Failure](http://www.youtube.com/watch?v=aHDNmTpqi7w)


### Tools

- Fly around your directories with ease using an awesome shell script called
  [z](https://github.com/rupa/z)

- When you need to test page loads (and don't need a beautiful UI while doing it)
  [webpagetest.org](http://www.webpagetest.org)

- A database of various web performance information for the Internet's top
  websites [httparchive.org](http://httparchive.org)

- A black-hole site for testing scripts/pages that timeout
  [blackhole.webpagetest.org](http://blackhole.webpagetest.org)

- [Paul Irish](http://paulirish.com) has a nice site for checking HMTL5
  compatibility: [html5please.com](http://html5please.com)

- [PhantomJS](http://phantomjs.org) is a headless webkit for testing JavaScript

- Quickly share your localhost website with
  [bunyip](http://bunyip.pagekite.me/)



### Some cool JavaScript stuff I didn't know about

- [Array Buffers](http://www.khronos.org/registry/typedarray/specs/latest/)
  and
  [Typed Arrays](https://developer.mozilla.org/en/JavaScript_typed_arrays)

- [Low Level JavaScript](http://mbebenita.github.com/LLJS/)

- An [interesting technique](http://www.stevesouders.com/blog/2012/05/22/self-updating-scripts/)
  for 3rd party script developers to self-update their scripts while keeping far future cache expiry

- [Brendan Eich mentioned](http://brendaneich.com/2011/09/capitoljs-rivertrail/)
  that Intel has a
  [research project called River Trail](http://brendaneich.com/2011/09/capitoljs-rivertrail/)
  which is a technology for utilizing multicore and ultimately GPU parallel
  processing power for JavaScript without shared memory.

- `document.elementFromPoint()` Holy shit! Never heard of this

### Libraries

- [AlmondJS](https://github.com/jrburke/almond)
  Fast AMD loading for compiled code

- [Sound Manager](http://www.schillmania.com/projects/soundmanager2/)
  A Library for sound that [SoundCloud](http://www.soundcloud.com) uses.

- [brunch](http://brunch.io) is a
  *"lightweight approach to building HTML5 applications"* that might be
  interesting to play with

- [easyxdm](http://easyxdm.net/wp/) is a library for doing cross domain xhr
  *(what's that about flash!?)*

- [Ender.js](http://ender.no.de) like NPM but for the front-end

- [Thorax.js](http://walmartlabs.github.com/thorax) is
  *"an opinionated Backbone application framework"*

### Mobile

- [mobilehtml5.org](http://mobilehtml5.org)
  A comprehensive List of HTML5 compatibility on mobile devices

- [iWebInspector.com](http://www.iwebinspector.com)
  A web inspector tool for mobile Safari

- [Adobe Shadow](http://labs.adobe.com/technologies/shadow/)
  Cool app to link pc browser to mobile browsers for testing

- Always specify *device-width* to avoid really small rendered content on mobile
  devices   
  `<meta name="viewport" content="width=device-wdith">`

- A [bookmarklet](http://stevesouders.com/mobileperf/mobileperfbkm.php) by
  [Steve Souders](http://stevesouders.com) for debugging mobile web apps

- [cubiq](http://cubiq.org/add-to-home-screen)
  A cool library that lets users add to home-screen easily

- The [HTML Input capture](http://www.w3.org/TR/html-media-capture) attribute
  looks pretty rad



### Random Bits

- [Backbone.js](http://backbonejs.org) has no concept of application level
  events. Therefore using a pub/sub framework like
  [amplify.js](http://amplifyjs.com/api/pubsub/) might be good if you need such
  events.

- In [Backbone.js](http://backbonejs.org) declarative event listeners get
  wrapped so they can be hard to unit test.

- The [SoundCloud](http://www.soundcloud.com) guys are doing some cool things
  with
  [nested Backbone Views](http://spadgos.github.com/sfjs-next-soundcloud/#/step-22)

- If using Uglify.js you can add a bunch of debug logging statements like these
  that will get completely removed by the compiler   
  `
  if (__DEBUG_WARNINGS__) {
    console.log('uh oh, shit is broken');
  }
  `

- Twitter Bootstrap uses a pretty cool declarative
  [data-api](https://github.com/twitter/bootstrap/tree/master/js#data-attribute-api)
  for all their JS plugins (which can optionally be disabled)

- [Web Components](http://dvcs.w3.org/hg/webcomponents/raw-file/tip/explainer/index.html)
  and [Shadow DOM](http://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/shadow/index.html)
  are the future!

- [dotfiles.github.com](http://dotfiles.github.com/) Is a great place to
  get started if you don't already host your dotfiles on github

- `npm install --save ...` will save the installed package as a dependency in
  your package.json

- When deploying node apps to production use
  [upstart](http://upstart.ubuntu.com) and
  [node cluster](http://nodejs.org/docs/latest/api/cluster.html)


### Also check out
- [The official videos here](http://www.youtube.com/view_play_list?p=PL75AC4484E6866741)

- [All the speakers' slides here](http://fluentconf.com/slides)

