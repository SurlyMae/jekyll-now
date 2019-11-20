---
layout: post
title: /Notes/ Java Optionals
---

_Optionals are gaining popularity on my team. What are they?_

- Introduced in Java 8
- An approach for writing methods that may not be able to return a value
- An immmutable container (immutable means unable to change)
  - can hold a single non-null type reference or nothing at all
  - optionals containing nothing are said to be empty
  - the value contained in an optional is said to be present
- "An optional-returning method is more flexible and easier to use than one that throws an exception, & less error-prone that one that returns null"
- Optional.empty() returns an empty optional (duh)
- Optional.of(value) returns an optional containing the given non-null value
- Optional.ofNullable(value) accepts a possibly null value, then returns an empty optional if null is passed in
- "Optionals are similar in spirit to checked exceptions"
- Container types (maps, collections, streams, arrays, optionals) shouldn't be wrapped in optionals
- "Declare a method to return an optional if it might not be able to return a result AND clients will have to perform special processing if no result is returned"
