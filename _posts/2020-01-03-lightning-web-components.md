---
layout: post
title: /Notes/ Lightning Web Components (Salesforce)
---

_We've started implementing these over the last couple of months at work. Interesting!_

**Summary:**
- Salesforce (SF) implementation of lightweight frameworks built on web standards
- Built on code that runs natively in browsers, so lightweight and delivers exceptional performance
- Most of the code written is standard JS & HTML
- Provides a layer of specialized SF services on top of the core stack:
    - Base Lightning Components
        - a set of over 70 UI components all built as custom elements
    - Lightning Data Service
        - provides declarative access to SF data & metadata, data caching, and data synchronization
    - User Interface API
        - underlying service that makes Base Lightning Components and the Lightning Data Service 'metadata aware'
- Let LWCs manipulate the DOM instead of writing JS to do it.
- Leverages custom elements, templates, shadow DOM, decorators, modules

**Composition:**
- Owners / containers

**Patterns:**
- Use `getters` to compute a value
- When a component renders, all the expressions used in the template are evaluated, which means that getters are invoked

**Decorators:**
- `@api`: makes the property public so other components can set it. 
- If we remove `@api` the property still binds to the HTML template, but it's private

**Directives:**
- <ins>Rendering Lists:</ins>
    - [`for:each`](https://lwc.dev/guide/html_templates#for%3Aeach)
        - used to render an array
        - add it to the nested `<template>` tag that encloses the HTML elements you want to repeat
        - to access current item, use `for:item="currentItem`
        - to access current item's index, use `for:index="index"`
    - [`iterator`](https://lwc.dev/guide/html_templates#iterator)
        - use to apply a special behavior to the first or last item in a list: `iterator:iteratorName={array}`
        - add `iterator` directive to a nested `<template>` tag that encloses the HTML elements you want to repeat
        - use `iteratorName` to access these properties:
            - value
                - the value of the item in the list
                - use this property to access the properties of the array, i.e. `iteratorName.value.propertyName`
            - index
                - the index of the item in the list
            - first
                - a boolean value indicating whether this item is the first item in the list
            - last
                - a boolean value indicating whether this item is the last item in the list
    - `key`
        - must use a `key` directive to assign a unique ID to each item. When a list changes, the framework uses the `key` to re-render only the item that changed.
            - key must be a string or number
            - can't use `index` as a value for `key`
            - assign unique keys to an incoming data set
            - to add new items to a data set, use a private property to track and generate keys
            - to assign a key to every element in the list, use the `key={uniqueId}` directive
- <u>Rendering HTML conditionally:</u>
    - [`if:true|false ={property}`](https://lwc.dev/guide/html_templates#render-html-conditionally)
        - add this directive to a nested `<template>` tag that encloses the conditional content
        - this directive binds `{property}` to the template and removes/inserts DOM elements based on whether `{property}` is truthy or falsy


[LWC dev guide](https://lwc.dev/)

