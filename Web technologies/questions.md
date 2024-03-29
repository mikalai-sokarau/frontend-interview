### What are web components and how do they work?

Web Components is a set of different technologies allowing you to create reusable custom elements — with their functionality encapsulated away from the rest of your code — and utilize them in your web apps.

Web Components consist of three main technologies:
- **Custom elements:** A set of JavaScript APIs that allow you to define custom elements and their behaviour, which can then be used as desired in your user interface.
- **Shadow DOM:** A set of JavaScript APIs for attaching an encapsulated "shadow" DOM tree to an element — which is rendered separately from the main document DOM — and controlling associated functionality. In this way, you can keep an element's features private, so they can be scripted and styled without the fear of collision with other parts of the document.
- **HTML templates:** The `<template>` and `<slot>` elements enable you to write markup templates that are not displayed in the rendered page. These can then be reused multiple times as the basis of a custom element's structure.
