---
title: Don't Be A Hero
date: 2010-01-09 00:00:00 Z
layout: post
---

My [last work-related post](http://al3x.net/2009/12/06/criticism.html), regarding the difference between criticism and negativity in the workplace, was well-received. I don’t plan on this turning into Yet Another Business Advice Blog, but I figured I’d share one of the scant few other things I’ve figured out so far in my time working in tech.

The Hero
--------

Every team I’ve ever worked on has had a hero. You’ve probably worked with one too: the guy or gal eager and willing to pull all-nighters, work weekends, and take over on-call duty when nobody else wants to.

Of course, everyone appreciates the hero. Her efforts are more tangible than the rest of the team’s. Everyone else is writing code, sure, but the hero is writing code *at the office at four in the morning*. That’s real, real in a way that a bunch of commits from the rest of the team aren’t, real in a way that’s particularly visible to managers. The hero is celebrated. The hero is a role model.

Here’s the thing: the hero is the most damaging person on a team, particularly on a team that’s supposed to be writing high-availability or otherwise mission-critical software.

Why The Hero Undermines Everyone Else
-------------------------------------

If you’ve built a system that’s supposed to be reliable, you shouldn’t be up fixing it at four in the morning. You shouldn’t be getting paged at all hours. Sure, you might need to do some occasional planned after-hours maintenance, or some very occasional unplanned-but-process-driven disaster recovery, but you *shouldn’t need a hero*.

Heroes are damaging to a team because they become a crutch. As soon as you have someone who’s always willing to work at all hours, the motivation from the rest of the team to produce reliable, trouble-free software drops. **The hero is a human patch.** Sure, you might sit around talking about how reliability is a priority, but in the back of your mind you know that the hero will be there to fix what doesn’t work.

Relying on the hero to make up for poor software reliability might be a reasonably cost-effective (if cynical) strategy if it weren’t for heroism being *utterly unsustainable*. Nobody can pull heroic hours for long. Heroes get sick. They get burnt out. Eventually, the hero resents the rest of the team for not pulling their weight, and rightly so: if your team is relying on a hero, they’re not doing their jobs.

Why You Shouldn’t Be A Hero
---------------------------

I’m willing to bet that everyone reading this has probably *been* the hero at one time or another. If you love what you do, it’s inevitable that you’ll want to pull late hours and help out. In moderation, there’s nothing wrong with that.

If you’re carrying the rest of your team through heroism, though, it’s time for a change. Ultimately, by playing the hero, you’re shortchanging yourself, your coworkers, and your customers:

-   By playing the hero, you shortchange yourself by maintaining an unhealthy work-life balance. You may love your work, but you can’t do nothing but work and expect to stay happy and healthy. What happens when your job starts being less fulfilling? You’ve put all your eggs in one basket.
-   By playing the hero, you shortchange your coworkers by enabling mediocrity. When a team can rely on a hero, they don’t need to grow and learn collectively. They don’t need to get better. They can coast along, which serves no one in the end.
-   By playing the hero, you shortchange your customers by allowing a lower-quality product to ship. Heroism is only valuable when things are going wrong, and if things are going wrong, your customers are feeling the pain.

If the above is happening in your work, it’s time to make a change. But what to do?

What To Do About Heroes
-----------------------

By all means, love what you do. Work hard. Get involved. But recognize when your level of involvement is actually doing harm. If you’re playing the hero, or if you have a hero on your team, it’s probably time for a serious talk with your coworkers and manager.

Talk about numbers; people can agree more readily on numbers because they’re aren’t (or shouldn’t be) subjective. What are your metrics for reliability and how can you improve them? Get everyone to agree on operational requirements, then iterate towards a stable, trouble-free system that meets those requirements. Make everyone on the team a stakeholder in the system’s reliability. Artificial divisions between “reliability work” and “feature work” need to come down; it’s all connected.

Managers: stop rewarding people for pulling long hours. Don’t punish them, of course, but rephrase the conversation within your company. If someone is working at four in the morning, something is *deeply wrong*. Figure out what’s broken and delegate the work out evenly across your team such that it doesn’t happen again. Don’t pat your hero on the back for “pulling another late-nighter”. You’re clearly managing someone highly motivated, but you need to shape that motivation into something more constructive. That energy needs to go into design, architecture, planning, and testing, *not* late night patch sessions.

If you make the above changes, you’ll probably find that you, your coworkers, and your customers are happier. If you have a conversation like the above and nothing changes, you’ve got some hard choices to make about where you work, who you work with, and how you’re approaching your job.

Good luck, heroes.
