---
layout: post
title: /Notes/ JavaScript Basics
---

_Notes from reading Marijn Haverbeke's [Eloquent JavaScript](http://eloquentjavascript.net/)_

- JS uses 64 bits
- Calculations w/ fractional numbers are generally not guaranteed to be precise
- Template literal = backtick-quoted string
- Ternary = `true ? 1 : 2` = if true then 1 else 2
- Logical `||` and `&&`
    - part to right is only evaluated when necessary
    - `||` returns value to left when it can be converted to true, returns right value otherwise
    - `&&` returns value to left when it can be converted to false, returns right value otherwise

**Side effect:**
- application state change that is observable outside the called function other than its return value
- piece of code whereby a variable is created and available throughout a scope when it doesn't need to be
- network requests, I/O devices, data mutation
- changing a variable that exists outside the function, to calling another method from within a function

**Pure function:**
- Always returns same result if same arguments are passed in
- Does not depend on any state or data change during a program's execution
- Must only depend on its input arguments

**Const/let/var:**
- `const` identifier can't be reassigned
- `let` variable may be reassigned
- `let` also signals that variable will only be used in the block its defined in
- both `const` and `let` are local to the block they are declared in, while in pre-2015 JS, a `var` binding could be seen throughout the whole function
    
