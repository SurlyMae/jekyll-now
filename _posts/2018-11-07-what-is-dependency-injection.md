---
layout: post
title: What is dependency injection?
---

_Dependency injection is a principle of object-oriented programming. But what does it actually mean?_

In the world of object-oriented programming (OOP), applications are designed using, well, objects! Everything in an app is constructed as an object, with defined attributes it has and actions it performs. These objects have to interact with each other to make the app work - for instance, Object A needs to ask Object B to do something, and therefore Object A needs to know the types of things Object B can do. This needing to know about the details of other objects creates dependencies, which are necessary to a degree, but when objects know too much about each other it can create issues. If Object A is designed and built around the way it's expected to interact with Object B, then Object A can't easily be re-used to interact with Object C. And when Object B is changed, if Object A is too tightly intertwined, Object A will have to change too. Objects designed like this become a problem for developers: A change to the app is requested and the change will take much longer than it should, or will be so difficult that it's determined the change isn't possible. That's not how we want our applications to be, is it? We want to be able to move quickly on changes and give the app users what they need and want.
