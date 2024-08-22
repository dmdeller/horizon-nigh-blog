---
layout: post
title: PowerMate 3.0 volume scripts for Mac
date: '2011-08-20T13:48:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/9171661080/powermate-30-volume-scripts-for-mac
---
[PowerMate 3.0 volume scripts for Mac](https://gist.github.com/1159393)  

In previous versions of Mac OS X, you could hold shift+option while pressing volume up/down keys on the keyboard, to increase or decrease the volume by minute amounts. I used this frequently and it drives me crazy that [it’s absent in Lion](http://hints.macworld.com/article.php?story=20110730172909171).

There are a few possible workarounds, but as I already had a neglected [PowerMate](http://store.griffintechnology.com/powermate) sitting on my desk, I figured I may as well dust it off.

Unfortunately, version 3.0 of the PowerMate software has lost the ability to increase or decrease system volume by small amounts, which was present in previous versions. By default, it only simulates the volume up/down key presses, like a keyboard, which is of no help to me. But, after Googling for a few minutes, I was able to combine several bits of information I found into this:

<script src="https://gist.github.com/1159393.js?file=volume-down.scpt"></script><script src="https://gist.github.com/1159393.js?file=volume-up.scpt"></script>

This may not be the best way to accomplish this. Please submit improvements via GitHub.

One nice thing about 3.0 is that you can paste inline AppleScript to assign to an action (if you can ever figure out how to use it - the UI is a nightmare).

