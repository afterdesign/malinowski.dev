---
layout: post
title:  "Upgrading bash on your MacOS"
date:   2019-06-16
category: "tech gibberish"
---

I do not recommend change of SHELL systemwide. Let's make it safe if brew upgrade will go bad.

MacOS is using bash version 3 (until MacOS 10.14 as in 10.15 zsh will replace it). Or to be exact it's using ```/bash/sh``` which is:

```bash
sh-3.2# sh --version
GNU bash, version 3.2.48(1)-release (x86_64-apple-darwin12)
Copyright (C) 2007 Free Software Foundation, Inc.
```

Newer bash (v5 as of right now) has usefull things like associative arrays:

```bash
declare -A array
array[foo]=bar
array[bar]=foo
```

And more you can read in [NEWS file](http://tiswww.case.edu/php/chet/bash/NEWS).

So to upgrade bash to version 4 on our osx we need [brew](https://brew.sh) (kinda obvious).

Then we need to install bash:

```bash
brew install bash
```

Next we need to add our bash to shells:

```bash
sudo bash -c "echo $(brew --prefix)/bin/bash >> /private/etc/shells"
```

And the last step is to change our shell in system preferences so go to:

system preferences -> Users & Groups (unlock pref pane) -> right click on your account Advanced Options... and change Login shell option to ```/usr/local/bin/bash```:
