---
layout: post
title: What are automatic properties in C#?
---

`public int Name { get; set; }`
_Ever seen C# code like this and wondered what's going on? I've got you covered._

One of the pillars of object-oriented programming (OOP) is encapsulation. We can think of encapsulation in two ways: First, when we're designing classes, how do we 'hide' the details of the code from those who don't need to see it? And second, how do we protect the data belonging to each object?

Let's look at a traditional way of implementing encapsulation.

<script src="https://gist.github.com/SurlyMae/77770f5492632387a089a3538d579654.js"></script>

Here, each gear object has its own chainring and cog. We declare these as private so that other objects can't access them directly. Then we provide public methods for getting and setting the chainring and cog values - now other objects can access the information, but in a way that the gear object controls.
