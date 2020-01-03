---
layout: post
title: /Notes/ Lightning Web Components (Salesforce)
---

_We've started implementing these over the last couple of months at work. Really interesting._

**LWCs:**
- Salesforce (SF) implementation of lightweight frameworks built on web standards
- Built on code that runs natively in browsers, so lightweight and delivers exceptional performance
- Most of the code written is standard JS & HTML
- Leverages custom elements, templates, shadow DOM, decorators, modules
    - custom elements
    - templates
    - shadow DOM
    - decorators
        - `@api`: makes the property public so other components can set it. If we remove `@api` the property still binds to the HTML template, but it's private
    - modules
    - directives
        - `for:each`
            - used to render an array
            - add it to the nested `<template>` tag that encloses the HTML elements you want to repeat
            - to access current item, use `for:item="currentItem`
            - to access current item's index, use `for:index="index"`
        - `iterator`
        - must use a `key` directive to assign a unique ID to each item. When a list changes, the framework uses the `key` to re-render only the item that changed.
- Provides a layer of specialized SF services on top of the core stack:
    - Base Lightning Components
        - a set of over 70 UI components all built as custom elements
    - Lightning Data Service
        - provides declarative access to SF data & metadata, data caching, and data synchronization
    - User Interface API
        - underlying service that makes Base Lightning Components and the Lightning Data Service 'metadata aware'
- Let LWCs manipulate the DOM instead of writing JS to do it.
- Use `getters` to compute a value
- When a component renders, all the expressions used in the template are evaluated, which means that getters are invoked

[LWC dev guide](https://lwc.dev/)

