---
title: 'C4-[1]: Cabel Sasser on Coda'
date: 2007-08-12 00:00:00 Z
layout: post
---

Cabel works for Panic, makers of fine Mac software like Transmit, Unison, and most recently, Coda. Cabel met his business partner, Steven Frank, through the Amiga community when they were high school students. After heading off to college and getting “terrible” jobs, they decided to start a Mac software company on the side during “the worst time in Apple’s history” (the Gil Amelio era). After a stab at a software updating app that they never released, the pair decided to write a competitor to the then-standard Mac FTP client, Fetch. That product was Transit, later renamed Transmit.

The company’s next incarnation was “four guys in an apartment,” working on Audion and a never-released interactive chat environment called Ripcord. They made the conscious decision to scrap much of their pre-OS X code at this juncture. The current “version” of the company is nine people in an office in Portland. They’ve branched into shirts as well, which makes up “5%, but a fun 5%” of their business; Cabel claims the shirts are all they wear in the office. In the next year, Panic is looking is looking to grow, and is grappling with questions of how much to expand their staff, their stable of apps, their office space, and so forth.

Coda
----

At the start of their application design process, Cabel mocks up the whole application in Photoshop; each feature is a layer group. This Photoshop document is then passed on to the engineers.

Cabel describes the decision process behind picking the feature set for Coda’s features. He shows an example of a user-friendly grep feature, the sort of subtle improvement to the text editor concept that they’d decided on for Coda. More complex, Cabel had mocked-up an alternate toolbar look which ultimately necessitated a totally new toolbar implementation. Apparently, this new toolbar look may make it into Leopard, as Apple has taken notice. Cabel suggests a pragmatic and judicious application of this sort of UI revisionism. Some UI work, like nested windows and file browsing, proved challenging, and Cabel remains unsatisfied with some of the decisions they’ve made (ex: moving single- vs double-click file browser behavior to a preference pane).

The topic now changes to resolution independence. The simplest UI elements in Coda are drawn programmatically, which solves the issue of scaling to higher resolutions. PDFs are used for flat color and basic shapes in controls, and multi-resolution TIFFs are used elsewhere. Cabel zooms in tightly to Coda’s interface to demonstrate the effect of through-and-through resolution independence, and it’s stunning. For designing resolution-independent textures, Cabel recommends working with Photoshop’s vector-based shapes and applying effects thereupon.

The process of deciding on a name and icon for Coda was difficult. The application was originally named “Transmit Studio,” but this was abandoned in the icon selection process. The Icon Factory worked up an icon of a forklift, but this was abandoned when Panic realized that an application called Forklift with an eponymous icon was on the market. They then went in a more organic direction, embracing the concept of developers “growing” the applications they’d develop in this application. A leaf was settled on, and after several revisions they settled on a design that’s a balance of hyper-realistic and a more idealized form. There’s apparently a hint of fuzz around the stem of the leaf, testament to Cabel’s and icon designer David Lanham’s attention to detail. Two sets of toolbar icons were developed, and they settled on the more literal collection.

On to the top of partnering. Panic courted the developer of CSSEdit, as they had no interest in competing with “a great CSS editor.” The deal didn’t work out, so Panic wrote their own. Panic wanted to use O’Reilly for the books section of Coda, but the publisher wanted too large a cut of every sale. They partnered with No Starch Press instead.

On the subject of anti-piracy, Cabel claims it’s a losing battle. They attempted to block the trading of serial numbers with a “depressing message” and network serial number checking, but haven’t seen any wide trading of serial numbers yet. They have seen one attempt at scripted serial number generation.

Cabel concludes by mentioning that Panic is hiring, and that they’re open to developers who work on shareware on the side.

Questions
---------

“Comment on the shaded look of Coda?” Cabel says that “we’ve seen Aqua become less Aqua over time,” and remarks on the dramatic change between 10.2 and the present OS X look. He likes the look of Leopard, and his hopeful about some of the best aspects of the iPhone making it in to the OS’s look.

“Why hire a designer when you’re clearly good at it?” Cabel claims he’s not a good artist (and that Steven Frank is a great artist but a bad designer). He describes himself as the bottleneck in Panic’s development process because all UI elements have to be approved by him.

“How did you make the decision to migrate to Cocoa?” Cabel says it simply felt like the right thing to do at the time.

“Do you really rapidly prototype in Photoshop?” Cabel claims he does, with occasional Interface Builder mockups to grab controls from.

“Any feedback on your blog post about resolution independent stuff from Apple?” Yup!

“What about the design philosophy a small, disparate Unix tools like grep?” Cabel describes the challenge as determining the scope of the “pieces of the web design puzzle” that they put together.

“How do you prototype interactivity beyond Photoshop?” Thinking about storyboarding.

“Opening up the books feature?” It’s a very popular request. Not sure how it’s going to look yet.

(I missed a couple questions at the end.)
