---
title: "Community Round-up #22"
layout: post
author: Lou Husson
---

## Saving time & Staying sane? Pros & Cons of React
[Kent William Innholt](http://http://kentwilliam.com/) text text text [New Web app tech stack](http://kentwilliam.com/articles/saving-time-staying-sane-pros-cons-of-react-js). 

```javascript
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


## Blazing Fast HTML

[Evan Czaplicki](http://evan.czaplicki.us) wrote an article about the new [elm-html](https://github.com/evancz/elm-html). It's a library which lets you use HTML and CSS directly in Elm.

[![](/img/sampleResults.png)](http://elm-lang.org/diagrams/sampleResults.png)

## Referencing Dynamic Children

While Matt was working  on [react-tabs](https://www.npmjs.org/package/react-tabs) he discovered how to use React.Children.map and React.addons.cloneWithProps in order to [referencing dynamic children](http://www.mattzabriskie.com/blog/react-referencing-dynamic-children).

```javascript
var App = React.createClass({
    render: function () {
        var index = 0,
            children = React.Children.map(this.props.children, function (child) {
            return React.addons.cloneWithProps(child, {
                ref: 'child-' + (index++)
            });
        });
        return (
            <div>
                {children}
            </div>
        );
    }
});
```


## JSX with Sweet.js using Readtables

Have you ever wondered how JSX was implemented? James Long wrote a very instructive blog post that explains how to [compile JSX with Sweet.js using Readtables](http://jlongster.com/Compiling-JSX-with-Sweet.js-using-Readtables).

<a href="http://jlong\
ster.com/Compiling-JSX-with-Sweet.js-using-Readtables"><img src="http://i.imgur.com/jlvJqx1.png" /></a>


## First Look: Getting Started with React

[Kirill Buga](http://modernweb.com/authors/kirill-buga/) wrote an article on Modern Web explaining how React is [different](http://modernweb.com/2014/07/23/getting-started-reactjs/) from traditional MVC used by most JavaScript applications 

[![](/img/getstart.png)](http://modernweb.com/2014/07/23/getting-started-reactjs)


## React Draggable

[Matt Zabriskie](https://github.com/mzabriskie) released a [project](https://github.com/mzabriskie/react-draggable) to turn your react component draggable.

[![](http://i.imgur.com/EiWPhGP.png)](http://mzabriskie.github.io/react-draggable/example/)


## HTML Parser2 React

[Jason Brown](http://browniefed.github.io/) adapted htmlparser2 to React : [htmlparser2-react](https://www.npmjs.org/package/htmlparser2-react). That allows you to convert raw html to react DOM components.
This is not the intended way to use React but can be useful as last resort if you have an existing piece of HTML.

```javascript
var html = '<div data-id="1" class="hey this is a class" style="width:100%;height: 100%;"><article id="this-article"><p>hey this is a paragraph</p><div><ul><li>1</li><li>2</li><li>3</li></ul></div></article></div>';
var parsedComponent = reactParser(html, React);
```

## Building UIs with React

If you haven't yet tried out React, Jacob Rios did a Hangout where he covers the most important aspects and thankfully he recorded it!

<iframe width="650" height="315" src="//www.youtube.com/embed/lAn7GVoGlKU" frameborder="0" allowfullscreen></iframe>


## Random Tweets
<blockquote class="twitter-tweet" lang="en"><p>We shipped reddit&#39;s first production <a href="https://twitter.com/reactjs">@reactjs</a> code last week, our checkout process.&#10;&#10;<a href="https://t.co/KUInwsCmAF">https://t.co/KUInwsCmAF</a></p>&mdash; Brian Holt (@holtbt) <a href="https://twitter.com/holtbt/statuses/493852312604254208">July 28, 2014</a></blockquote>
<blockquote class="twitter-tweet" lang="en"><p>.<a href="https://twitter.com/AirbnbNerds">@AirbnbNerds</a> just launched our first user-facing React.js feature to production! We love it so far. <a href="https://t.co/KtyudemcIW">https://t.co/KtyudemcIW</a> /<a href="https://twitter.com/floydophone">@floydophone</a></p>&mdash; spikebrehm (@spikebrehm) <a href="https://twitter.com/spikebrehm/statuses/491645223643013121">July 22, 2014</a></blockquote>
