---
layout: post
title: Designing GitHub for Mac
date: '2011-06-29T21:56:00-07:00'
tags:
- git
- mac
- programming
tumblr_url: https://blog.horizon-nigh.org/post/7066257980/designing-github-for-mac
---
[Designing GitHub for Mac](http://warpspire.com/posts/designing-github-mac/)  

Very interesting background story on developing GitHub for Mac, which, as I [previously mentioned](http://tlog.horizon-nigh.org/2011/06/22/github-for-mac-launched.html), simplifies and improves upon several areas of Git’s workflow, for the better.

It contains an interesting point, which I had been thinking about, but forgot to mention:

> I wanted to build an awesome version control client. As it happens, Git is the perfect backend to do that …

Git itself was originally conceived as ‘Git Core’, not a complete version control system in its own right, but rather a framework which others could build version control systems _on top of_.

But nobody ever built a version control system on top of Git Core, and people wanted to use a version control system, not a framework. So the Git Core team gradually added more and more 'porcelain’ (as opposed to 'plumbing’) commands that would be easier for people to use directly in a version-control-like way. And eventually, they dropped the 'Core’ from the name when they decided the interface was good enough.

The interface was not good enough.

Git is amongst my favourite software; it changed the way I work, and there’s nothing that matches how powerful it is. But the brilliance of its internals just makes the glaring flaws in the interface more apparent; the ideas that GitHub for Mac introduces have been badly needed for a long time.

