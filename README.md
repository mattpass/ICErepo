ICErepo
=======

Show diffs, push, pull &amp; sync your site with Github repo's.

While Github has a fantastic website, mobile app, desktop app and of course bash system, there's no web based UI I can find to sync your website code with Github repo's. That's what ICErepo provides.

Originally intended to be a plugin for ICEcoder (https://github.com/mattpass/ICEcoder), I have decided to make it a standalone lib so it can run by itself or easily be integrated into any existing system.

The aim is a simple UI to view diffs between your server dir's and Github repo's. This list will consist of new files (those only on server), deleted files (those only on Github) and changed files (files that exist in both places but are different). Files that exist in both locations and the same are not shown to keep things minimalist.

Users can then to pick & choose the files they'd like to commit, provide a commit message and push to Github. Those that are only on the server are pushed to Github. Those no longer on the server are removed from Github. Those that have changed are patched over the top of the existing Github held file. As each file is synced by the user to match the server it dissapears from the UI list.

**Current screnshot:**

<img src="http://www.icecoder.net/github/screenshot.jpg" alt="ICErepo screenshot">

This lib uses customised & minified versions of these brilliant and time tested repos:

Github API lib: https://github.com/michael/github

JS Diff lib:    https://github.com/cemerick/jsdifflib

###Installation

####Step 1: Clone the repo

```
$ git clone git@github:mattpass/ICErepo
```

####Step 2: Enter your auth settings
```
Open index.php and enter either your Github oauth token or username & password
oauth is recommended here, view http://developer.github.com/v3/oauth/ for info
(If using oauth ensure you have repo scope and your app is granted the URL you'll run under)

```

####Step 3: Enter your repo/server settings
```
Also in index.php enter the repo and corresponding server paths
Once done, enter 'selected' as a 3rd array param next to your default repo/server option
Upload ICErepo & visit in a web browser
```

**Dev schedule:**

**v0.8**
Bug testing, refactoring & optimisation.

**v0.9**
Alpha testing

**v0.95**
Beta testing

**v1.0**
Version 1 released

**Estimated completion date:** Wed 22nd Aug