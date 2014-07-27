---
title: "Community Round-up #21"
layout: post
author: Lou Husson
---

## React Router : A complete routing library for React.
[Ryan Florence](https://github.com/rpflorence) share a project named [React Router](https://github.com/rackt/react-router) on Github who allow you to complete trace your library for React.
The author highlights four benefits of this approach : an incredible screen-creation productivity, an immediate understanding of application structure, a code tractability and urls are your first thought, not an after-thougt.

>```
Features
- Nested views mapped to nested routes
- Modular construction of route hierarchy
- Fully asynchronous transition hooks
- Transition abort / redirect / retry
- Dynamic segments
- Query parameters
- Links with automatic .active class when their route is active
- Multiple root routes
- Hash or HTML5 history URLs
```

## Building UIs with ReactJS
Tutorial with Jacob Rios about buidling user interfaces with ReactJS.
<iframe width="560" height="315" src="//www.youtube.com/embed/lAn7GVoGlKU" frameborder="0" allowfullscreen></iframe>

## Using React components as Backbone Views
[Venmo](https://venmo.com/) have begun rewriting and redesigning his front-end. The best situation to try ReactJS :)
[Thomas Boyt](http://www.thomasboyt.com/) write a news [Using React components as Backbone View](http://www.thomasboyt.com/2013/12/17/using-reactjs-as-a-backbone-view.html).

> "The most unique and most controversial part of React is its use of JSX"

>```javascript
/** @jsx React.DOM */
var component = React.createClass({
  render: function() {
    return <a href="http://venmo.com">Venmo</a>
  }
});
```

## React Dispatcher
The dispatcher is used to control the flow of actions through your application. That's what you can find in this [project](https://github.com/rackt/react-dispatcher) started by [Michael Jackson](https://github.com/mjackson). So, let's Beat it !

>```javascript
Dispatcher.registerHandler(function (actionName, actionArgs) {
  if (actionName === 'login') {
    var username = actionArgs[0], password = actionArgs[1];
    return checkCredentials(username, password);
  }
});
var Login = React.createClass({
  mixins: [ Dispatcher.ActionSender ],
  getInitialState: function () {
    return { errorMessage: '' };
  },
  handleLoginError: function (error) {
    this.setState({ errorMessage: error.message });
  },
  handleSubmit: function () {
    var username = this.refs.username.getDOMNode().value;
    var password = this.refs.password.getDOMNode().value;
    this.sendAction('login', username, password).then(function () {
      Router.transitionTo('/home/' + username);
    }, this.handleLoginError);
  },
  render: function () {
    var error;
    if (this.state.errorMessage)
      error = <div className="error">{this.state.errorMessage}</div>;
    return (
      {error}
      <form onSubmit={this.handleSubmit}>
        <input ref="username" type="text" name="username"/>
        <input ref="password" type="password" name="password"/>
      </form>
    );
  }
});
```

## React Draggable
[Matt Zabriskie](https://github.com/mzabriskie) release a [project](https://github.com/mzabriskie/react-draggable) to turn your react component draggable.

[![](/img/draggable.png)](http://mzabriskie.github.io/react-draggable/example/)

## First Look: Getting Started with Facebook’s ReactJS Library
[Kirill Buga](http://modernweb.com/authors/kirill-buga/) share about his [experience](http://modernweb.com/2014/07/23/getting-started-reactjs/?utm_content=bufferac1a8&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer) getting started with the ReactJS Library from Facebook.
ReactJS will definitely change your perception of Front-end implementation.

[![](/img/reactimg21.png)](http://modernweb.com/2014/07/23/getting-started-reactjs/)

## What's ReactJS ?
[Craig McKeachie](http://www.funnyant.com/author/admin/) author of [Javascript Framework Guide](http://www.funnyant.com/javascript-framework-guide/) write an excellent news named ["What is React.js? Another Template Library?](http://www.funnyant.com/reactjs-what-is-it/) Like Web Components? A Framework like AngularJS?". I think everybody who's starting React have to read it !

### 5 Best Mobiles Web App Frameworks : React
[Grgur Grisogono](https://github.com/grgur) write an article ["5 Best Mobile Web App Frameworks : React"](http://moduscreate.com/5-best-mobile-web-app-frameworks-reactjs/).
This news describe with precision the ReactJS strenght's.

## Random Tweet
<blockquote class="twitter-tweet" lang="en"><p>Testing newforms' upcoming locale release with <a href="https://twitter.com/reactjs">@reactjs</a> 0.11.x - I like it when little weird things get improved</p>&mdash; Jonny Buchanan (@jbscript) <a href="https://twitter.com/jbscript/status/493339826796908544/photo/1">July 20, 2014</a></blockquote>