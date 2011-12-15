RubyGems Developers
===================

Showing off the latest and greatest projects in the RubyGems ecosystem!

Goals
=====

* Help developers get involved in RubyGems and its associated projects
* Have one place to find out where these projects are!

Setup
=====
xxx

I think just documenting the need of a 
   javaScript runtime and 
   suggestion to add either node or 
   
   therubyracer seems enough.

xxx

This is a Rails 3.1 app that is deployed to Heroku. Get the app running on your box with:

    bundle
    rails server

Done! There's no database requirement (in fact, ActiveRecord is not loaded at all!) so setup should go smoothly.

Setup for Linux
================
xxx


xxx
For Rails 3.1, Linux must have a JavaScript runtime. 
Without one Rails says:  
    Linux Could not find a JavaScript runtime. 
      See https://github.com/sstephenson/execjs 
      for a list of available runtimes. 
      (ExecJS::RuntimeUnavailable)

So modify the Gemfile before you run bundle.  The gemfile should look like this:


    require 'rbconfig'
    HOST_OS = RbConfig::CONFIG['host_os']
    source 'http://rubygems.org'
    gem 'rails', '3.1.1'

    if HOST_OS =~ /linux/i
      gem 'therubyracer', '>= 0.9.8'
    end

    gem 'flutie'
    gem 'high_voltage'
    gem 'jquery-rails'
    gem 'redcarpet'

    gem 'sass-rails',   '~> 3.1.4'
    gem 'coffee-rails', '~> 3.1.1'
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
