---
title: "Community Round-up #20"
layout: post
author: Lou Husson
---
## We don’t made any Round-up for month ago, it is thus time to make the Round-up #20.
Currently, React get more commit from open source than Facebook Software Engineer

## React Meetups!
ReactJS will be present from 20 till 23 July in [San Francisco](http://www.meetup.com/ReactJS-San-Francisco/events/195518392/)  for a Meetup powered by Prezi about “Immediate Mode on the Web: How We Implemented the Prezi Viewer in JavaScript”.

If you have miss the last [London User Group Meetup](http://www.meetup.com/London-React-User-Group/events/191406572/) : 

<iframe width="560" height="315" src="//www.youtube.com/watch?v=CP3lvm5Ppqo" frameborder="0" allowfullscreen></iframe>

By the way, Wednesday in May the 28th 2014 there was the [JSConf](http://2014.jsconf.us/) 2014 where Christopher Chedeau do a talk about “Why does React Scale?” :

<iframe width="560" height="315" src="//www.youtube.com/watch?v=D-ioDiacTm8" frameborder="0" allowfullscreen></iframe>


## More People Using React

[Josephine Hall](http://icelab.com.au/about/#josephine-hall), from Ice Lab write a news named [“Thinking and Learning React.js”](http://icelab.com.au/articles/thinking-and-learning-reactjs/) after using React to build a mobile-focussed app for one of his clients

### Adding live edit to a React Project
[Dan Abramov](https://twitter.com/dan_abramov) wrote step-by-step instructions on [adding live edit to a React project](http://gaearon.github.io/react-hot-loader/)

>```
Meet react-hot-loader, a drop-in Webpack loader1 you can use to enable live editing for React components in your projects. No browser plugins or IDE hooks required.
```

###Acorn JSX a 1.5-2x faster React.js JSX parser
[Acorn JSX Edition](https://github.com/RReverser/acorn-jsx) by Ingvar Stepanyan is an experimental, alternative, faster React.js JSX parser by integrating pieces of code from official parser, modified to match Acorn’s parsing logic.

### ReactScriptLoader
Yariv Sadan created [ReactScriptLoader](https://github.com/yariv/ReactScriptLoader) to make it easier to load external scripts.

>```javascript
/** @jsx React.DOM */
var Foo = React.createClass({
    mixins: [ReactScriptLoaderMixin],
    getInitialState: function() {
        return {
            scriptLoading: true,
            scriptLoadError: false,
        };
    },
    getScriptURL: function() {
        return 'http://d3js.org/d3.v3.min.js';
    },
    onScriptLoaded: function() {
        this.setState({scriptLoading: false});
    },
    onScriptError: function() {
        this.setState({scriptLoading: false, scriptLoadError: true});
    },
    render: function() {
        var message;
        if (this.state.scriptLoading) {
            message = 'loading script...';
        } else if (this.state.scriptLoadError) {
            message = 'loading failed';
        } else {
            message = 'loading succeeded';
        }
        return <span>{message}</span>;
    }
});
```

### ReactIntl Mixin by Yahoo
Yahoo implements a [ReactJS component mixin](https://github.com/yahoo/react-intl) that adds these new methods to any React component.

>```javascript
var MyComponent = React.createClass({
  mixins: [ReactIntlMixin],
  render: function () {
    return <div>
      <p>A: {this.intlDate(1390518044403, { hour: 'numeric', minute: 'numeric' })}</p>
      <p>B: {this.intlNumber(400, { style: 'percent' })}</p>
    </div>;
  }
});
```

### Atom version 0.116.0 enable React editor component by default
Atom.io recently release the new [React editor Component](http://blog.atom.io/2014/07/22/default-to-react-editor.html) using ReactJS.
[![](http://blog.atom.io/img/posts/use-react-editor.png)](http://blog.atom.io/2014/07/22/default-to-react-editor.html)

### Using ReactJS and KendoUI Together
Beautiful Design explained by Jim Cowart in this [news](http://www.ifandelse.com/using-reactjs-and-kendoui-together/).

[![](/img/kendoresult.png)](http://www.ifandelse.com/using-reactjs-and-kendoui-together/)

## Random Tweet
<blockquote class="twitter-tweet" lang="en"><p>I take back the mean things I said about <a href="https://twitter.com/reactjs">@reactjs</a> I actually like it.</p>&mdash; Apphacker (@apphacker) <a href="https://twitter.com/apphacker/status/490738080156893184">July 20, 2014</a></blockquote>