---
title: The Cost of Privacy in Social Web Applications
date: 2007-09-22 00:00:00 Z
layout: post
---

Part of the sign-up process for most any social networking site is a privacy option: do you want the whole world to see your presence on this particular site, or just a handful of people that you select? This simple option illustrates a fascinating intersection between technology and social interaction.

The most basic action you can perform on a social network is getting a list of people. For computers, fulfilling a request for such a list is easy: ask the database for a list of *n* people, hand that list back to the web application to be processed and formatted, and send back some HTML to the user’s browser. In many circumstances, this list is easily cached, making it a snap to serve millions of users per day. More pages served means more potential ads clicked, and that means more money.

Privacy mucks this happy scenario up. Ask for a list of users on a social network with privacy controls and you’re kicking off a complex series of computations behind the scenes. The database can’t just retrieve a simple list when privacy is in the mix. Instead, it has to jump around its tables of data figuring out who’s allowed to see who. The web application now has to provide different decorations to denote the private users, so you need extra logic and some new icons. Everything just got twice as hard: harder for the machines, harder for the programmer, harder for the designer, and (before this was a common UI pattern) conceptually harder for the user.

It wouldn’t be a stretch to say that most social networks are conceived of, designed, and developed by young men (see Facebook, MySpace, Friendster, LiveJournal, Twitter, &c.). Young men have nothing to gain from online privacy. If you’re young and male, the online world is your oyster: you can build a reputation, find new relationships, and share your opinions in what’s historically been a culture of your peers. The only reason to “go private” if you’re young and male is if you’re already hugely successful offline; movie stars and rappers have nothing to gain from being *your* virtual buddy once they’ve blown up, but they probably want to stay in touch with their friends.

Thankfully, the social web isn’t comprised solely of young men. This makes online communities more diverse and engaging, and that diversity is essential for both the survival and monetization of those communities. That said, it’s the people who aren’t young men who usually want privacy: women afraid of being stalked, older users uninterested in expanding their social networks, or everyday misanthropic curmudgeons like my [coworker Jeremy](http://twitter.com/jeremy). Private users present a paradox for social networks: you can’t serve with ’em, but you can’t survive with ’em.

I’ve been thinking about this paradox for some time, as [Peeramour](http://peeramour.com/) - the site I’ve been conceiving of in my free time for over two years - is an experiment in online social openness. Peeramour doesn’t have a conceptual place for private users, yet it requires a diverse demographic to succeed. My hope is that the potential social benefit of the site is enough of an incentive to draw those private users out of their shells, but it’s a tricky business.
