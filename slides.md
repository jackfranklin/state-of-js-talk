slidenumbers: true

# The State of JavaScript

---

```js
this.setState('javascript', talk());
```

---

# Jack Franklin

# Frontend NE, August 2016

---

# @pusher

---

![fit](https://cl.ly/430q300M3E1n/Untitled.png)

---

![fit](http://f.cl.ly/items/2m2H1y3h0o460y0O2D2p/3E444D0F-12C8-4E17-AEDF-88FA1C400362.JPG)

---

# The State of JavaScript

---

_Or_: a series of things that I've been thinking about.

----

# :+1:

---

# Never been a better time

---

# Browers are getting more powerful

---

# More and more APIs being added

---

# The native DOM API isn't complete crap!

---

# Low Level APIs

---

# Service Worker vs App Cache

![inline](https://d2wvs5jsbn4h49.cloudfront.net/items/1g0k0h2C3d341k0F2U33/Screen%20Shot%202016-08-01%20at%2011.12.39.png)

https://vimeo.com/album/3953264/video/165995029

---

# App Cache

High Level, does one thing, hard to customise / control

---

# Service Worker

- Low level
- Less functionality "out of the box"
- Developers get full control

---

# JS is everywhere!

---

# Learning

---

# Reacting to frameworks

MVC doesn't work for client side applications.

---

Angular 1.X moved heavily to components.

Ember 2 removed controllers.

React only has components.

---

# Web Components

```html
<chat-app name="Jack"></chat-app>
```

---

![inline](https://d2wvs5jsbn4h49.cloudfront.net/items/3Z2j3m463j0e05472e08/Screen%20Shot%202016-08-01%20at%2011.27.33.png)

https://blog.pusher.com/realtime-web-components/

---

![](http://images.hellogiggles.com/uploads/2015/05/29/cc514bd2-9de1-4af6-840e-5dc07bd07b54.jpeg)

---

# ES2015 was a mess

---

# A _fantastic_, feature heavy mess

---

# ES2015 advances the language hugely

---

# But it came at a cost of overwhelming developers

---

# 50+

New features in ES2015[^1]

[^1]: I got bored of counting...

---

# 2

New features in ES2016

---

## `Array.prototype.includes`

---

Was going to be called `contains`, but MooTools adds `Array.prototype.contains`... [^2]

[^2]: https://esdiscuss.org/topic/having-a-non-enumerable-array-prototype-contains-may-not-be-web-compatible

---

# `**` (exponatiation)

---

# The new process works

---

- Stage 0: strawman
- Stage 1: proposal
- Stage 2: draft
- Stage 3: candidate
- Stage 4: finished

http://www.2ality.com/2015/11/tc39-process.html

---

# Each year any stage 4 proposals are taken into JS

---

# Yearly, small releases

---

# Easy to keep up with, easy to know browser support

---

# Transpilers

---

![](http://www.eikongraphia.com/images/language/Tower_of_Babel_3_S.jpg)

---

![](https://raw.githubusercontent.com/babel/logo/master/babel.png)

---

# ES2015 support

- Edge 14: 90%
- Chrome 52 / Opera 39: 98%
- FF 49: 93%
- Safari 10: 99%
- Node 6: 93%

(The final stumbling block is modules).

---

# Will we ever be rid of transpilers?

---

![fit](https://openclipart.org/image/2400px/svg_to_png/16078/noxin-crosshairs.png)

---

# Huge part of the JS proposal process

---

![fit](https://cl.ly/0T412x0j1p0o/Screen%20Shot%202016-08-01%20at%2013.53.08.png)

---

# :+1:

- Developers can try out new features ahead of time
- Feedback loop is shortened
- JS proposals don't feel so far away

---

# :-1:

- Developers leaning on features that _might_ not exist

---

# Be wary of depending on Babel plugins for early stage proposals

Or at least, be prepared for a rewrite.

---

# Do you need Babel?

---

- Edge 14: 90%
- Chrome 52 / Opera 39: 98%
- FF 49: 93%
- Safari 10: 99%
- Node 6: 93%

---

# Node 6: (nearly) full ES2015 support

`babel-preset-node6`

OR: no Babel depending on what features you need.

---

# Will we be using transpilers forever?

---

# If you want to stick right on the cutting edge and use features before they are in browsers, yes.

---

# If you're happy to use a subset of new features, or lucky enough to target "modern" browsers, no.

---

# Once ES2015 is fully supported across all browsers most people build for, less people will use transpilers

---

#`<br />`

---

# Modules!

---

# NodeJS is dreamy

```
$ npm install x

// index.js
var x = require('x');

$ node index.js
```

---

1. Install a package.
2. Use it.

---

# That's what we want in the browser.

---

# ES2015 modules in the browser [^3]

```html
<script type="module">
  import { fn } from './lib';
  import React from 'http://cdn.com/react.js';
</script>
```

[^3]: not yet supported across browsers

---

![inline](https://cl.ly/1G3K2R3z3q1o/Screen%20Shot%202016-08-01%20at%2014.12.11.png)


Guy Bedford, PolyConf[^4]

[^4]: https://www.youtube.com/watch?v=cRSBi1EAOCo

---

![](http://miriadna.com/desctopwalls/images/max/Looking-at-the-tops-of-trees.jpg)

---

# ES2015 imports and exports are _static_

---

```js
// nooooppee
if (x) {
  import React from 'react';
  export { y };
}

```

---

Use `map` from Lodash:

```
var _ = require('lodash');

_.map(...);
```

Then:

```
some-bundle-tool app.js > bundle.js
```

Included:

- your code
- ALL of Lodash

---

In a fully ES2015 moduled world

```
import { map } from 'lodash';

_.map(...);
```

Then:

```
some-bundle-tool app.js > bundle.js
```

Included:

- your code
- Just `lodash.map!`

---

# We're not there yet

ES2015 module support is lacking across _everywhere_.

---

# A fully ES2015 module web will be a much better one.

---

![inline](https://cl.ly/082i1b2b3X2J/Screen%20Shot%202016-08-03%20at%2009.45.18.png)

https://github.com/rollup/rollup

---

# Tooling woes

---

![fit](http://www.internationalhealth.info/wp-content/uploads/2015/11/fatigue.jpg)

---

# JavaScript Fatigue = we're figuring this out

---

# _You_ have control here.

---

# Find your preferred tool set.

---

# Browserify, Webpack, jspm, others?

---

# ES2015? Babel?

---

# Stick with your toolchain

---

# Evaluate every now and then

---

# The baseline

---

Webpack is _not_ the baseline

Gulp / Grunt is _not_ the baseline

browserify is _not_ the baseline

React is _not_ the baseline

---

```html
<script>
  console.log('hello world');
</script>
```

is the baseline

---

# This should _always_ be the baseline

---

# Especially for beginners

---

# And this is how we have to teach JavaScript

---

# Layer your tools as you need to

---

# But _not_ before

---

# Finding the right abstraction

--- 

# React is an abstraction

---

# The price of abstractions is a little indirection

---

# The payoff is quicker, nicer and _more enjoyable_ development

---

# _Nothing_ is free

---

# Performance

---

![inline](https://d17oy1vhnax1f7.cloudfront.net/items/3h1w0E1C3t2n0F2P0a2v/Screen%20Shot%202016-08-03%20at%2008.34.42.png)

https://developers.google.com/web/tools/chrome-devtools/profile/evaluate-performance/rail?hl=en

---

# Paul Lewis: RAIL in the real world [^5]

[^5]: https://www.youtube.com/watch?v=iIV1xPFXmBs

---

# Progressive Web Apps

---

![inline](https://cl.ly/2f1i3u013D3o/Screen%20Shot%202016-08-03%20at%2008.39.54.png)

https://addyosmani.com/blog/getting-started-with-progressive-web-apps/

---

:+1: Load Instantly (Service Worker)
:+1: Add to Home Screen
:+1: Web push notifications
:+1: Secure
:+1: Fast
:+1: Responsive

https://developers.google.com/web/progressive-web-apps/

---

# Offering a great mobile experience on the web

---

## Flipkart, India’s largest e-commerce site, decided to combine their web presence and native app into a Progressive Web Application that has resulted in a 70% increase in conversions. [^6]

[^6]: https://developers.google.com/web/showcase/2016/flipkart

---

# Server Side Rendering

---

![inline](https://cl.ly/0A3v0N3M2e2b/Screen%20Shot%202016-08-03%20at%2009.38.31.png)

---

# GoCardless is a universal ReactJS application [^7]

[^7]: https://gocardless.com/blog/how-we-built-the-new-gocardless.com/

---

> Once the initial page is displayed, a request is made to fetch the rest of the site's React app.

---

> All subsequent navigation is blindingly fast, not suffering the latency of HTTP requests since the browser already has the whole app.

---

> If the user does not have JS, they still experience the fully rendered page and only miss out on the fast navigation.

---

- Ember Fastboot
- Angular 2 Universal
- And others

(This isn't for every app!)

---

![inline](https://cl.ly/2H1h1p3k0331/Screen%20Shot%202016-08-03%20at%2009.41.48.png)

https://www.youtube.com/watch?v=Bb0Uk8c6ltQ

---

# Is the web getting more complicated?

---

# It _depends_

---

# Is it hard work to build a performant, mobile friendly, offline first web application?

---

# Yes

---

# But that's exciting!

---

# No one is making you build complex, progressive, offline first apps in the browser.

---

# But there's lots of great reasons to

---

# And if you spend the time and energy.

---

# You'll get your rewards.

---

# And have _loads_ of fun in the meantime!

---

# Thanks

@Jack_Franklin

javascriptplayground.com

---


