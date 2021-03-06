---
title: 'My Side-Projects: Let Me Show You Them'
date: 2008-03-17 00:00:00 Z
layout: post
---

I wrote about the value of [side-projects](http://www.al3x.net/2008/02/on-side-projects.html) back in February, in part because I had a total lack of them at the time. Shortly thereafter, that changed. Rather than picking up the side-projects I mentioned in that post, I’ve ended up spending a few spare hours on other things entirely

git-wiki!
---------

[git-wiki](http://github.com/al3x/git-wiki/tree/master) is a web-based wiki whose data store is a Git repository of plain text files. I found the original implementation by [Simon Rozet](http://atonie.org/2008/02/git-wiki) while browsing recent commits on [GitHub](http://github.com/) and got inspired.

I kicked some patches around with [Jesse Andrews](http://overstimulate.com/), and pretty soon our version was a good ways beyond where Simon started. I’ve gotten permission from Simon to fork the project under a new (ideally, sexier) name, but nothing has come to me just yet. Others are creating their own forks of git-wiki and contributing improvements, expect it to be a pretty solid wiki for personal use or small teams fairly soon. If nothing else, it’s got a simple, clean design.

Down for everyone or just me?
-----------------------------

The other day a friend Twittered “is LiveJournal down for everyone, or just me?” It was about the billionth time I’ve seen someone on a forum, IRC, IM, or Twitter ask if a site was down. See, sometimes bad things happen to good internet connections, and there’s no telling if someone upstream from you biffed the DNS server or if your destination is actually unreachable. [downforeveryoneorjustme.com](http://downforeveryoneorjustme.com/) is one trivial answer to this perennial question.

Here’s how it works: you type in a domain, we transform what you typed in to something sane, and then we do a HEAD request against “/” for that domain. If the site responds in 4 seconds, it’s up. If it doesn’t, we report that it “looks down from here”. This is, of course, totally cheesy. But it also tells you what you need to know 90% of the time.

Obviously, this is not a pro-grade monitoring solution. This is for quick, simple checks against popular domains. It gives you a quick answer and lets you go on your way, only encumbering you with some tasteful AdWords (not that I see them with my ad-blocker on). If it’s not the level of detail you’re looking for, there are a ton of tools that do geographically multi-homed monitoring, historical reports, etc.

I’ve done nothing to promote the site other than Twitter about it and put it on [my del.icio.us](http://del.icio.us/al3x) since bringing it online this past Thursday evening. In that time it’s had over 85,000 visits and over 232,000 pageviews according to Google Analytics, which is pretty much insane. It’s running off of a tiny [Gandi](http://gandi.net/) VPS and the code is a couple hundred lines (including templates) of Ruby, powered by the [Sinatra](http://sinatra.rubyforge.org/) micro web framework. I’m running four instances of the application behind [Nginx](http://nginx.net/), and save for the occasional slow request it’s been standing up pretty well (low load on the box, response times are usually fast). I’ll probably switch from serving via Mongrel to [Thin](http://code.macournoyer.com/thin/) fairly soon, once traffic has calmed down a bit.

Where Is Britt?
---------------

The future of geolocation is [here](http://whereisbritt.com/).

What I’ve Learned
-----------------

While [downforeveryoneorjustme.com](http://downforeveryoneorjustme.com/) has quickly become popular, it’s more responsibility than I really wanted out of a quick hack. If it gives someone a wrong answer, that sucks, but I don’t have the time or resources or desire to build the ideal solution. I hope that some big ISP or networking outfit takes the simple design and puts it in front of a proper setup. In the meantime, it’s novel to be making a few bucks off of AdWords, which I’ve never tried before.

Working on git-wiki is, like most developer-oriented projects I’ve spent time on, much more rewarding. Other developers are the best customers. But I’m actually spending more time hacking on it than, say, putting stuff in my personal wiki. I have the feeling that the quote-management application I’ve been dreaming of would be the same sort of affair: put hours into building it, use it for mere minutes.

Honestly, what I’ve learned is that I need a hobby that isn’t coding. I haven’t understood why so many programmers get involved with gaming when coding is, for me, really enjoyable. But it’s hard to code something worthwhile and exciting that doesn’t leave you beholden to supporting that code and its users. Really good personal projects quickly become jobs. Sometimes that’s what you want, but one job is enough for me at this point in time.

Ultimately, I’ve ended up with a quandary: how do you keep side-projects manageable?
