---
title: "Community Round-up #21"
layout: post
author: Lou Husson
---

## React Router
[Ryan Florence](http://ryanflorence.com/) and [Michael Jackson](http://twitter.com/mjackson) ported Ember's router to React in a project boringly called [React Router](https://github.com/rackt/react-router). This is a very good example of both communities working together to make the web better!

```javascript
React.renderComponent((
  <Routes>
    <Route handler={App}>
      <Route name="about" handler={About}/>
      <Route name="users" handler={Users}>
        <Route name="user" path="/user/:userId" handler={User}/>
      </Route>
    </Route>
  </Routes>
), document.body);
```

## Going big with React

Areeb Malik talks about using React at Facebook. "On paper, all those JS frameworks look promising: clean implementations, quick code design, flawless execution. But what happens when you stress test Javascript? What happens when you throw 6 megabytes of code at it? In this talk, we'll investigate how React performs in a high stress situation, and how it has helped our team build safe code on a massive scale"

<iframe allowfullscreen="" data-progress="true" frameborder="0" height="390" id="vimeo-player" mozallowfullscreen="" src="//player.vimeo.com/video/100245392?api=1&amp;title=0" webkitallowfullscreen="" width="640"></iframe>


## What's React?

[Craig McKeachie](http://www.funnyant.com/author/admin/) author of [Javascript Framework Guide](http://www.funnyant.com/javascript-framework-guide/) wrote an excellent news named ["What is React.js? Another Template Library?](http://www.funnyant.com/reactjs-what-is-it/) 

>
- Is React a Template Library?
- Is React Similar to Web Components?
- Are the Virtual DOM and Shadow DOM the Same?
- Can React be used with other JavaScript MVC Frameworks?
- Who Uses React.js?
- Is React a Premature Optimization if you aren’t Facebook or Instagram?
- Can I Work with Designers?
- Will React Hurt my Search Engine Optimization (SEO)?
- Is React a Framework for Building Applications or a Library with One Feature?
- Are components a better way to build an application?
- Can I build something complex with React?

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
