---
layout: post
title: /Notes/ Java Optionals
---

- Introduced in Java 8
- An approach for writing methods that may not be able to return a value
- An immmutable container (immutable means unable to change)
  -> can hold a single non-null type reference or nothing at all
  -> optionals containing nothing are said to be empty
  -> the value contained in an optional is said to be present
- An optional-returning method is more flexible and easier to use than one that throws an exception, & less error-prone that one that returns null
