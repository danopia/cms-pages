<img style="border: thin solid #808080; margin: 1em; padding: 1em; float: right; background-color: #fff;" title="Ruby on Sails" src="http://github.com/danopia/ruby-on-sails/raw/master/contrib/sails_sailing.png" alt="Ruby on Sails" width="284" height="302" />

Welcome to Ruby on Sails!
=========================
Ruby on Sails is an ambitious project by a high schooler, and will hopefully end up being a decent library, provider, and Web UI for Google Wave. It currently has a degree of federation, but is still in *very* rapid development and federation constantly breaks and works again as I restructure the code from being one 1000-line file into having classes, folders, files, and even docs.

Why?
----
Why not?

Technical Information
---------------------
At the low-level, the raw provider requires Ruby OpenSSL bindings (thank Google), an existing XMPP server, certificates, and a couple gems (hpricot for one). There is a web frontend, written in Ruby on Rails, which is currently pretty basic but has a degree of responsiveness, if it's in a good mood. The Rails app communicates with the provider with DRb, so there is barely any client/server code to be seen. This makes the source quite a bit cleaner.

The web app is more than just Rails, though. Running it in mod_passenger or similar is *not recommended*! Instead, use a Rack-enabled server, such as thin. Thin is what the test server runs, and the _only_ HTTPd that I use with it. To start the thin app, go to the repo root, i.e. ruby-on-sails/. Don't run `thin start` in rails/, ad this will not enable the custom config. Use `rake thin:start` to start up a thin instance using the RackUp file.
