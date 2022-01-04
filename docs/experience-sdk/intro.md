---
title: Intro
sidebar_position: 0
---

Welcome to the Wyng JS API reference!

The API consists of two major components:
- Action Dispatcher
- Event Listener

The Wyng JS API allows developers to programmatically interact with drag and drop
campaigns through a global `wyng` object. You can write custom javascript that
dispatches an action or registers a callback function for a given event.

The Wyng JS API, or SDK, is located at the `window` level and scoped by experience ID.
The methods can be accessed through `window.wyng['YOUR EXPERIENCE ID']`.
For convenience, when inserting javascript through the "Custom Javascript" of the campaign, you may use the `_WYNG_ID_` tag and it will automatically be replaced with the active experience ID.

It is also recommended to scope your custom code with an [Immediately-Invoked Function Expression](https://developer.mozilla.org/en-US/docs/Glossary/IIFE) to avoid potential side-effects when embeding the experience on a page that already has some JavaScript in it.

All in all a good starting point would look something like this:

``` javascript
(function() {
    const sdk = window.wyng['_WYNG_ID_'];
    // YOUR CUSTOM JAVASCRIPT
})();
```