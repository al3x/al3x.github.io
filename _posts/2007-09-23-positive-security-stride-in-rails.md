---
title: Positive Security Strides in Rails
date: 2007-09-23 00:00:00 Z
layout: post
---

At last year’s RailsConf Europe in London, I argued that security is a framework-level concern, and a great place for Rails to offer developers sensible, responsible conventions. Reading over the Rails changelog just now, I was thrilled to see some positive momentum in the security arena.

First of all, Rick Olsen’s [csrf\_killer plugin now comes standard in Rails](http://dev.rubyonrails.org/changeset/7592) (you can see [more work being done on the merge here](http://dev.rubyonrails.org/changeset/7596)). Edge Rails users can now decorate their controllers with a call to protect\_from\_forgery. Forms built “the Rails way” will then be secured with a hidden token. We use a similar pattern for critical actions in Twitter and it’s worked out well.

Secondly, the [sanitize, strip\_tags, and strip\_links](http://dev.rubyonrails.org/changeset/7589) helper methods are now far more robust. While Rails’s previous string sanitization was better than nothing, it let many non-trivial XSS attacks sneak by. This change should ensure that all but the most determined attackers can’t pollute your Rails-powered site with sneaky scripts.

Improvements like these go a long way towards improving the default security stance of Rails applications. It’s also an example of the rewards of framework usage: you get good stuff for free.
