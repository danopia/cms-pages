Ruby on Sails Dependencies
==========================

[Ruby on Sails] [[sails]] requires a few packages and gems to run.

Packages
--------
* Ruby 1.8
* Rubygems 1.8 (although on Debian, it's recomeanded to install from source)
* Dev packages for Ruby
* Ruby OpenSSL bindings
* Ruby SQLite3 bindsings (libsqlite3-dev)

Gems
----
* rails
* thin
* hpricot
* authlogic
* sqlite3-ruby

Certificates
------------
One of the hardest parts about setting up a Wave server, no matter which
software you use, is setting up the cerficates and private keys. You need to
have a third-party certificate with your domain name in the Common Name field,
and your XMPP server will soon be required to use signed certs as well.

Unfortunately, I don't have a guide for this yet.
