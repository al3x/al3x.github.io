---
title: Announcing Acts As Sanitized
date: 2007-01-12 00:00:00 Z
layout: post
---

When I was doing my [talk on Rails security](http://static.al3x.net/securing_rails.pdf) at RailsConf Europe I joked about delivering a magical plugin, `acts_as_impenetrable`, that solved all of your security needs. There’s still no magic bullet for security, but I’d like to contribute a smidge of code that brings us a step closer.

Rails has the ability to mitigate [cross-site scripting attacks](http://en.wikipedia.org/wiki/Cross-site_scripting) in the form of its [ActionView::Helpers::TextHelpers\#sanitize](http://api.rubyonrails.org/classes/ActionView/Helpers/TextHelper.html#M000516) method. This method won’t catch every clever XSS out there, but it sure helps. Sadly, `sanitize` is unavailable by default from your models and controllers; the expected usage pattern is that you’ll handle sanitization in your view, ex: `<%= sanitize(`story.title) \>@ or `<%=h `story.body\>@.

I don’t think that’s especially, uh, agile (or whatever). Neither is importing those TextHelpers into your controller and reassigning your models’ various attributes to sanitized versions of themselves before saving. It’s tedious, it’s repetitive, and it opens the door to careless errors. Are you sure that you know *every* field that gets displayed in your views, even after all those revisions and migrations?

My solution to this is a plugin: [acts\_as\_sanitized](http://code.al3x.net/svn/acts_as_sanitized/). You use it like so:

class Comment \< ActiveRecord::Base
 acts\_as\_sanitized
 end

That’s it. The plugin figures out which fields in your model are able to be sanitized at application runtime. If you’re not comfortable with that for some strange reason, you can also specify which fields you’d like sanitized. You can even tell it to strip all tags, not just the ones that the `sanitize` method in Rails handles (`script` and `form`). Plus no more monkeying around in your controllers, no more wasteful filtering in your views.
Install like so from the root directory of your Rails app:

script/plugin install http://code.al3x.net/svn/acts\_as\_sanitized/

Documentation is included in the README file, and there’s a decent suite of tests included.

There isn’t much to this plugin as it stands, but as XSS attacks become ever-more complicated, I’m hoping that this plugin evolves to detect and combat them. If you see attacks that are sneaking by `sanitize` and `strip_tags`, let me know! Bugs and patches are more than welcome.
