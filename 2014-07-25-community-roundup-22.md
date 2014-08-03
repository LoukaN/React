---
title: "Community Round-up #22"
layout: post
author: Lou Husson
---

## Saving time & Staying sane? Pros & Cons of React
When [Kent William Innholt](http://http://kentwilliam.com/) start working for [M>Path](http://mpath.com/) he had to build an ambitious new web app, where the UI complexity represents most of the app's complexity overall. It is in this spirit he start to uses React and he wrote this  [article](http://kentwilliam.com/articles/saving-time-staying-sane-pros-cons-of-react-js). 


>```javascript
ToggleButton = React.createClass
  getInitialState: -> 
    active: false
  toggle: ->
    @setState active: not @state.active
  render: ->
    React.DOM.button
      className: 'active' if @state.active 
      onClick: @toggle
```


## Deconstructing ReactJS's Flux

Mikael Brassman shown [some examples](http://spoike.ghost.io/deconstructing-reactjss-flux/) of the single directional data-flow architecture by comparing React reference implementation of Flux and using a library he wrote called [Reflux](https://github.com/spoike/reflux).

<iframe allowfullscreen="" data-progress="true" frameborder="0" height="390" id="vimeo-player" mozallowfullscreen="" src="//player.vimeo.com/video/100245392?api=1&amp;title=0" webkitallowfullscreen="" width="640"></iframe>


## How to keep a fast build with Browserify and React

[idontknowyet](http://blog.avisi.nl/2014/04/25/how-to-keep-a-fast-build-with-browserify-and-reactjs/)

>```javascript
var gulp = require('gulp');
var browserify = require('browserify');
var source = require('vinyl-source-stream');
var reactify = require('reactify');
var production = process.env.NODE_ENV === 'production';
gulp.task('scripts', function () {
  var bundler = browserify('./src/client.js', {basedir: __dirname, debug: !production}});
  bundler.transform(reactify);
  var stream = bundler.bundle();
  return stream
    .pipe(source('bundle.js'))
    .pipe(gulp.dest('./assets/js'));
});
```


## IntegratedCSS

After integrating HTML into JavaScript by React, a logical next step for Sander Spies is to do the same for [CSS](https://github.com/SanderSpies/IntegratedCSS).

>
- It takes out the css function and transform it into plain CSS
- The css function is executed on its own, it has no reference to 'this'
- connect the (something.)css().something blocks to CSS
- create CSS with annoyingly small CSS className selectors (3 characters max - up to 140608 classes)
- CSS is coupled to the component and can be passed to another component via props (aProp={this.css().something})
- isn't smart about actual references to the CSS function


## Blazing Fast HTML

[Evan Czaplicki](http://evan.czaplicki.us) wrote an article about the new [elm-html](https://github.com/evancz/elm-html). It's a library which lets you use HTML and CSS directly in Elm.

[![](/img/sampleResults.png)](http://elm-lang.org/diagrams/sampleResults.png)

## React : Components Tutorial

[Harris Brakmic](https://twitter.com/brakmic/status/490910003650633728) shared 2 youtube video from [Joe Maddalone](http://www.joemaddalone.com/)

- Part 1 : how to create and nest React Components
<iframe width="560" height="315" src="//www.youtube.com/embed/rFvZydtmsxM" frameborder="0" allowfullscreen></iframe>

- Part 2 : Dynamic React interactive components
<iframe width="560" height="315" src="//www.youtube.com/embed/5yvFLrt7N8M" frameborder="0" allowfullscreen></iframe>

## Javascript's History and How it led to React
[Chris Dawson](https://github.com/xrd) wrote an article about Christopher Chedeau [OSCon presentation's](http://www.oscon.com/oscon2014/public/schedule/speaker/133198)

## Reusable components by Khan Academy
[Khan Academy](https://www.khanacademy.org/) wrote a pretty cool [collection](http://khan.github.io/react-components/) of some of the most reusable React component built at Khan Academy.

> 
- Button Group
- $_
- Layered Component Mixin
- Set Interval Mixin
- TimeAgo
- Blur Input
- TeX
- Tooltip
- Info-Tip
- Sortable
- Drag Target
- Timeout Transition Group
- Backbone Mixin
- Window Drag


## Using Flux to Build UIs with React

If you haven't yet tried out React, [Gary Chambers](https://twitter.com/garychambers108) did a [guide](https://medium.com/@garychambers108/flux-in-practice-ec08daa9041a) to building UIs with React on [Flux](http://facebook.github.io/flux/).



## Random Tweets
<blockquote class="twitter-tweet" lang="en"><p>We shipped reddit&#39;s first production <a href="https://twitter.com/reactjs">@reactjs</a> code last week, our checkout process.&#10;&#10;<a href="https://t.co/KUInwsCmAF">https://t.co/KUInwsCmAF</a></p>&mdash; Brian Holt (@holtbt) <a href="https://twitter.com/holtbt/statuses/493852312604254208">July 28, 2014</a></blockquote>
<blockquote class="twitter-tweet" lang="en"><p>.<a href="https://twitter.com/AirbnbNerds">@AirbnbNerds</a> just launched our first user-facing React.js feature to production! We love it so far. <a href="https://t.co/KtyudemcIW">https://t.co/KtyudemcIW</a> /<a href="https://twitter.com/floydophone">@floydophone</a></p>&mdash; spikebrehm (@spikebrehm) <a href="https://twitter.com/spikebrehm/statuses/491645223643013121">July 22, 2014</a></blockquote>
