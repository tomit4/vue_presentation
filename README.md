<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/logo.svg"/>
</div>

<h1 align="center">VueJS</h1>

<h2 align="center">The Other JS Framework</h1>

### Introduction

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

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/slide_02.png"/>
</div>

### The Basics

This helpful introduction page provides you with plenty of excellent
recommendations to get started, but in the interest of time. let's go over the
basics. Let's take a look at Vue's basic file structure. Those of you who have
worked in ReactJS's ecosystem might notice some similarities.

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/slide_03.png"/>
</div>

### The .vue file

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

### Props, Emits, and Refs

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

Let's take a look at our simple custom event in action:

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/slide_04.gif"/>
</div>

### Two Way Bindings

As simple as the passing of props and emitting custom events was to implement,
Vue provides another directive called `v-model` which allows us to
essentially do the same with less syntax. In this section, let's build out a
basic form within a child component, where our parent component, App.vue, will have a
basic text element that will change whenever our form input changes.

Starting with App.vue:

```vue
<script setup lang="ts">
// ...
const input = defineModel({ default: "inputString" });
// ...
</script>

<template>
  <HelloWorld
    v-model="input"
    @showConfirmation="confirmDidIt"
    msg="You did it!"
  />
  <br />
  <input v-model="input" />
</template>
```

And also our child component, HelloWorld.vue:

```vue
<script setup lang="ts">
//...
const input = defineModel();
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h2>{{ input }}</h2>
    <br />
  </div>
</template>
```

These snippets are simplified to highlight the code relevant to the subject of Vue's two-way data binding.
We first utilize the Vue's `defineModel()` macro in each component. Within the parent component, `App.vue`, we establish a default value of "inputString". Within our template, we then "bind" this input variable to our `<HelloWorld>` component as well as our new `<input>` element using the `v-model` syntax. In essence, this is a form of syntactical sugar over the creationg of refs, props, and emits between a parent and child component, allowing each component to "see" this particular data and display it on the page.

This allows whatever we type into our new input field in our App.vue parent
component to be rendered in our child `HelloWorld.vue` component. As before, this is a
trivial example, but it demonstrates Vue's emphasis on giving developers
multiple tools to create reactivity within their components in an easy and
flexible fashion.

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/slide_05.gif"/>
</div>

### LifeCycle Hooks

VueJS gives Developers access to various LifeCycle Hook Methods, which allows
them to inject custom logic at various times during the lifecycle of each
Component. Sometimes this is to ensure certain custom directives are loaded
prior to the component loading. Other times, the Developer might wish to ensure
a certain function cleans up some data (like localStorage or cookies) prior to
or after a component loads, or is "mounted".

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/vue_lifecycle_hooks.png"/>
</div>

As this is a simple introduction to Vue, I won't be covering each lifecycle
hook in detail, and rather will leave you with the specific documentation
[here](https://vuejs.org/guide/essentials/lifecycle.html).

Instead, I'll provide you with a brief demonstration of Vue's `onMounted()`
LifeCycle method, which, according to the [official docs](https://vuejs.org/api/composition-api-lifecycle.html#onmounted), is typically used for performing side effects that need access to the component's rendered DOM.

In the following demonstration, I'll be using a fake REST API called [jsonplaceholder](https://jsonplaceholder.typicode.com/) to bring in some fake data about users and render it on the page.

Because I want this to happen as soon as the child component loads (i.e. is Mounted), I'll be using a classic JavaScript method, `fetch()` within vue's `onMounted()` lifecycle method to pull in this data from the API and then performing logic to render it nicely in our component. Additionally, I'll also demonstrate the very useful `v-for` directive, which works akin to how `map` works within ReactJS's JSX syntax.

### Demo Project

Firstly, let's clean up our App.vue file so that we can clearly demonstrate
this. We'll solely keep the Vue Logo, and greatly simplify the stylings. We'll
keep first child component, HelloWorld, more or less the same, only passing the
props `msg` as the value, "Demo Project", to be rendered within our
`<HelloWorld>` component:

```vue
<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/logo.svg"
        width="125"
        height="125"
      />
      <HelloWorld msg="Demo Project" />
      <br />
    </div>
  </header>
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

.wrapper {
  margin: 0 auto;
}
</style>
```

Not much we haven't seen already, let's move on. Here in our `<HelloWorld.vue>`
component, we've greatly changed around things to demonstrate the `onMounted()`
hook. Let's break down the `<script>` and `<template>` parts of our component.

```vue
<script setup lang="ts">
import { ref, type Ref, onMounted } from "vue";
import UserCard from "../components/UserCard.vue";

defineProps<{ msg: string }>();

const users: Ref<Array> = ref([]);

onMounted(async (): Promise<void> => {
  try {
    const res = await fetch("https://jsonplaceholder.typicode.com/users", {
      method: "GET",
    });
    if (!res.ok) {
      throw new Error("ERROR while grabbing users from jsonplaceholder");
    }
    const jsonRes = await res.json();
    users.value = jsonRes;
  } catch (err) {
    if (err instanceof Error) console.error(err.message);
  }
});
</script>
```

You'll notice right away that we've introduced a new component `<UserCard>`: You'll
also notice we now bring in the onMounted hook. As mentioned earlier, the
`onMounted()` hook encapsulates custom logic that runs after the component has
been "mounted", meaning that its virtual DOM nodes have been loaded into the
virtual DOM has been created and then inserted into it's parent component's
virtual DOM. If this sounds confusing, don't worry too much about it,
essentially it simply means it runs whenever this component loads.

You'll also notice that we create a new `ref`, into which we instantiate a new
Array object.

Within the `onMounted()` hook, we utilize the native fetch API to create a
simple HTTP GET request to the url,
`https://jsonplaceholder.typicode.com/users`. This simple JSON API is a
toy REST API which returns various dummy JSON data. In this case, if
queried via HTTP GET, this URL endpoint returns this JSON:

```json
[
  {
    "id": 1,
    "name": "Leanne Graham",
    "username": "Bret",
    "email": "Sincere@april.biz",
    "address": {
      "street": "Kulas Light",
      "suite": "Apt. 556",
      "city": "Gwenborough",
      "zipcode": "92998-3874",
      "geo": {
        "lat": "-37.3159",
        "lng": "81.1496"
      }
    },
    "phone": "1-770-736-8031 x56442",
    "website": "hildegard.org",
    "company": {
      "name": "Romaguera-Crona",
      "catchPhrase": "Multi-layered client-server neural-net",
      "bs": "harness real-time e-markets"
    }
  },
  {
    "id": 2,
    "name": "Ervin Howell",
    "username": "Antonette",
    "email": "Shanna@melissa.tv",
    "address": {
      "street": "Victor Plains",
      "suite": "Suite 879",
      "city": "Wisokyburgh",
      "zipcode": "90566-7771",
      "geo": {
        "lat": "-43.9509",
        "lng": "-34.4618"
      }
    },
    "phone": "010-692-6593 x09125",
    "website": "anastasia.net",
    "company": {
      "name": "Deckow-Crist",
      "catchPhrase": "Proactive didactic contingency",
      "bs": "synergize scalable supply-chains"
    }
  },
  {
    "id": 3,
    "name": "Clementine Bauch",
    "username": "Samantha",
    "email": "Nathan@yesenia.net",
    "address": {
      "street": "Douglas Extension",
      "suite": "Suite 847",
      "city": "McKenziehaven",
      "zipcode": "59590-4157",
      "geo": {
        "lat": "-68.6102",
        "lng": "-47.0653"
      }
    },
    "phone": "1-463-123-4447",
    "website": "ramiro.info",
    "company": {
      "name": "Romaguera-Jacobson",
      "catchPhrase": "Face to face bifurcated interface",
      "bs": "e-enable strategic applications"
    }
  },
  {
    "id": 4,
    "name": "Patricia Lebsack",
    "username": "Karianne",
    "email": "Julianne.OConner@kory.org",
    "address": {
      "street": "Hoeger Mall",
      "suite": "Apt. 692",
      "city": "South Elvis",
      "zipcode": "53919-4257",
      "geo": {
        "lat": "29.4572",
        "lng": "-164.2990"
      }
    },
    "phone": "493-170-9623 x156",
    "website": "kale.biz",
    "company": {
      "name": "Robel-Corkery",
      "catchPhrase": "Multi-tiered zero tolerance productivity",
      "bs": "transition cutting-edge web services"
    }
  },
  {
    "id": 5,
    "name": "Chelsey Dietrich",
    "username": "Kamren",
    "email": "Lucio_Hettinger@annie.ca",
    "address": {
      "street": "Skiles Walks",
      "suite": "Suite 351",
      "city": "Roscoeview",
      "zipcode": "33263",
      "geo": {
        "lat": "-31.8129",
        "lng": "62.5342"
      }
    },
    "phone": "(254)954-1289",
    "website": "demarco.info",
    "company": {
      "name": "Keebler LLC",
      "catchPhrase": "User-centric fault-tolerant solution",
      "bs": "revolutionize end-to-end systems"
    }
  },
  {
    "id": 6,
    "name": "Mrs. Dennis Schulist",
    "username": "Leopoldo_Corkery",
    "email": "Karley_Dach@jasper.info",
    "address": {
      "street": "Norberto Crossing",
      "suite": "Apt. 950",
      "city": "South Christy",
      "zipcode": "23505-1337",
      "geo": {
        "lat": "-71.4197",
        "lng": "71.7478"
      }
    },
    "phone": "1-477-935-8478 x6430",
    "website": "ola.org",
    "company": {
      "name": "Considine-Lockman",
      "catchPhrase": "Synchronised bottom-line interface",
      "bs": "e-enable innovative applications"
    }
  },
  {
    "id": 7,
    "name": "Kurtis Weissnat",
    "username": "Elwyn.Skiles",
    "email": "Telly.Hoeger@billy.biz",
    "address": {
      "street": "Rex Trail",
      "suite": "Suite 280",
      "city": "Howemouth",
      "zipcode": "58804-1099",
      "geo": {
        "lat": "24.8918",
        "lng": "21.8984"
      }
    },
    "phone": "210.067.6132",
    "website": "elvis.io",
    "company": {
      "name": "Johns Group",
      "catchPhrase": "Configurable multimedia task-force",
      "bs": "generate enterprise e-tailers"
    }
  },
  {
    "id": 8,
    "name": "Nicholas Runolfsdottir V",
    "username": "Maxime_Nienow",
    "email": "Sherwood@rosamond.me",
    "address": {
      "street": "Ellsworth Summit",
      "suite": "Suite 729",
      "city": "Aliyaview",
      "zipcode": "45169",
      "geo": {
        "lat": "-14.3990",
        "lng": "-120.7677"
      }
    },
    "phone": "586.493.6943 x140",
    "website": "jacynthe.com",
    "company": {
      "name": "Abernathy Group",
      "catchPhrase": "Implemented secondary concept",
      "bs": "e-enable extensible e-tailers"
    }
  },
  {
    "id": 9,
    "name": "Glenna Reichert",
    "username": "Delphine",
    "email": "Chaim_McDermott@dana.io",
    "address": {
      "street": "Dayna Park",
      "suite": "Suite 449",
      "city": "Bartholomebury",
      "zipcode": "76495-3109",
      "geo": {
        "lat": "24.6463",
        "lng": "-168.8889"
      }
    },
    "phone": "(775)976-6794 x41206",
    "website": "conrad.com",
    "company": {
      "name": "Yost and Sons",
      "catchPhrase": "Switchable contextually-based project",
      "bs": "aggregate real-time technologies"
    }
  },
  {
    "id": 10,
    "name": "Clementina DuBuque",
    "username": "Moriah.Stanton",
    "email": "Rey.Padberg@karina.biz",
    "address": {
      "street": "Kattie Turnpike",
      "suite": "Suite 198",
      "city": "Lebsackbury",
      "zipcode": "31428-2261",
      "geo": {
        "lat": "-38.2386",
        "lng": "57.2232"
      }
    },
    "phone": "024-648-3804",
    "website": "ambrose.net",
    "company": {
      "name": "Hoeger LLC",
      "catchPhrase": "Centralized empowering task-force",
      "bs": "target end-to-end models"
    }
  }
]
```

As long as our `fetch()` is successful, we then assign our `users` `ref` this
data on line 17:

```
const jsonRes = await res.json()
users.value = jsonRes
```

Great! We've got our user data as soon as this `<HelloWorld>` component mounts!
Let's now move onto our `<template>` tag and see how we then send this data down
and render each object individually using the `v-for` directive:

```vue
<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
  </div>
  <div class="users-wrapper" :key="user.id" v-for="user in users">
    <UserCard
      class="user-element"
      :id="user.id"
      :name="user.name"
      :username="user.username"
      :street="user.address.street"
      :suite="user.address.suite"
      :city="user.address.city"
      :zipcode="user.address.zipcode"
      :lat="user.address.geo.lat"
      :lng="user.address.geo.lng"
      :phone="user.phone"
      :website="user.website"
      :companyName="user.company.name"
      :catchPhrase="user.company.catchPhrase"
      :bs="user.company.bs"
    />
  </div>
</template>
```

Specifically, let's break down what's happening with this `v-for` loop, although
it is more or less self-explanatory. Very much like the common use of `map()`
within React JSX, we can iterate over values returned from Vue's `ref` attribute using
Vue's `v-for` directive. This `v-for` works pretty much the same way that
JavaScript's [for...in loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in).

```
<div class="users-wrapper" :key="user.id" v-for="user in users">
```

Should you desire to reference the index, by the way, you can do so like this:

```
<div v-for="(item, index) in items"></div>
```

Or if you wish to iterate an object instead of an array, you have a few options
there as well:

```
<div v-for="(value, key) in object"></div>
<div v-for="(value, name, index) in object"></div>
```

The `:key="user.id"` syntax might be familiar to you if you are coming from the
ReactJS ecosystem. In both VueJS and ReactJS, whenver looping over objects or
arrays, a <em>unique</em> key must be set to ensure that unexpected behavior
does not occur and the Virtual DOM does not inadvertently destroy data passed to
it when a re-render of our component occurs. This can happen when some other
part of our component's state changes, but the majority of it remains the same.

These unique keys keep a sort of record that holds onto the state of our data, ensuring
that the Virtual DOM does not re-render or destroy data related to state that
has not changed. Note that you may be tempted to use the `index` of an array as
the key when this occurs. <em>Do NOT do this</em>, as Array ordered indexes can
change when data is dynamically rendered (like when pulling in an API). Usually
some other unique identifier is provided via any well designed API, like in this
case, where we utilize the `user.id` as our key.

Finally, within our `v-for` loop, we pass the `ref`, `users` array down into our custom `<UserCard>` component. To recap briefly, recall that this array was popualted by calling `fetch()` within Vue's `onMounted()` hook.

Note that within our `<UserCard>` component, we also introduce a new
vue-directive, though it may not be apparent. Note the syntax here with each of
our data points:

```
<UserCard
  class="user-element"
  :id="user.id"
  :name="user.name"
  :username="user.username"
  :street="user.address.street"
  :suite="user.address.suite"
  :city="user.address.city"
  :zipcode="user.address.zipcode"
  :lat="user.address.geo.lat"
  :lng="user.address.geo.lng"
  :phone="user.phone"
  :website="user.website"
  :companyName="user.company.name"
  :catchPhrase="user.company.catchPhrase"
  :bs="user.company.bs"
/>
```

The colon followed by data name is a shorthand for the `v-bind` directive, which
is a commonly used Vue directive that allows us to pass "dynamic" props to a
child component. It technically can also be utilized like this:

```
<UserCard
  class="user-element"
  v-bind:id="user.id"
  v-bind:name="user.name"
  v-bind:username="user.username"
  v-bind:street="user.address.street"
  v-bind:suite="user.address.suite"
  v-bind:city="user.address.city"
  v-bind:zipcode="user.address.zipcode"
  v-bind:lat="user.address.geo.lat"
  v-bind:lng="user.address.geo.lng"
  v-bind:phone="user.phone"
  v-bind:website="user.website"
  v-bind:companyName="user.company.name"
  v-bind:catchPhrase="user.company.catchPhrase"
  v-bind:bs="user.company.bs"
/>
```

But due to how common this directive is utilized in the Vue ecosystem, the
creators of Vue shortened how to instantiate the v-bind directive. Let's move
onto our final component where we can see how each `<UserCard>` component
utilizes the data:

```vue
<script setup lang="ts">
defineProps<{
  id: number;
  name: string;
  username: string;
  street: string;
  suite: string;
  city: string;
  zipcode: string;
  lat: string;
  lng: string;
  phone: string;
  website: string;
  companyName: sring;
  catchPhrase: string;
  bs: string;
}>();
</script>

<template>
  <div class="user-card">
    <p><em>id:</em> {{ id }}</p>
    <p><em>Name:</em> {{ name }}</p>
    <p><em>UserName:</em> {{ username }}</p>
    <p><em>Address:</em> {{ street }}</p>
    <p><em>Suite:</em> {{ suite }}</p>
    <p><em>City:</em> {{ city }}</p>
    <p><em>ZipCode:</em> {{ zipcode }}</p>
    <p><em>Latitude:</em> {{ lat }}</p>
    <p><em>Longitude:</em> {{ lng }}</p>
    <p><em>PhoneNumber:</em> {{ phone }}</p>
    <p><em>WebSite:</em> {{ website }}</p>
    <p><em>CompanyName:</em> {{ companyName }}</p>
    <p><em>CatchPhrase:</em> {{ catchPhrase }}</p>
    <p><em>BS:</em> {{ bs }}</p>
  </div>
</template>

<style scoped>
.user-card {
  text-align: left;
  font-size: 22.5px;
  color: #34495e;
  overflow: scroll;
  text-wrap: nowrap;
}
.user-card > p {
  font-weight: 400;
}
em {
  font-weight: 500;
}
</style>
```

As you can see, there really isn't too much going on here that we haven't
covered already. We invoke `defineProps()` to get access to the data we bound
using the `v-bind` directive in the `<HelloWorld>` parent component.

As an aside, note that the majority of the text around `defineProps()` is
related to TypeScript (in JavaScript, we'd simply invoke the `defineProps()` API
and call it a day).

```vue
<script setup lang="ts">
defineProps<{
  id: number;
  name: string;
  username: string;
  street: string;
  suite: string;
  city: string;
  zipcode: string;
  lat: string;
  lng: string;
  phone: string;
  website: string;
  companyName: sring;
  catchPhrase: string;
  bs: string;
}>();
// in JS: defineProps();
</script>
```

Having access to these props, we can then simply populate our `<template>` with
the props data using the ejs handlebars syntax:

```vue
<template>
  <div class="user-card">
    <p><em>id:</em> {{ id }}</p>
    <p><em>Name:</em> {{ name }}</p>
    <p><em>UserName:</em> {{ username }}</p>
    <p><em>Address:</em> {{ street }}</p>
    <p><em>Suite:</em> {{ suite }}</p>
    <p><em>City:</em> {{ city }}</p>
    <p><em>ZipCode:</em> {{ zipcode }}</p>
    <p><em>Latitude:</em> {{ lat }}</p>
    <p><em>Longitude:</em> {{ lng }}</p>
    <p><em>PhoneNumber:</em> {{ phone }}</p>
    <p><em>WebSite:</em> {{ website }}</p>
    <p><em>CompanyName:</em> {{ companyName }}</p>
    <p><em>CatchPhrase:</em> {{ catchPhrase }}</p>
    <p><em>BS:</em> {{ bs }}</p>
  </div>
</template>
```

And that's it. Here is what our final output looks like:

<div align="center">
    <img src="https://raw.githubusercontent.com/tomit4/vue_presentation/main/assets/slide_06.gif"/>
</div>

### Conclusion

In truth, we have only really scratched the surface of what VueJS has to offer.
We didn't even cover the Page Router([Vue-Router](https://router.vuejs.org/)), the State Manager, [Pinia](https://pinia.vuejs.org/core-concepts/state.html), or the Meta Framework, [Nuxt](https://nuxt.com/).

Keep in mind that Vue is now on its 3rd version, and very much like ReactJS,
there are <em>significant</em> differences between versions, so should you
choose to use Vue, I highly recommend you use Vue3, as Vue2 is deprecated,
and it utilizes a less ergonomic syntax (i.e. always work with the Composition
API, and use the "setup" option with the `<script>` tags by default). As always,
be discerning when looking into documentation that is over a year old. Like
other JavaScript frameworks, VueJS's ecosystem moves rapidly and changes
quickly. They have recently been experimenting with a new "Vapor" mode that
will allow Developers to experiment with direct JavaScript compilation
instead of working with a Virtual DOM. This is very much taking inspirations
from both the SvelteJS JavaScript library, and in my opinion holds great
potential for the future of Frontend Web Development.

As mentioned earlier, it is not lost on me that ReactJS is the defacto standard
in the JavaScript framework ecosystem at this time. And while I do appreciate
all that ReactJS has done to advance this aspect of Web Development further,
there are a great number of JavaScript frameworks out there that offer up
different approaches to handling classic Front End Web Development
challenges. VueJS, while my personal favorite, is just one of them, and I'd
invite you to take a look at others (SvelteJS takes a lot of inspiration
stylistically from VueJS, and SolidJS remains the most performant of all
the modern frontend JavaScript frameworks currently).

#### Other Vue Related Resources

I invite you to look into VueJS, and it's large ecosystem which includes their:

- [Jobs Board](https://vuejobs.com/?ref=vuejs)
- [Discord Channel](https://discord.com/invite/HBherRA)

And of course, you can find more out at their [Official Website](https://vuejs.org/).
