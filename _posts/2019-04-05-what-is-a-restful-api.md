---
layout: post
title: What is a RESTful API?
---

_It's in job ads everywhere: employers looking for developers with experience in building RESTful APIs. What does REST mean and what does it take for an API to be considered RESTful?_

REST is a way to build a web service. Think of a web service as a common platform that allows communication between client and server applications. So, REST is just a way to do that! It's an architectural style, and it stands for _Representational State Transfer_. [Roy Fielding](http://roy.gbiv.com/), [who gave us REST](https://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm), explains it like this:

> "REST is intended to evoke an image of how a well-designed web app
> behaves: A network of web pages (a virtual state-machine) where the
> user progresses through an application by selecting links (state
> transitions), resulting in the next page (representing the next state > of the application) being transferred to the user and rendered for
> their use."

Here is a real-life example:

1. User opens browser (the browser is the HTTP client)
2. User points the browser to a URI (unique resource identifier)
   - the URI identifies where the resource lives
3. The browser sends an HTTP request to that URI
4. The server on the other end does some magic, then sends an HTTP response message back to the browser
   - This response message contains a **representation** of the resource the browser has requested
5. The browser interprets the representation and displays it
   - In other words, our browser (the HTTP client, remember) has changed **state**
6. The client changes _state_ depending on _representation_ of the resource we're accessing.

(The HTTP client can be a browser, but often it's an application.)

REST is defined by six constraints

REST often uses HTTP protocol
-what is http protocol?

Things that are important:
-status codes
-naming conventions
-unchanging URIs

To be truly RESTful, must implement HATEOAS
