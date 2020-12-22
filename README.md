# Book Finder with Svelte

This repository contains a sample project to build a book finder app using [Svelte](https://svelte.dev/). 

The repository is intended for educational purpose.

The repository will guide you on how to build the app step by step. Each branch represents each step. You can walk through each branch from branch 0 to 10, or you can view the final code in the main branch.

# Installation

Before you begin, you should create a Svelte project on your own. 
```
npx degit sveltejs/template bookfinder

cd bookfinder

// install dependencies
npm install 

// or
yarn install

```

After successfully create the project, your code should look like the code in the branch [0-initial-setup](https://github.com/cahyonobagus/bookfinder-svelte/tree/0-initial-setup)

## Branches

Here is the list of the branches that will guide you to build the app: 

* [0-initial-setup](https://github.com/cahyonobagus/bookfinder-svelte/tree/0-initial-setup)

* [1-adding-css-framework](https://github.com/cahyonobagus/bookfinder-svelte/tree/1-adding-css-framework)

* [2-adding-search-box](https://github.com/cahyonobagus/bookfinder-svelte/tree/2-adding-search-box)

* [3-binding-text-input](https://github.com/cahyonobagus/bookfinder-svelte/tree/3-binding-text-input)

* [4-adding-card-book](https://github.com/cahyonobagus/bookfinder-svelte/tree/4-adding-card-book)

* [5-component-card-book](https://github.com/cahyonobagus/bookfinder-svelte/tree/5-component-card-book)

* [6-event-click-handler](https://github.com/cahyonobagus/bookfinder-svelte/tree/6-event-click-handler)

* [7-connect-to-api](https://github.com/cahyonobagus/bookfinder-svelte/tree/7-connect-to-api)

* [8-conditional-rendering](https://github.com/cahyonobagus/bookfinder-svelte/tree/8-conditional-rendering)

* [9-show-each-books](https://github.com/cahyonobagus/bookfinder-svelte/tree/9-show-each-books)

* [10-tidy-up-card-book](https://github.com/cahyonobagus/bookfinder-svelte/tree/10-tidy-up-card-book)

## What you learn

After following the steps, you should have some understanding of Svelte. Here is some knowledge that you have gained: 

* Svelte special elements (</svelte:head>)
* Text input binding and reactivity
* Creating your own svelte component
* Props
* Events Handling
* Connecting to API
* Conditional Rendering (svelte's if-else blocks)
* Loop (svelte's each blocks)


## Notes
The app uses API from [ITBook](https://api.itbook.store/). If you get some errors when accessing the bookfinder app related to CORS, please try to use a proxy or [moesif chrome extension](https://chrome.google.com/webstore/detail/moesif-origin-cors-change/digfbfaphojjndkpccljibejjbppifbc)
.
