---
layout: post
title: What is dependency injection?
---

_Dependency injection is a principle of object-oriented programming. But what does it actually mean?_

In the world of object-oriented programming (OOP), applications are designed using, well, objects! Everything in an app is constructed as an object, with defined attributes it has and actions it performs. These objects have to interact with each other to make the app work - for instance, Object A needs to ask Object B to do something, and therefore Object A needs to know the things Object B can do. This needing to know about other objects creates dependencies, which are necessary to a degree, but it's the way you write those dependencies into the objects that matters. You can either basically 'hardcode' the dependencies into the objects, or you can 'inject' them. Let's look at some code.

_I'm using an adapted code example from the [POODR book](https://www.poodr.com/) by [Sandi Metz](https://www.sandimetz.com/) because she is smart and awesome. I learned about dependency injection (DI) from her book and in order to do that I recreated her Ruby examples in C#, so it made sense that I would re-use those examples here._

<script src="https://gist.github.com/SurlyMae/995848ee79c86c44bc9ff2aad5c669b7.js"></script>
