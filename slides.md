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
```

---

# Tooling woes

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

# Layer your tools as you need to

---

# But _not_ before

---

## Finding the right abstraction

--- 

# Performance

---

# Server Side

---

