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

**Scope:**
- scopes can look out into the scope around it, can't look in
- if multiple bindings have same name however, only innermost one can be seen. Example:
```
const halve = function(n) { return n/2 }
let n = 2
halve(100) = 50
console.log(n) logs 10
```

**Lexical scoping:**
- Describes how a parser resolves variable names when functions are nested
- the word lexical refers to the fact that lexical scoping uses the location where a variable is declared to determine where that variable is available
- Actual definition of lexical:
    - "of or relating to words or the vocab of a language as distinguished from its grammar and construction"
    - "a dictionary provides lexical information, it tells you what a words means and not all there is to know about that word"
- So we could say lexical is about how the word (variable) relates to the words (code) around it. Lexical scoping is like the context of a variable. What is the variable's meaning here, in this context? Visible. What is its meaning in this other context? Not useable.

**Callstack:**
- Because a function has to jump back to the place that called it when it returns, the computer must remember the context from which the call happened.
- Context is stored in the callstack.
- Every time a function is called, the current context is stored on top of this stack.
- When a function returns, it removes the top context from the stack and uses that context to continue execution.

**Closures:**
- combination of a function and the lexical environment within which that function was declared
- This environment consists of any local variables that were in scope at the time the closure was created
- kind of like referring to an instance of an inner function created when outer function is ran. The instance of the inner function maintains a reference to its lexical environment.
- Closure recipe:
    1. Create your parent function (i.e. the `checkScope` function)
    2. Define some variables in the parent's local scope (can be accessed by child function) (i.e. `var innerVar = "local scope"`)
    3. Define a function inside the parent function. this is a child (i.e. the `innerFunc` function)
    4. Return that function from inside the parent function (i.e. `return innerFunc`)
    ```
    function checkScope() {
        var innerVar = "local scope"
        function innerFunc() {
            return innerVar
        }
        return innerFunc
    }
    ```
    
