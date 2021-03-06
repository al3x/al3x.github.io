---
title: 'C4[1]: Bob Ippolito on Exploring Erlang'
date: 2007-08-11 00:00:00 Z
layout: post
---

Speaker works for Mochi Media, which builds analytics tools for Flash developers, ad targeting systems, etc. Their applications have high concurrency needs.

Introduction
------------

Erlang is a functional language that revolves around a “process” abstraction. The language has no mutable data structures; which apparently necessitates lots of linked lists. State exists solely in the stack, so backtraces are comprehensive. A common pattern is to use accumulators that make use of tail calls (calls to another function at the end of a function). Another language feature is pattern matching, which binds variables when patterns are matched.

Types
-----

Two collection types are available: lists and tuples. Basic types include atoms (effectively a constant string, apparently quite fast to work with), binary (a contiguous chunk of bytes), integer (unbounded), float (64-bit), and ref (a unique reference across a cluster of nodes). Other data types include fun (anonymous functions, which are serialized and close over variables), pid (reference to a process, which can be on another node), port (reference to a driver, socket, pipe, and so on, much like a pid). There are no boolean, character, or string types; the above types meet these needs in various configurations.

Syntax
------

Variable start with a capital letter, and can only be assigned once (“single assignment”). Equivalency (=) is a simple form of pattern matching. Case statements can take advantage of pattern matching in more complex ways; an example of matching particular dates in given. Pattern matching is also ideal for working with file formats and a bits-and-bytes level; an example of checking for Flash files is shown. Expressions end in commas (delimit expressions), semicolons (delimits clauses), and periods (which end expressions or trigger evaluation in the shell). Anything that starts with a question mark is a compiler macro. Exclamation points mean “send a message to the left”.

Modules
-------

Modules exist in a flat namespace, and explicitly export “public” functions. Modules are referenced by name (which is an atom) and compiled to a .beam file. Erlang boasts hot code reloading, and modules take advantage of this. When declaring functions, arity (the number of variables the function takes) is noted. To compile all the modules in your project just do make:all([load]).

Processes
---------

Bob notes that Erlang processes are lightweight and fast, being neither native threads nor pthreads, but rather lightweight green threads. Processes communicate only with asynchronous messages, which they may selectively receive. Because there are no mutable variables, processes are where program state lives. Server processes are written in tail-recursive loops. Matching and logging unexpected messages is considered best practice; unhandled messages will pile up, which is effectively a memory leak.

Distributed
-----------

There’s little security between nodes; a shared secret cookie is standard. Language semantics are such that communication between nodes works just like local communication. Nodes may connect transitively. It’s fairly simple to start multiple nodes and add process monitoring. Erlang is designed around the idea that nodes will fail, and as such it’s easy to trap errors and restart nodes.

OTP
---

Originally designed for high-availability telephony, OTP is now a way of designing fault-tolerant applications in Erlang. An OTP is a tree of supervisor processes which start, monitor, and restart child processes. Also available in OTP are behaviors, which are a kind of enforced inheritance. The example of gen\_server and its conventions is shown.

Demo
----

The presentation was being given from a simple Erlang-based web server, which Bob then load tests to varying degrees, demonstrating excellent performance. Bob mentions that the networking core of Erlang is multiplexed and takes advantage of the OS-level polling features (kqueue, etc.). Performance for their app has been excellent: millions of hits per day per server.

Questions
---------

The “Programming Erlang” book is “an extremely good resource,” says Bob.
