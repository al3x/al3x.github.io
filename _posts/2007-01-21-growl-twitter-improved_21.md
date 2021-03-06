---
title: Growl + Twitter Improved
date: 2007-01-21 00:00:00 Z
layout: post
---

I’ve got a full-blown [Twitter](http://www.twitter.com/) addiction. There are plenty of ways to get my fix throughout the day: RSS, IM, SMS, [Twitterriffc](http://iconfactory.com/software/twitterrific), or just looking at the dang site itself.

But I’m also addicted to [Growl](http://growl.info/), the global notification system for Mac OS X (that Apple *should* be shipping with Leopard, cough). Throughout the day I have all sorts of data pouring across the bottom of my screen thanks to Growl, from incoming emails to IM status messages to completed downloads. Twitter updates would fit right in!

I’m not the first guy to have this idea. Matt Bidulph of [Hackdiary](http://www.hackdiary.com/) put together a clever, terse [Ruby script](http://www.hackdiary.com/src/twitter-monitor.rb) that does the job. Unfortunately, Matt’s script is a bit lacking in the features department.

So I’m breaking you off a piece of the remix with my own [twitter\_monitor.rb](http://code.al3x.net/svn/scraps/twitter_monitor.rb). It uses the absolute latest [Twitter Ruby gem](http://twitter.rubyforge.org/) from [John Nunemaker](http://addictedtonew.com/), which includes a lil patch from me to grab the full spectrum of data available from [Twitters API](http://twitter.com/help/api).

My script adds the following features to Matt’s original:

-   Retrieval, caching, refreshing, and display of your friends user icons.
-   Use of `~/.twitter` to store your username and password, as per the Twitter gem.
-   Daemonization to work around Growls strained relationship with `cron` (see the [Growl forum](http://forums.cocoaforge.com/viewforum.php?f=6) for more on this).
-   Error checking all over the place to survive network failures, etc.

You’ll want to `sudo gem install twitter daemons` and make sure that `growlnotify` is being called from the right path before you fire this thing up. Once you do, expect a warm fuzzy feeling every 15 minutes (or whenever you set it for) as your friends’ latest musings float by.

Ahh. Twitter.
