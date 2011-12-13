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

    bundle
    rails server

Done! There's no database requirement (in fact, ActiveRecord is not loaded at all!) so setup should go smoothly.

Setup for Ubuntu
================

Ubuntu needs a JavaScript runtime. It says: 
    Ubuntu Could not find a JavaScript runtime. 
      See https://github.com/sstephenson/execjs 
      for a list of available runtimes. 
      (ExecJS::RuntimeUnavailable)

So modify the Gemfile before you run bundle.  The gemfile should look like this:

    source 'http://rubygems.org'
    .            
    .            
    .            
    gem 'rails', '3.1.1'
    gem 'therubyrunner'
    .            
    .            
    .            
    gem 'uglifier', '>= 1.0.3'

Then, run the same 2 commands shown above:

    bundle
    rails server

Now, rails and rake should run for you in ubuntu

Adding links
============

This site's content lives mostly in `app/views/pages/home.html.md`. Jump in and edit it, send a pull request, and we'll merge it in!

Thanks
======

Huge thanks to [thoughtbot](http//thoughtbot.com) whose [playbook](http://playbook.thoughtbot.com) these styles are based off of.

Legal
=====

The actual content of the articles is licensed under Creative Commons. The code that this project consists of is licensed under MIT.
