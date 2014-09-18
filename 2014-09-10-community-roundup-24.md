---
title: "Community Round-up #24"
layout: post
author: Lou Husson
---

# Flux Special Edition

<iframe width="560" height="315" src="//www.youtube.com/embed/nYkdrAPrdcw?list=PLb0IAmt7-GS188xDYE-u1ShQmFFGbrk0v" frameborder="0" allowfullscreen></iframe>

Flux is an application architecture for React utilizing a unidrectional data flow.
[Christian Alfoni](https://github.com/christianalfoni) wrote an [article](http://christianalfoni.github.io/javascript/2014/08/20/react-js-and-flux.html) which explain why you would want to consider the flux architecture with React JS as your tool to build an interface, and handle interaction and updates to that interface.
[An example of this architecture is available](https://github.com/facebook/flux/tree/master/examples/flux-todomvc)

## Flux : Step by Step approach

[Nicola Paolucci](https://github.com/durdn) wrote a great guide to help your getting understand [Flux Step by Step](http://blogs.atlassian.com/2014/08/flux-architecture-step-by-step/)


## Flux architecture with a Demo app built with React & ASP.NET

[Shiju Varghese](https://github.com/shijuvar) developped a Demo app using Flux architecture [react-aspnet](https://github.com/shijuvar/react-aspnet) and looking for contributor to optimitize the Flux implementation.

## RefluxJS

[Mikael Brassman](https://github.com/spoike) wrote a simple library for unidirectional dataflow architecture inspired by React [Flux](http://facebook.github.io/react/blog/2014/05/06/flux.html).

[![](http://puu.sh/bBEvU/b068472024.png)](https://github.com/spoike/refluxjs)


## React And Flux at New Circle

Facebook engineers [Bill Fisher](https://github.com/fisherwebdev) and [Jing Chen](https://github.com/jingc) gave a talk about Flux and React, and how using an application architecture with a unidirectional data flow cleans up a lot of their code.

<iframe width="560" height="315" src="//www.youtube.com/embed/i__969noyAM" frameborder="0" allowfullscreen></iframe>

## React + Flux is going into Adobe's Brackets

Kevin Dangoor wrote [xx](http://www.kevindangoor.com/2014/09/intro-to-the-new-brackets-project-tree/)

![](http://puu.sh/bDoyG/fcf73f9057.jpg)


## Implementing Undo-Redo

[Ameya Karve](https://github.com/ameyakarve) write an [article](http://ameyakarve.com/jekyll/update/2014/02/06/Undo-React-Flux-Mori.html) about implementing Undo-Redo in React components using Flux.


## Refactoring to React

[Stafano Masini](https://github.com/stefanomasini) gave a talk at [Amsterdam Javascript MVC Meetup](http://www.meetup.com/JavaScript-MVC-Meetup-Amsterdam/) on the Refactoring to React.

<iframe width="420" height="315" src="//www.youtube.com/embed/MivXyEtwK24" frameborder="0" allowfullscreen></iframe>


## Deconstructing ReactJS's Flux

Mikael Brassman shown [some examples](http://spoike.ghost.io/deconstructing-reactjss-flux/) of the single directional data-flow architecture by comparing React reference implementation of Flux and using a library he wrote called [Reflux](https://github.com/spoike/reflux).

<iframe allowfullscreen="" data-progress="true" frameborder="0" height="390" id="vimeo-player" mozallowfullscreen="" src="//player.vimeo.com/video/100245392?api=1&amp;title=0" webkitallowfullscreen="" width="640"></iframe>


## Using Flux to Build UIs with React

If you haven't yet tried out React, [Gary Chambers](https://twitter.com/garychambers108) did a [guide](https://medium.com/@garychambers108/flux-in-practice-ec08daa9041a) to building UIs with React on [Flux](http://facebook.github.io/flux/).


## DoLorean : Back to the future !
[DoLorean](https://github.com/deloreanjs/delorean) is a tiny Flux pattern implementation developped by [Fatih Kadir Akin](https://github.com/f).
>
- Unidirectional data flow, it makes your app logic simpler than MVC,
- Automatically listens to data changes and keeps your data updated,
- Makes data more consistent across your whole application,
- It's framework agnostic, completely. There's no view framework dependency.
- Very small, just 4K gzipped.
- Built-in React.js integration, easy to use with Flight.js and Ractive.js and probably all others.
- Improve your UI/data consistency using rollbacks.

![](http://puu.sh/bBFkq/2720b577ef.png)