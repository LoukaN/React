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


## Building UIs with React

If you haven't yet tried out React, Jacob Rios did a Hangout where he covers the most important aspects and thankfully he recorded it!

<iframe width="650" height="315" src="//www.youtube.com/embed/lAn7GVoGlKU" frameborder="0" allowfullscreen></iframe>


## Compiling JSX with Sweet.js using Readtables

[JSX](http://jlongster.com/Compiling-JSX-with-Sweet.js-using-Readtables) is a Facebook project that embeds an XML-like language in JavaScript.

<img src="http://i.imgur.com/jlvJqx1.png" />

## Airbnb launched first user-facing React feature to production

[![](/react/img/blog/airbnb.png)](https://www.airbnb.com/resolutions)

## React Draggable
[Matt Zabriskie](https://github.com/mzabriskie) release a [project](https://github.com/mzabriskie/react-draggable) to turn your react component draggable.

[![](/react/img/blog/draggable.png)](http://mzabriskie.github.io/react-draggable/example/)

## HTML Parser2 React
[Jason Brown](https://github.com/browniefed) 

## Referencing Dynamic Children
Very good news by Matt Zabriskie about [referencing dynamic children](http://www.mattzabriskie.com/blog/react-referencing-dynamic-children).

>```javascript
var App = React.createClass({
    render: function () {
        return (
            <div>
                {this.props.children}
            </div>
        );
    }
});
```

## A Few more words on Acorn-JSX

Ingvar Stepanyan talking about Acorn JSX in the last Roundup, now Ingvar finish the developpment of [complete ES6 support](http://rreverser.com/a-few-more-words-on-acorn-jsx/)


## First Look: Getting Started with Facebookâ€™s React Library

[Kirill Buga](http://modernweb.com/authors/kirill-buga/) share about his [experience](http://modernweb.com/2014/07/23/getting-started-reactjs/?utm_content=bufferac1a8&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer) getting started with the ReactJS Library from Facebook.
React will definitely change your perception of Front-end implementation.

[<img src="http://modernweb.com/wp-content/uploads/2014/07/Screen-Shot-2014-07-22-at-15.30.40.png" style="width: 100%;" />](http://modernweb.com/2014/07/23/getting-started-reactjs/)


## What's React ?

[Craig McKeachie](http://www.funnyant.com/author/admin/) author of [Javascript Framework Guide](http://www.funnyant.com/javascript-framework-guide/) write an excellent news named ["What is React.js? Another Template Library?](http://www.funnyant.com/reactjs-what-is-it/) Like Web Components? A Framework like AngularJS?". I think everybody who's starting React have to read it !


## 5 Best Mobiles Web App Frameworks : React

[Grgur Grisogono](https://github.com/grgur) write an article ["5 Best Mobile Web App Frameworks : React"](http://moduscreate.com/5-best-mobile-web-app-frameworks-reactjs/).
This news describe with precision the React strenght's.


## Random Tweet

<blockquote class="twitter-tweet" lang="en"><p>Testing newforms' upcoming locale release with <a href="https://twitter.com/reactjs">@reactjs</a> 0.11.x - I like it when little weird things get improved</p>&mdash; Jonny Buchanan (@jbscript) <a href="https://twitter.com/jbscript/status/493339826796908544/photo/1">July 20, 2014</a></blockquote>