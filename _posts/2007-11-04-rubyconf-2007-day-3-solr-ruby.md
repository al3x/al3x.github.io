---
title: 'RubyConf 2007, Day 3: Solr-Ruby'
date: 2007-11-04 00:00:00 Z
layout: post
---

Solr, the Apache foundation’s open source search engine, has been good to me. Twitter’s people search feature (the “find folks!” box you’ll see around the site) is powered by Solr, and it’s been a rock-solid piece of our infrastructure. Speaker Erik Hatcher is a committer on Solr and the search library that powers it, Lucene.

Solr boasts features like replication, faceting , highlighting, spell checking, an administrative interface, and more. Big names like CNET, the Internet Archive, Netflix, Digg, and AOL are making use of the project. The Lucene library is in use at Technorati, IBM, Monster, Wikipedia, and many more big installations. It’s safe to say that Solr and Lucene have been battle-tested.

Lucene is an *inverted index*. You put documents into it, and those documents are composed of fields. Inside those fields, a tokenization process finds terms after applying transformations like downcasing, whitespace removal, word-stemming, and so forth. Those terms are then scored, and those scores are used to figure out which search results are the most relevant.

Solr is a Java web application, and can be deployed on any Java application server (Jetty, by default). Talking to Solr just requires speaking HTTP: POST to add or update a document, GET to search, and so forth. While default responses are in XML, it’s possible to get other formats like JSON or Ruby hashes back from Solr.

solr-ruby is Hatcher’s library for communicating with Solr from Ruby. He demos inserting a number of documents into a local Solr instance, and then retrieving some results in various formats directly from the browser.

Some brief sample ruby-solr code is then shown, with a note that “auto-committing” can be inefficient when loading many documents at one time. Hatcher also notes that Solr adds a primary key semantic where Lucene does not, by default. Lucene also does not have a concept of updating a document, only replacing or adding documents. A patch that provides updating behavior is in progress.

solr-ruby is behind the acts\_as\_solr Rails plugin (in use on Twitter with some small modifications), Flare, Blacklight (a project by Hatcher at the University of VA), Collex (a database of literature), and more. Hatcher suggests interacting directly with Solr as a means for sorting out bugs in acts\_as\_solr and other tools that hide away communication with the search engine. Also demonstrated is Luke, the Lucence Index Toolbox, which provides a host of interesting output and modification options for a Lucene index.

As a general solution for mapping Ruby objects to Solr results, Hatcher has developed Mapper. Unfortunately, his demonstration of its code was somewhat side-tracked by an explanation of Lucene’s index structure. In a nutshell, it allows mapping Ruby symbols to attributes in Solr documents. The use of Procs is supported, allowing for more dynamic mappings.

In the future, Hatcher is interesting in bringing parts of acts\_as\_solr into solr-ruby, along with more introspection into Ruby objects and an improved response writer. He’s looking for guidance on improving the library’s API and DSL, as well as help with documentation. You’ll find Solr-related recipes by Hatcher in the upcoming “Rails Recipes” book.
