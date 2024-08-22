---
layout: post
title: All Logitech Mac drivers silently install Unsanity hacks
date: '2007-06-28T16:44:45-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/4494751/all-logitech-mac-drivers-silently-install-unsanity
---
[All Logitech Mac drivers silently install Unsanity hacks](http://forums.logitech.com/logitech/board/message?board.id=macmice&message.id=257)  

I stumbled upon this today when I was trying to figure out why my new Logitech mouse’s tilt-scrolling functionality wasn’t working, and nearly had an aneurism.

Unsanity’s [Application Enhancer](http://en.wikipedia.org/wiki/Application_Enhancer) is a hack (by their own admission) that ties into the OS and makes all kinds of strange changes to it that can cause complicated problems. Apple [automatically disregards](http://lists.apple.com/archives/carbon-dev/2007/Mar/msg00225.html) any bug reports sent to them from systems with Application Enhancer installed.

There’s a debate among developers and users about whether these hacks are ‘worth it’. I myself tend to lean more towards the 'no, a few cheap tricks aren’t worth compromising the system’s stability and integrity’ side. Needless to say, I had no idea that I was _already running it._

That Logitech for some reason feels it’s necessary to install this mess just for basic functionality of its products speaks volumes to the quality (or lack thereof) of their software. I will never buy from them again.

Even worse, running the Logitech uninstaller doesn’t get rid of the Unsanity junk that it put there in the first place. I had to download [Unsanity’s installer](http://www.unsanity.com/haxies/ape) (which cheerfully confirmed that I was already running version 2.0.2) in order to uninstall Application Enhancer.

Although most of the mouse’s functionality works fine on Mac OS X without any drivers at all (all three buttons, and vertical scrolling), the horizontal tilt-scrolling does not. Alternatives suggested in the linked thread are [USB Overdrive](http://www.usboverdrive.com/USBOverdrive/News.html) and [SteerMouse](http://plentycom.jp/en/steermouse/); neither of which, unfortunately, are free.

