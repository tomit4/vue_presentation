# VueJS

## That Other JS Framework

### On JavaScript Frameworks

The ecosystem within Web Development is perhaps the most fast past and
continually changing environment out of all Development Fields. While the
majority of Web Developers will point to their bread and butter tools like HTML,
CSS, and JavaScript as being the cornerstone necessities of their field, it would be
naive to claim that that's all one needs to know to work within Web
Development today. Keeping up with Web Standards such as Semantic and Accessible HTML,
Browser Compatibility, Search Engine Optimization, and a plethora of other
conventions is only scratching the surface of what one needs to become familiar with.

One of the most contentious and exciting aspects of Frontend Web Development is
that of JavaScript Libraries. Very briefly, a JavaScript library is a collection
of pre-written JS code that allows for easier development of applications,
with an emphasis on AJAX and web-centric technologies.

One of the earliest JavaScript libraries that is still under active development
and usage today is [JQuery](https://en.wikipedia.org/w/index.php?title=JQuery),
which utilizes a series of syntactically simplified callback functions to more
easily manipulate the DOM (Document Object Model).

More modern JavaScript Libraries have been in active development and usage
since the release of Google's AngularJS in 2010, and Facebook's ReactJS in 2013. The
history of each of these libraries indicates that the complexity of what
web developers have been tasked with creating has only become more and more
complex over the years. Therefore, in order to alleviate some of the common
technical hurdles encounted when creating a modern Web Application, JavaScript Libraries like
AngularJS and ReactJS were created to improve Developer Experience and to speed up
Development Lifecycles.

Although most Web Developers (at least in the USA) utilize ReactJS, there are now
a plethora of Frontend JavaScript Libraries to choose from today including SvelteJS,
SolidJS, Lit, and my personal favorite, VueJS.

### What Is VueJS?

Unlike AngularJS and ReactJS, VueJS was technically not created in-house at a FAANG company,
at least not at the time of its creation. VueJS was authored by now renowned
JavaScript programmer, Evan You, who had had vast experience with Angular JS
during his prior employment at Google. His aim, in essence, was to create a
light-weight framework with an emphasis on Developer Experience and ease of use.

> "I figured, what if I could just extract the part that I really liked about Angular and build something really lightweight without all the extra concepts involved?" - Evan You

Naming his first version of the libary, Vue (after the French word for "View"), Evan released his creation on Github in 2013. Initially there was slow adoption, but after being praised by notable Developer, Taylor Otwell (author of the popular PHP web framework, Laravel), VueJS started to gain attention and popularity.

Known for it's arguably more approachable syntax, fast runtime speed, and modern Virtual DOM implementation, VueJS offers a compelling alternative to ReactJS for Frontend Web Application Development.

### Why VueJS?

It is not lost on me that ReactJS is still the King of the Roost when it comes
to JavaScript frameworks. According to [State Of JS's 2022 survey](https://2022.stateofjs.com/en-US/libraries/front-end-frameworks/), 67.9% of respondents polled they "Would Use Again" for ReactJS (1st place), with VueJS, receiving 35.7% for this same metric (2nd place). That said, in this brief section, I'll point out some of the many factors when considering whether to learn and utilize VueJS.

On the jobs front, many major companies utilize VueJS, including Facebook, Netflix, Adobe, Nintendo, Apple, BMW, and Google (sourced from [trio.dev](https://trio.dev/websites-using-vue/)). While there may not be as much demand in the US for VueJS developers as there are for ReactJS, there is still a notable demand for VueJS developers that I would argue is non-negligible.

Employment is not the sole factor one should consider when choosing a
new technology to learn (although it may be the predominant one). VueJS is often
touted as being a good "First JavaScript Framework" to learn, as it is easier to
pick up than ReactJS and has a look and feel closer to working in traditional HTML,
CSS, and JavaScript. We'll soon be covering Vue's specific formatting and syntax
in the next section.

Additionally, VueJS performs better than ReactJS in pretty much all benchmarks.
One can find up to date benchmarking results [here](https://krausest.github.io/js-framework-benchmark/index.html) as well as an article detailing them [here](https://medium.com/@danialeshete/comparative-web-performance-evaluation-benchmarking-of-vue-react-using-jswfb-a76982097225). This is achieved by VueJS's more selective use of Virtual Dom Diffing. Unlike ReactJS, a component's state is not updated <em>on each render</em>, but rather Vue updates a component's state on change of <em>only elements referenced specifically by Vue's API</em>. This is heavliy detailed in VueJS's official Documentation [here](https://vuejs.org/guide/extras/rendering-mechanism.html).

Lastly, one of the most compelling reasons I can think of to use Vue is its
<em>superb</em> documentation. ReactJS's documentation, which, while sufficient
and by no means inadequate, pales by comparison to VueJS. Indeed, if you want
to see what <em>Gold Standard Documentation</em> looks like, please [take a look for yourself](https://vuejs.org/guide/introduction.html).

### Getting Started With VueJS

VueJS's ecosystem is not quite as vast as ReactJS's, but it is by no means small.
Many of the commonly used tools a Modern Web Developer has come to expect of a
JavaScript Library exist within Vue, such as Client Side Routers
([Vue-Router](https://router.vuejs.org/)) and State Management
Libraries([Pinia](https://pinia.vuejs.org/core-concepts/state.html)),
amongst [others](https://vue-community.org/).

In the following sections, I'll be covering installing Vue's Development Environment via
[npm](https://www.npmjs.com/) and the modern development server, [Vite](https://vitejs.dev/)
(also created by Evan You, side note: you also can also use Vite for your ReactJS apps!).

I'll also introduce how Vue approaches Web Development using Components, which
is quite different from ReactJS's approach syntactically. This will include an
introduction to VueJS's Lifecycle Hooks API, which provide the Vue developer with
ways to update and manipulate Component State, and subsequently, the DOM.
Additionally, I'll also be covering Vue's built in directives, which
conditionally render HTML elements within the component based on Application
State.

I'll also cover how to pass custom attributes, commonly known as Props,
from one component (the parent) to another (the child). I'll also demonstrate
emitting events from one component to another (essentially passing props from
child components back "up" to their parent component). I'll briefly cover the related
topic of two-way data binding as it is related to this topic as well.

This hopefully will give you a general overview of VueJS, so let's get started.

### Installation
