Deprecation Notice
==================

**This site was previously linked from the [rubygems.org home page](https://rubygems.org/). That link has
been redirected to the [RubyGems Guides Contributing page](http://guides.rubygems.org/contributing/). Future
updates should be made in the [RubyGems Guides GitHub Project](https://github.com/rubygems/guides).**

RubyGems Developers
===================

Showing off the latest and greatest projects in the RubyGems ecosystem!

Goals
=====

* Help developers get involved in RubyGems and its associated projects
* Have one place to find out where these projects are!

Setup
=====

This is a Rails 3.1 app that is deployed to Heroku. Get the app running on your box with:

```bash
bundle
rails server
```

Done! There's no database requirement (in fact, ActiveRecord is not loaded at all!) so setup should go smoothly.

JavaScript Runtime Required
===============================

Rails 3.1 needs a Javascript runtime and on Linux this requires special handling.
Without a runtime, rails commands like  *rails server* throw an exception saying:

    Linux Could not find a JavaScript runtime.
    See https://github.com/sstephenson/execjs
    for a list of available runtimes.
    (ExecJS::RuntimeUnavailable)

To fix this error either **install node.js** (with: sudo apt-get nodejs)

OR

Include **'therubyracer'** in your Gemfile.

```bash
gem "therubyracer", :require => 'v8'
```

See https://github.com/sstephenson/execjs for more.

Adding links
============

This site's content lives mostly in `app/views/pages/home.html.md`. Jump in and edit it, send a pull request, and we'll merge it in!

Thanks
======

Huge thanks to [thoughtbot](http//thoughtbot.com) whose [playbook](http://playbook.thoughtbot.com) these styles are based off of.

Legal
=====

The actual content of the articles is licensed under Creative Commons. The code that this project consists of is licensed under MIT.
