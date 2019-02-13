---
layout: post
title: What are containers?
---

_Containers seem to be the hot new term lately. What are they?_

I'm going to let the experts answer this one. Last night on Twitter, @anildash did a cool thing where he had his followers ask him what certain 'jargony' words actually mean - words like kernel, REST, API - and he explained those terms in an easy-to-understand manner. Figuring out what containers are and why someone would use them has been on my TODO list for about a month, so when I saw someone ask what docker/containers/kubernetes meant, I jumped right in there to read.

> @anildash:
> Containers are a way of making each app on a computer system think
> that it has a whole computer to itself, like putting it in a
> holodeck simulation. Docker is the most popular tool for creating
> those containers on a computer. Kubernetes manages lots of
> containers across systems.

> @surlymae:
> what are the benefits of an app thinking it has a whole computer
> to itself?

> @justinabrahms:
> You know when you're at home alone and you just kinda trash the
> place b/c why not? Apps do that. They don't clean up after
> themselves (files everywhere). They don't have to worry about
> using the bathroom (CPU) when someone else was going to use it.
> Theyve got it all to themselves

> @anildash:
> Ah! A lot of nice things, mostly for programmers & people who
> manage computers. First, It's easy to simulate the same environment
> on your computer where you're writing the code as on the eventual
> server that will run it for real.

> @anildash
> You don't have to worry about one app stepping on another. And
> then if you manage server computers, you can seamlessly move an
> app from one computer to another (or even clone a copy to another)
> and it still thinks it's in the same pristine environment.

> @GlennF
> Also great for software-defined networks and whitelist-based
> networks, in which instead of defining rules for servers and their
> services, containers have defined network routes. Dramatically
> reduces network exploit surfaces in right environments.

Sounds pretty cool, right? Got me all excited to learn about them.
