---
title: Getting Started with Scala and Liftweb
date: 2007-10-20 00:00:00 Z
layout: post
---

I’ve had an ongoing dilemma when sitting down to work on Peeramour. I could write the site in Rails in an afternoon, which is tempting. Thing is, I write Ruby/Rails code all day. I’m burnt out on it. Plus, I’d like to learn something new if I’m going to be programming in my off-hours.

Looking around the landscape of web application development, only one technology has really caught my eye: [Liftweb](http://liftweb.net/), a framework built with the [Scala](http://www.scala-lang.org/) language, which in turn runs on the JVM. I like that both Lift and Scala borrow successful ideas where appropriate. I like that both are built with performance, scalability, and ease of deployment in mind. Most of all, though, I like that neither Lift nor Scala is particularly sexy. It’s just ugly enough to work.

Getting started with Scala on Mac OS X 10.4 is pretty straightforward:Download either the Gzip or Bz2 Unix tarballs from the [Scala downloads page](http://www.scala-lang.org/downloads/index.html).

Unpack your tarball of choice and put it somewhere sensible like ~/src/scala.

Add the path to the bin directory to your shell’s PATH.You should now be able to run scala, type in some arithmetic expressions, that sort of thing. Hunky-dory. Now let’s get Lift-ed.

1.  If you’ve got [MacPorts](http://www.macports.org/) (and you should), do a sudo port install maven2. Maven is a build system for big honkin’ Java projects, and it takes care of grabbing dependencies and all sorts of junk.
2.  Now, grab the actual [liftweb](http://code.google.com/p/liftweb/source) source from Subversion. The packaged versions are *old*.
3.  Pop into your new liftweb directory and do a mvn install. It’ll take a few minutes while Maven grabs and builds this and that, but at the end you’ll have built all the examples and whatnot.
4.  A basic blog built in liftweb can be found in sites/hellolift. Head over there, run maven jetty:run and you can poke around at a real actual Lift app.Instructions for starting your own liftweb project can be found [at the developer’s blog](http://blog.lostlake.org/index.php?/archives/62-lift-QuickStart.html). Though that post was written in June, the invocations therein still work.

I’m used to working in TextMate, but the only [Scala bundle](http://harnly.net/2007/blog/geek/macosx/textmate-bundle-for-scala/) out there is pretty immature. I’m not after a bunch of IDE fanciness, but good syntax highlighting is a must. I imagine things are more hospitable in Eclipse, but that way perdition lies. My next step is to check out the [vim support](https://lampsvn.epfl.ch/trac/scala/browser/scala-tool-support/trunk/src/vim).

Now that I’ve got a reasonable working environment, tomorrow I’m going to take a stab at some actual code.
