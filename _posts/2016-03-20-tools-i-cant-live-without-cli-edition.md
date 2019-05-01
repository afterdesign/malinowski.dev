---
layout: post
title:  "Tools I can't live without - CLI edition"
date:   2016-03-20
category: "tooling rant"
issue_id: 6
---

When I was writing about my pain with [OSX reinstallation](http://afterdesign.net/2016/03/07/os-x-reinstallation-pain.html) I had also idea to write a list of tools that I'm using and that I really like (or even love). So let's do this !

This time I'm going to list CLI tools.

# Command Line Tools installed with [homebrew](http://brew.sh)

"Homebrew installs the stuff you need that Apple didn’t."
In general this is package manager. I like it because I don't have to install packages with root privileges.

##### <a href="https://github.com/wting/autojump" rel="noreferrer" aria-label="autojump tool external URL" target="_blank">autojump</a>

I have more then 50 repositories cloned to my ```~/Projects``` directory so using ```cd``` is a bit painfull. With autojump I can change directory even when I remember part of the path.

<picture>
  <source srcset="/images/posts/6/autojump.webp" type="image/webp">
  <img src="/images/posts/6/autojump.png" alt="autojump screenshot">
</picture>

##### <a href="http://hisham.hm/htop/" rel="noreferrer" aria-label="htop tool external URL" target="_blank">htop</a>

I know there is a activity monitor app but I really like htop and it looks cool with colors, options to sort or even see tree of threads.

<picture>
  <source srcset="/images/posts/6/htop.webp" type="image/webp">
  <img src="/images/posts/6/htop.png" alt="htop screenshot">
</picture>

##### <a href="https://github.com/jeffkaufman/icdiff" rel="noreferrer" aria-label="icdiff tool external URL" target="_blank">icdiff</a>

The best diff tool I know.
I'm using it always before I commit something (with this simple [bash script](https://github.com/afterdesign/dotfiles/blob/master/bin/git-diff-add)).
I'm using icdiff also as my git difftool:

{% highlight bash %}
[difftool]
    prompt = false
[difftool "icdiff"]
    cmd = icdiff $LOCAL $REMOTE | less -R
{% endhighlight %}

<picture>
  <source srcset="/images/posts/6/icdiff.webp" type="image/webp">
  <img src="/images/posts/6/icdiff.png" alt="icdiff screenshot">
</picture>

##### <a href="https://dev.yorhel.nl/ncdu" rel="noreferrer" aria-label="ncdu tool external URL" target="_blank">ncdu</a>

If you're like me sometimes you're trying to figure out "why the hell all my disk space is gon".
Instead of using paid tools like [daisydisk](https://daisydiskapp.com) I'm using this free, open and awesome tool

<picture>
  <source srcset="/images/posts/6/ncdu.webp" type="image/webp">
  <img src="/images/posts/6/ncdu.png" alt="ncdu screenshot">
</picture>

##### <a href="https://stedolan.github.io/jq/" rel="noreferrer" aria-label="jq tool external URL" target="_blank">jq</a>

Pretty print json files.

<picture>
  <source srcset="/images/posts/6/jq.webp" type="image/webp">
  <img src="/images/posts/6/jq.png" alt="jq screenshot">
</picture>

##### <a href="https://pngquant.org" rel="noreferrer" aria-label="pngquant tool external URL" target="_blank">pngquant</a>

When I'm adding screenshots (like in this post) then I'm using pngquant. It can really crunch image size without much quality loss (hell, I can't even see the quality difference)

<picture>
  <source srcset="/images/posts/6/pngquant.webp" type="image/webp">
  <img src="/images/posts/6/pngquant.png" alt="pngquant screenshot">
</picture>

##### <a href="http://www.nano-editor.org" rel="noreferrer" aria-label="nano tool external URL" target="_blank">nano</a>

Yup I'm one of those people that are not using vi/vim.
And to install newest nano you have to add [homebrew/dupes](https://github.com/Homebrew/homebrew-dupes) with ```brew tap homebrew/dupes```

<picture>
  <source srcset="/images/posts/6/nano.webp" type="image/webp">
  <img src="/images/posts/6/nano.png" alt="nano screenshot">
</picture>

##### <a href="https://mosh.mit.edu" rel="noreferrer" aria-label="mosh tool external URL" target="_blank">mosh</a>
I'm using this to connect with my personal servers. I'm still using IRC and my connection at home is a bit flaky lately. Now I know that I lost connection to my server (and irssi) and the connection is reestablished right after the internet is back.

<picture>
  <source srcset="/images/posts/6/mosh.webp" type="image/webp">
  <img src="/images/posts/6/mosh.png" alt="mosh screenshot">
</picture>

##### <a href="https://github.com/dennishafemann/tmux-cssh" rel="noreferrer" aria-label="tmux cssh tool external URL" target="_blank">tmux-cssh</a> and/or <a href="http://code.google.com/p/csshx" rel="noreferrer" aria-label="csshx tool external URL" target="_blank">csshx</a>

When I want to check something on multiple servers I'm just using one of those tools.
Depends if I want to have multiple windows or all in one window.

##### <a href="https://www.gnu.org/software/bash/" rel="noreferrer" aria-label="bash tool external URL" target="_blank">bash</a> with <a href="https://github.com/scop/bash-completion" rel="noreferrer" aria-label="bash completion tool external URL" target="_blank">bash-completion2</a>

Yes I'm using bash and I like it, also OSX by default is comming with 3.2 and one of first things I do is upgrade bash with brew to newest version

##### <a href="http://git-scm.com" rel="noreferrer" aria-label="git tool external URL" target="_blank">git</a> with <a href="https://github.com/tj/git-extras" rel="noreferrer" aria-label="git extras tool external URL" target="_blank">git-extras</a> and <a href="https://github.com/holygeek/git-number" rel="noreferrer" aria-label="git number tool external URL" target="_blank">git-number</a>

I'm a programmer and I really like git

##### <a href="https://www.vanheusden.com/multitail/" rel="noreferrer" aria-label="muti tail tool external URL" target="_blank">multitail</a>

Tail multiple files with nice ncurses windows.

##### <a href="https://sites.google.com/a/chromium.org/chromedriver/" rel="noreferrer" aria-label="chromedriver tool external URL" target="_blank">chromedriver</a> with <a href="http://www.seleniumhq.org/download/" rel="noreferrer" aria-label="selenium tool external URL" target="_blank">selenium-server-standalone</a>

I'm using this to locally run tests from behat/behave.
Or just to run [my project](https://github.com/afterdesign/unsuck-ads) to now how much faster sites are without ads.


# Command Line Tools installed manually from pkg/dmg

##### <a href="http://vagrantup.com" rel="noreferrer" aria-label="vagrant tool external URL" target="_blank">vagrant</a>

Every project I'm starting is tested and run within debian stable. To create this environment I'm using virtualbox and to automate this I'm using vagrant. It's just easier for me to do ```vagrant up``` and have once configured OS running.

<picture>
  <source srcset="/images/posts/6/vagrant.webp" type="image/webp">
  <img src="/images/posts/6/vagrant.png" alt="vagrant screenshot">
</picture>

##### <a href="http://packer.io" rel="noreferrer" aria-label="packer tool external URL" target="_blank">packer</a>

I'm using this tool to create custom boxes to use with vagrant. It's easier to create box with already installed databases cause installing it once when creating box is much simpler and faster then installing it with


# Command Line Tools installed with <a href="https://www.npmjs.com" rel="noreferrer" aria-label="npm tool external URL" target="_blank">npm</a>

Npm is installed with [nodejs](http://nodejs.org) which I'm installing with homebrew.

##### <a href="https://github.com/tldr-pages/tldr-node-client" rel="noreferrer" aria-label="tldr tool external URL" target="_blank">tldr</a>

I don't like to search man pages all the time, this tool gives me all I need to know from man in shorter version (especially often used ```tldr ln```)

<picture>
  <source srcset="/images/posts/6/tldr.webp" type="image/webp">
  <img src="/images/posts/6/tldr.png" alt="tldr screenshot">
</picture>

# Command Line Tools installed with <a href="https://pypi.python.org/pypi/pip" rel="noreferrer" aria-label="pip tool external URL" target="_blank">pip</a>

Pip can be installed with [python](https://python.org) or with ```easy_install```.
I'm always installing newest python version from homebrew.

##### <a href="https://github.com/jkbrzt/httpie" rel="noreferrer" aria-label="httpie tool external URL" target="_blank">httpie</a>

The quote from the website is saying everything: "HTTPie (pronounced aitch-tee-tee-pie) is a command line HTTP client. Its goal is to make CLI interaction with web services as human-friendly as possible."

<picture>
  <source srcset="/images/posts/6/httpie.webp" type="image/webp">
  <img src="/images/posts/6/httpie.png" alt="httpie screenshot">
</picture>
