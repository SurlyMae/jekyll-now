---
layout: post
title: What are classes?
---

_Let's talk about the different types of classes in OOP. This post still in notes mode._

Class:

- User-defined type composed of field data (i.e. member variables) and members that operate on the data (i.e. constructors, methods, properties, events)
- Collectively, the set of field data represents the state of a class instance
- Class instance = object

Classical inheritance model:

- Base classes are used to define general characteristics common to all descendants
- Subclasses extend this general functionality while adding more specific functionality

Collection classes:

- Built to dynamically resize themselves on the fly as you insert/remove items
- Nongeneric collections are designed to be loosely-typed containers
- Generic collections are much more type-safe
- Telltale sign of any generic item is the 'type parameter' i.e. List<T>
- Generics provide better performance, they are type-safe, reduce code creation
- Enum types cannot be written generically - only classes, structs, interfaces, delegates
- Generics will help manage in-memory data
