mec-mec
=======

using:
  * [locomotiveCMS](http://www.locomotivecms.com/)
  * [rvm](https://rvm.io/) (optional)
  * [pow](http://pow.cx/) (optional)
  * [tmuxinator](https://github.com/aziz/tmuxinator) (optional)
  * [heroku](http://www.heroku.com/)


If this is your first install, automatically load on login with:
  mkdir -p ~/Library/LaunchAgents
  cp /usr/local/Cellar/mongodb/2.0.5-x86_64/homebrew.mxcl.mongodb.plist ~/Library/LaunchAgents/
  launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist

If this is an upgrade and you already have the homebrew.mxcl.mongodb.plist loaded:
    launchctl unload -w ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
    cp /usr/local/Cellar/mongodb/2.0.5-x86_64/homebrew.mxcl.mongodb.plist ~/Library/LaunchAgents/
    launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist

Or start it manually:
    mongod run --config /usr/local/etc/mongod.conf

The launchctl plist above expects the config file to be at /usr/local/etc/mongod.conf.