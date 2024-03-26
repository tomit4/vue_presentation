# VueJS

## That Other JS Framework

### On JavaScript Frameworks

The ecosystem within Web Development is perhaps the most fast past and
continually changing environment out of all Development Fields. While the
majority of Web Developers will point to their bread and butter tools like HTML,
CSS, and JavaScript as being the cornerstone necessities of their field, it would be
naive to claim that that'https://vuejs.org/guide/quick-start.htmls all one needs to know to work within Web
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

You can utilize your preferred package manager for instantiating a VueJS
project. In this demonstration we'll be using the classic Node Package Manager,
`npm`. Should you want to explore your options further, please see [Vue's
Official Quick Start Guide](https://vuejs.org/guide/quick-start.html).

Open up your preferred terminal emulator and enter the following command:

```bash
npm create vue@latest
```

The installation script will then run asking you to set up a few defults. Here
are the defaults for this sample project:

```
Vue.js - The Progressive JavaScript Framework

? Project name: > demo-project
? Add TypeScript? Yes
? Add JSX Support? No
? Add Vue Router for Single Page Application development? Yes
? Add Pinia for state management? No
? Add Vitest for Unit Testing? No
? Add an End-to-End Testing Solution? No
? Add ESLint for code quality? Yes
? Add Prettier for code formatting? Yes
? Add Vue DevTools 7 extension for debugging? (experimental) No
```

Once you've entered your defaults, it will then create a project folder with a
project folder by the name you gave it. The installation process provides you
with some instructions on how to initialize the dev server, so let's do just
that:

```bash
cd demo-project
npm install
npm run format
npm run dev
```

Once npm has finished installing the required dependencies, the dev server
should be running on your localhost, port 5173 by default. Let's take a look and
see the default page:

(insert slide_02.png here)

## The Basics

This helpful introduction page provides you with plenty of excellent
recommendations to get started, but in the interest of time. let's go over the
basics. Let's take a look at Vue's basic file structure. Those of you who have
worked in ReactJS's ecosystem might notice some similarities.

(insert slide_03.png here)

Due to the time constraints of this presentation, we'll obviously not be going
over each and every one of these files in detail, of particular interest will be
what is within our src folder. Let's open up our App.vue, clean up some
defaults, and get to work creating an Demo App that will utilize some of Vue's
basic features. Here is our App.vue in its default state:

```vue
<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
```

Those of you familiar with ReactJS might be thrown for a loop here, though
perhaps not. VueJS really embraces the concept of breaking down all aspects of
development into individualized Components. VueJS, though it can support JSX
syntax, it is usually highly discouraged. Instead a specialized file format
defined by its `.vue` extension is parsed by the Vue library. Let's take a look
at the parts of a Vue component.

Very much like a traditional HTML file, Vue files contain XML style tags that
correspond pretty much to how they would work within HTML. We have our `<script>` tag, which provides us with access to creating JavaScript (or in this case TypeScript) logic. We also have our `<template>` tag, which encapsulates the HTML. And lastly we have our `<style>` tag, which holds our CSS.

Each Vue Component's logic, structure, and stylings are encapsulated within each
component. Technically each Component's `<script>`, `<template>`, and `<style>`
sections can be ordered however you like, but this is the order VueJS
Component's default to.

In our `App.vue` component, we'll notice right away that some HTML elements
within our `<template>` section are familiar, like the `<header>` and `<img>`
tags, but that others, like our `<HelloWorld>` tag, are not. Though right away,
if you're familiar with ReactJS, you have probably already guessed that
these are other Vue Components, or in the case of the `<RouterLink>`, these act
very much like ReactJS's Page Router.

Under the `<HelloWorld>` component on line 10, you'll find there's a custom attribute
called `msg`, which is set the string, "You did it!". As you might have guessed,
these are properties being passed down to the HelloWorld component. Let's
take a look at our `<HelloWorld>` component now (under the src/components
directory):

```vue
<script setup lang="ts">
defineProps<{
  msg: string;
}>();
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
      What's next?
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
```

And here we see how VueJS's API gives access to static properties passed down to
its Child Components. On lines 2-4, we see the simple `defineProps()` method
being invoked, with the TypeScript definition of the msg property showing the
expectation of a `string` type. On line 9, we see `handlebar` or `ejs` style
syntax found in many Libraries, encapsulating our `msg` property, which indeed,
renders out the `You did it!` text of our introduction page. We of course, could
change this, and upon save, our dev server would then refresh our browser
(probably through a websockets interface), to reflect our change, but we've all
seen that, let's write some code that actually will emit an event back up to our
App.vue component, and render some text back on our Home component.

First we'll need a button that emits our event. Within our `<HelloWorld.vue>`
component, we'll write in a simple button that uses Vue's `$emit()` syntax to
emit a custom event called "showConfirmation":

```vue
<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
      What's next?
    </h3>
    <button @click="$emit('showConfirmation')">Confirm</button>
  </div>
</template>
```

We'll now return to our `App.vue` component and write some basic logic that will
render a confirmation message depending on whether we clicked this `Confirm`
button.

```vue
<script setup lang="ts">
import { ref, type Ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";

let confirmed: Ref<boolean> = ref(false);
let confirmationMsg: Ref<string> = ref("");

const confirmDidIt = () => {
  confirmed.value = true;
  confirmationMsg.value = "I sure did!";
};
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <HelloWorld @showConfirmation="confirmDidIt" msg="You did it!" />
      <p v-if="confirmed>{{ confirmationMsg }}</p>
      <p v-else>Please Confirm You Did It!</p>

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
```

Here we see some very basic aspects of working with Vue. First We pull in `ref` from
Vue. Very much like useRef from ReactJS, this simple tool creates a reference to
variables and virtual DOM elements which we can then add basic reactivity to.

We then define our related variables `confirmed`, and `confirmationMsg`, and use
the ref attribute to define their starting values as `false` and an empty
string,`''` respectively. After that we then also define a new function called
`confirmDidIt()`, which simply sets these values to `true` and `I sure did!`
respectively. Leaving our entire new script tag in our App.vue file like this:

```vue
<script setup lang="ts">
import { ref, type Ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";

let confirmed: Ref<boolean | undefined> = ref(undefined);
let confirmationMsg: Ref<string> = ref("");

const confirmDidIt = () => {
  confirmed.value = true;
  confirmationMsg.value = "I sure did!";
};
</script>
```

Lastly, we then have some new code within our template, starting with your
HelloWorld component, to which we've added a custom event, `@showConfirmation`:

```
<HelloWorld @showConfirmation="confirmDidIt" msg="You did it!" />
```

You can see here that we're essentially telling Vue, that when a custom event
called `showConfirmation` is <em>emitted</em> up from our child `<HelloWorld>` component,
to then invoke our `confirmDidIt` function. As we noticed earlier, the
`confirmDidIt` function simply changes the values that our `confirmed` and
`confirmationMsg` variables are referencing via `ref`. So what does changing
these values do? Well below our `<HelloWorld>` component, we can see that we've
also added two lines that include what Vue calls "directives", custom attributes
that in this case act like basic conditionals:

```
<p v-if="confirmed">{{ confirmationMsg }}</p>
<p v-else>Please Confirm You Did It!</p>
```

This is very readable and even to the unitiated, it is very understandable what
is going on here. To be clear though, yes, `v-if` basically checks to see if
the reference to `"confirmed"` returns a truthy value, which, if we emitted up
the `showConfirmation` event from the button in our `<HelloWorld>` component, then
the `confirmDidIt()` function fires and the values of our references change.
The `v-else` statement is there solely to render a message that asks the user
the confirm that they "did it", which genherally just indicates they should push
the button.

This is a trivial example, but it demonstrates the ease with which Vue treats
the passing of props.
