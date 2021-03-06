---
title: The Case Against Everything Buckets
date: 2009-01-31 00:00:00 Z
layout: post
---

The Mac software ecosystem faces a plague. A plague of Everything Buckets. Indulge me.

If you search for “productivity” or “organization” software for the Mac, you’ll find variations on a particular type of application. These applications claim to be “your outboard brain” or “your digital filing cabinet” or similar. They go by many names: [Yojimbo](http://www.barebones.com/products/yojimbo/), [Together](http://reinventedsoftware.com/together/), [ShoveBox](http://wonderwarp.com/shovebox/), [Evernote](http://evernote.com/), [DEVONthink](http://www.devon-technologies.com/products/devonthink/). There may be differences in their implementation and appearance, but these applications are all of the same sinister ilk. They are Everything Buckets.

An Everything Bucket, since you’re probably wondering, is what I call applications that encourage the user to throw anything and everything into them. They’re virtual scrapbooks, applying a lightweight organization system to (often) unrelated data of varying types. These applications typically employ a proprietary database, or at best, build atop the SQLite database technology that Apple ships with Mac OS X. They usually default to storing information in Rich Text Format (RTF) or Portable Document Format (PDF). They are Not A Good Idea.

Why Everything Buckets Are Not A Good Idea
------------------------------------------

Computers work best with structured data. Everything Buckets discourage the use of structured data by providing a convenient place to commingle “structureless” data like RTF and PDF documents. Rather than forcing the user to figure out the rhyme and reason of their data (for example, by putting receipts in a financial management application and addresses in an address book), Everything Buckets cry: “throw it all in here! Search it! Maybe I’ll corrupt my proprietary database, but maybe I won’t and you’ll have the joy of sifting through a mire of RTF documents. Doesn’t that sound great?”

This proposition should *not* sound great. If you think you’re going to save time in the long run by throwing your data into a big bucket now, then sifting through it later, you are mistaken. There are better ways.

The Filesystem
--------------

If you want to store data of differing types within a lightweight organization system, I encourage you to check out *the filesystem*.

On Mac, an application called Finder provides a pleasant interface to listing, organizing, and previewing information in a filesystem. It’s free, and it’s running on your Mac right now. Oh sure, it’s got some quirks, but for the most part you’ll find it reliable. You can create directories, and even create *directories inside directories* (a feature that Yomjimbo currently lacks).

Everything Buckets are selling you a filesystem, and removing the step of creating and saving a new file within that filesystem. That’s their primary value. Whatever organization scheme they may claim to offer, you can replicate on the filesystem. I promise. Even tags (symlinks, aliases - look ’em up).

If you still feel like paying $39 for a proprietary second-rate filesystem, well, bless your heart. You’re the stuff a software developer’s dreams are made of.

The Search Illusion
-------------------

Most Everything Buckets also let you search. Let’s talk about that.

We live in the age of search. “Why can’t I just Google for it?” is a common complaint from anyone who’s ever misplaced a file and doesn’t know better. In response to this complaint, desktop search technologies like Spotlight have emerged. How do they work? They sift through your structureless data periodically and build a structure from it. This structure is called an *index*. Without an index, searching through all but smallest quantities of unstructured data takes ages. Once again: *computers work best with structured data*.

So while you, the user, are presented with the illusion of “Googling” for that phone number you threw into your Everything Bucket, your computer is constantly hauling ass to make up for the fact that you couldn’t be bothered to put the phone number in your virtual address book. “What do I care how much work my computer does?” you say, until the next time the Spotlight indexer kicks in and your Mac grinds to a halt.

This posits a stronger correlation between Everything Buckets and things like Spotlight than I really mean to put forward. The point is that if you don’t do some organization of your data up front, you probably won’t like the ways in which it’s done for you later.

With an Everything Bucket, you also miss out on opportunities to do interesting things with data. Once data is normalized and structured, finding correlations is faster and easier. Remember the first time you really got a spreadsheet to do something cool for you? You can’t do that with a big steaming pile of RTF files.

Applications That Actually Do Things
------------------------------------

One of my [Rules For Computing Happiness](http://al3x.net/2008/09/08/al3xs-rules-for-computing-happiness.html) is: “do not use software that does many things poorly.” Everything Buckets violate this rule up, down, and sideways. They’re poor filesystems, poor text editors, poor databases, poor to-do lists, poor calendars, poor address books, poor bookmark managers, and poor password managers. At their worst, they’re even poor web browsers, poor encryption systems, and poor synchronization schemes.

The corollary to that rule is: “use software that does one thing well.” When you need to store some data, there are *so many wonderful applications* to pick from. From recipes to receipts, photographs to music, journal entries to to-do list items, there’s a great application out there for what you need to do. Chances are good that the right application *structures* your data so that you can get more out of it. Use an application that actually does something more than holding data. You’ll be happier.

If you don’t want to be forever accumulating applications, store stuff as plain text on the filesystem. It’s dead reliable, you can shuffle it about however you want, and you’ll be able to search through it quickly, even without an index.

Conclusion
----------

Get your brain out of an Everything Bucket and in to an application (or two, or three) that adds some value to your data. Of the culprits named above, at least [DEVONthink](http://www.devon-technologies.com/products/devonthink/) can claim some intelligence in finding correlations between documents. But chances are good that if you think about the task you’re really trying to accomplish, there’s an application out there for it that will make your life easier. Do some research on a site like [I Use This](http://osx.iusethis.com/) or [MacUpdate](http://macupdate.com) and find an app you trust.

Your computer wants your data to be structured. Throw it a bone.
