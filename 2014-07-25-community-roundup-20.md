---
title: "Community Round-up #20"
layout: post
author: Lou Husson
---
## We don’t made any Round-up for month ago, it is thus time to make the Round-up #20.
[]()
## React Meetups!
ReactJS will be present from 20 till 23 July in [San Francisco](http://www.meetup.com/ReactJS-San-Francisco/events/195518392/)  for a Meetup powered by Prezi about “Immediate Mode on the Web: How We Implemented the Prezi Viewer in JavaScript”.

If you have miss the last [London User Group Meetup](http://www.meetup.com/London-React-User-Group/events/191406572/) you can find the broadcast [here](https://www.youtube.com/watch?v=CP3lvm5Ppqo).

By the way, Wednesday in May the 28th 2014 there was the [JSConf](http://2014.jsconf.us/) 2014 where Christopher Chedeau do a talk about  [“Why does React Scale?”](https://www.youtube.com/watch?v=D-ioDiacTm8).

## React Community
For some time, we are amaze by seeing how the community is invested, every action are the symbol of a growing community, and that’s clear to us  we have to support you the best we could.

[John Linch](https://twitter.com/johnrlynch) make a [Twitter List](https://twitter.com/johnrlynch/facebook-react-js/members) which can helps everybody to get in touch with the community.

## More People Using React

You have to read this article from Ice Lab, write by [Josephine Hall](http://icelab.com.au/about/#josephine-hall), [“Thinking and Learning React.js”](http://icelab.com.au/articles/thinking-and-learning-reactjs/)

### ReactScriptLoader
Yariv Sadan created [ReactScriptLoader](https://github.com/yariv/ReactScriptLoader) to make it easier to load external scripts.

>```
/** @jsx React.DOM */

var React = require('react');
var ReactScriptLoaderMixin = require('./ReactScriptLoaderMixin.js').ReactScriptLoaderMixin;

var Foo = React.createClass({
    mixins: [ReactScriptLoaderMixin],
    getInitialState: function() {
        return {
            scriptLoading: true,
            scriptLoadError: false,
        };
    },

    // this function tells ReactScriptLoaderMixin where to load the script from
    getScriptURL: function() {
        return 'http://d3js.org/d3.v3.min.js';
    },

    // ReactScriptLoaderMixin calls this function when the script has loaded
    // successfully.
    onScriptLoaded: function() {
        this.setState({scriptLoading: false});
    },

    // ReactScriptLoaderMixin calls this function when the script has failed to load.
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

>```
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
That's what Jim Cowart explain in this [news](http://www.ifandelse.com/using-reactjs-and-kendoui-together/).

>```
var KendoExample = React.createClass({

  mixins: [React.postal],

  getInitialState: function() {
    return {
      speed: 88,
      uom:"MPH"
    }
  },

  componentWillMount: function() {
    this.subscribe("change.#", function(data) {
      this.setState(data);
    });
  },

  componentWillUnmount: function() {
    this.disposeSubscriptions();
  },

render: function() {
    return <div>
      <div className="container">
        <Kendo.RadialGauge value={this.state.speed} />
        <Kendo.Slider value={this.state.speed} id="gauge-slider" channel={this.props.channel} />
        <UnitOfMeasure channel={this.props.channel} />
      </div>
      <SpeedDisplay speed={this.state.speed} uom={this.state.uom} />
    </div>;
  }
});
```
###Acorn JSX a faster React.js JSX parser
[Acorn JSX Edition](https://github.com/RReverser/acorn-jsx) by Ingvar Stepanyan is an experimental, alternative, faster React.js JSX parser by integrating pieces of code from official parser, modified to match Acorn’s parsing logic.

## Random Tweet

<blockquote class="twitter-tweet" lang="en"><p>I take back the mean things I said about <a href="https://twitter.com/reactjs">@reactjs</a> I actually like it.</p>&mdash; Apphacker (@apphacker) <a href="https://twitter.com/apphacker/status/490738080156893184">July 20, 2014</a></blockquote>