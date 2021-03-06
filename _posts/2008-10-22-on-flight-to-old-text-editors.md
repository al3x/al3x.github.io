---
title: On The Flight to Old Text Editors
date: 2008-10-22 00:00:00 Z
layout: post
---

It’s lately become vogue in the circle of programmers I follow to discontinue use of IDEs and modern text editors like TextMate in favor of Vim and Emacs. The battlegrounds of the [editor wars](http://en.wikipedia.org/wiki/Editor_war) are now [blogs](http://weblog.jamisbuck.org/2008/10/10/coming-home-to-vim) and [Twitter](http://search.twitter.com/search?q=&amp;ors=emacs+vim+textmate), and on those media I’ve watched a number of programmers I admire return to the editors they cut their teeth on. As someone perpetually interested in how people approach the practice of programming, I’ve been considering this trend and its implications.

The first thing I did to understand why programmers are returning to the editors of yore was to do the same myself. I noticed more people flocking to Emacs than Vim, and I had less experience with Emacs, so I started there.

Emacs
-----

The experience of choosing from the three major Emacs distributions ([Aquamacs](http://aquamacs.org/), [Carbon Emacs](http://homepage.mac.com/zenitani/emacs-e.html), or the [Emacs.app you can compile yourself](http://wfarr.org/posts/14-compiling-emacs-for-os-x)) on the Mac is unpleasant enough. Aquamacs is like installing a Linux distribution with every available package: everything you need is there, but it feels slow and unpredictable. Carbon Emacs has “”Carbon“:http://en.wikipedia.org/wiki/Carbon\_API” in the name, making it all too clear that it’s destined for deprecation. My hand-compiled Emacs.app felt fast and clean, but lacked features like fullscreen editing.

Configuration for all three is handled through a mess of Mac application preference windows, customization mode pseudo-GUIs, and Elisp configuration files. I tried to accomplish as much as possible via the latter, which allowed me some flexibility in moving between the three distributions. Still, having grasped the Emacs philosophy of *configuration uber alles*, I was willing to forgive the broken mapping between Emacs and my OS’s conventions.

Over the course of my experimentation I accrued a [fairly customized Emacs setup](http://github.com/al3x/emacs/tree/master). I read [Steve Yegge’s posts](http://www.emacswiki.org/emacs/SteveYegge) about the beauty of the editor and a fair bit of similar writing. I made a serious attempt to use Emacs day-to-day, and my pinky smarted enough to prove it.

The way I described my experience with Emacs to a colleague was that I came to appreciate the *idea* of Emacs, but not the reality. It would be great to have a completely customizable editor in which my modifications were first-class citizens if that editor was, well, better than Emacs. Better OS integration. A better configuration language (nothing against Lisps, but the gripes against Elisp are myriad and the inclusion of Common Lisp a copout). Just better, through and through.

That said, my beef with Emacs is ultimately more philosophical than practical. I don’t like that Emacs is everything plus the kitchen sink. It bothers me that developers get so tied to their Emacs customizations that they build things like web browsers, mail readers, and Twitter clients into their editors. This bothers me because I value craftsmanship in software, and most of these application-like Emacs modes are crude solutions to the problems they attempt to solve. They’re deemed acceptable only because they have the feature of being Emacs-hosted and thus customized to the user’s peculiarities. They are not the Best Way To Solve The Problem Goddamit.

That it takes an advanced Emacs developer like Yegge 11,600+ lines to express a feature-rich JavaScript mode also seems worth questioning. Intuitively, it doesn’t seem like it should take 11,600+ lines of code to do this job in an expressive, high-level language calling a set of rich APIs comprising an editor “platform”. That is to say, if one had a better platform for making a highly customized editor, it should take less code.

But then, competition for such platforms isn’t exactly stiff, which is precisely why programmers are going back to Emacs from IDEs and editors like TextMate. I could be dead wrong on this point, and perhaps 11,600+ lines is a miracle of programming to get the functionality that Yegge’s [js2-mode](http://code.google.com/p/js2-mode/) offers, but with respect to his effort on the project, my suspicion is that many of those lines could/should be obviated by a better platform.

Vim
---

I’m an accomplished Vim user, but I’d never bothered to establish a working Vim setup on my Mac since TextMate’s release. So I installed [MacVim](http://code.google.com/p/macvim/) and added to it a number of customizations, including those mentioned by Jamis Buck in the post linked above that make Vim behave more like TextMate. Having played around with it for a bit, the incentive to use Vim as one’s primary editor nowadays is difficult for me to grasp. Yes, it’s familiar, but customizations in Vim feel unwieldy and bolted-on compared to those in Emacs or TextMate. Vim gets the job done, but not beautifully. There’s more habit than Zen to it. Enough said.

Dissatisfaction
---------------

At the top of my list of computing heros you’ll find [Alan Kay](http://en.wikipedia.org/wiki/Alan_Kay) and [Rob Pike](http://en.wikipedia.org/wiki/Rob_Pike). Both men have consistently strived to surpass the conventions in computing we’ve come to accept, and in that process both have experimented with other ways of approaching programming.

The [Smalltalk development tools](http://wiki.squeak.org/squeak/4) offer a tight coupling of language to development environment that allows for a far more fluid development process than most IDEs can provide. Kay frequently references the impressive applications that *children* were able to build using this intuitive approach to programming. It’s testament to a rich development that isn’t as tyrannous as an IDE.

Pike offered the <a href="http://en.wikipedia.org/wiki/Acme_(text_editor)">Acme</a> editor in the [Plan9](http://en.wikipedia.org/wiki/Plan_9_from_Bell_Labs) operating system, which follows Emacs in acknowledging that programmers will do most everything in their editor of choice, but structures both the implementation and interaction model of that editor far more rigidly. Acme has a strong sense of design. It offers conventions, rather than throwing up its hands, smiling, and saying “customize it until you like it”. Question its choice of mouse-heavy interaction, but it’s incontrovertibly an attempt to move text editing and programming into the future (of the early 1990s, admittedly, but oh how far we haven’t come since).

Glimpses of editors like these, coupled with my experiences using TextMate, make me dissatisfied with my choices when it comes to editing text. It worries me that others are seemingly not dissatisfied with the old editors, and what’s more, are content to use antiquated software that’s been strung along for decades without any serious reengineering effort or thought towards user experience. Were the situation simply old programmers using old software out of habit, I’d understand, but it’s not.

That a new generation of programmers flocking to these old tools is concerning, if for no reason more selfish than the desire for peers in my dissatisfaction. Without a consensus that we can do better, there’s no incentive, no motivation, no market for improvements. If as modest a step towards a better editor as TextMate is abandoned, what hope is there for a true leap forward?
