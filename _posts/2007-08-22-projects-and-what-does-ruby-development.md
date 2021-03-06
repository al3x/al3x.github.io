---
title: Projects, and What Does Ruby Development Support on the Mac Really Mean?
date: 2007-08-22 00:00:00 Z
layout: post
---

Work keeps me busy. Not sleeping-under-my-desk busy, but busy enough that I’m drained at the end of the day. The thought of writing yet more code once I’ve come home is usually unappealing. This is frustrating, because I’ve had two side projects that I’ve been trying to get out the door for some time. The eldest is Peeramour, which I still intend to deliver despite having long since missed my Valentine’s Day launch date. Really, I do.

A more recent project is something I call *Quotidian*, a tagged database application for the Mac in which to store quotations. I’m not one to litter my writing, speech, and presentations with other people’s wisdom, but I like referring to relevant quotes when I’m thinking. The multi-purpose information capture applications out there like [Yojimbo](http://www.barebones.com/products/yojimbo/) or [DEVONthink](http://www.devon-technologies.com/products/devonthink/) don’t do it for me in this regard.

My secret motivation for writing Quotidian is that I’ve wanted an excuse to learn Cocoa programming for some time. Initially, I was thinking that I’d learn Objective-C in the process. I’ve since rethought this because:

None of the experienced Mac programmers I’ve talked to are particularly enthused about the language, even with the upcoming improvements in Objective-C 2.0. The consensus: “it’s fine… yeah.”

There’s no long-term value to me in learning Objective-C; I’m not about to become a full-time Mac developer, nor am I eager to maintain legacy NeXT systems. There’s nothing else one really does with Obj-C, is my impression.

There are languages I could learn that would have more value to me, or at least interest me more conceptually, and I can only fit so much in my head.

I know Ruby, and there’s [RubyCocoa](http://rubycocoa.sourceforge.net/) and [RubyObjC](http://www.rubyobjc.com/.So) last night I ran through Erik Kastner’s super handy “”Your first few days on RubyCocoa“”:http://metaatem.net/2007/05/27/your-first-few-days-on-rubycocoa tutorial, which is more like your first fifteen minutes if you have a working Ruby install. I wired up a simple interface to a Ruby controller, smiled when it all worked, and was then ready to start building something that looked like a real Mac application.

I started by looking for a way to put a toolbar in my application. That’s when I realized that you basically have to know everything about Cocoa programming in order to use something like RubyCocoa. RubyCocoa is for Cocoa programmers who want to write some stuff in Ruby, not Ruby programmers who want to take advantage of Cocoa. I’m not even sure anyone has implemented an NSToolbar with RubyCocoa (I’ll probably crib from this [PyObjC](http://www.blog.caffeinatedmacs.com/nstoolbar-tutorial/) tutorial).

I have much to learn. So this [comparative review of several Cocoa books](http://antoniocangiano.com/2007/08/21/a-preliminary-review-of-three-cocoa-and-objective-c-related-books/) caught my eye today. I sympathize with the first comment:

> “My basic test of a Cocoa book is a coherent explanation of why Interface Builder works the way it does: the Nextstep/Cocoa notion of ‘outlets’ and ‘messages’ and how IB works with them is the most confusingly counterintuitive concept Ive encountered in 32 years of programming, and most books scarcely mention it.”

Everybody’s been chirping about Apple supporting development in dynamic languages like Ruby and Python, seemingly based solely on [this page](http://developer.apple.com/leopard/overview/apptech.html) (see: “Picking Up the Pace of Cocoa Application Development”). It’s unclear, however, what form that support will take. As of yet, there’s nothing that illuminates the more oblique aspects of Cocoa development for us simple dynamic language folk. What’s more, it’s not immediately clear which of the Ruby bridges will be shipping with Leopard. While there are good community references like Tim Burks’ [RubyCocoa Resources](http://www.rubycocoa.com/), even accomplishing basic UI tasks like [displaying a sheet in a window](http://www.rubycocoa.com/ruby-external-sheets) seems like much guesswork and fiddling.

Some official guidance is necessary. Does Apple really want developers building full-fledged applications in anything but Objective-C, or is its “embrace” of dynamic languages going to be as rocky an affair as its fling with Java?
