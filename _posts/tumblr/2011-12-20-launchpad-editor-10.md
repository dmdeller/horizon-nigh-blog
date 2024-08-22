---
layout: post
title: Launchpad Editor 1.0
date: '2011-12-20T13:18:00-08:00'
tags:
- launchpad editor
tumblr_url: https://blog.horizon-nigh.org/post/14517468808/launchpad-editor-10
---
[Launchpad Editor 1.0](http://horizon-nigh.org/launchpad-editor.html)  

I created a Mac app - my first<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>.

I’ve been looking for an application launcher for a long time. When you have a lot of apps, like I do, the Dock just doesn’t cut it. Not that I didn’t try: I made various attempts to have a categorised, hierarchical list of applications in the Dock, which tended to get broken or more annoying in different ways with each major release of Mac OS X.

I’ve tried various third-party utilities, but they were all too complicated and customisable. Or, they expected me to type the name to launch it! There’s a reason I use a Mac instead of a UNIX terminal<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>.

What I was really looking for was something like the Classic Mac OS Launcher:

[![System 7 launcher screen shot](http://f.cl.ly/items/251O091a022t1s2R1T2A/launcher_sm.png)](http://www.macintouch.com/specialreports/lion/review2.html#launchpad)

Simple. To the point.

So when I first heard about Launchpad, to come as part of Lion, it seemed to be just what I was looking for.

And indeed, it was–after I took the time to actually organise my apps. Which took a really long time. Click, drag, wait…wait….wait…drop. Repeat. Sigh.

But it was worth it. All my apps, easily accessible and meticulously organised. Yes, I tend to be a little more obsessive about this than most people, but it made me happy.

And then, one day, Launchpad randomly corrupted its database, resetting all of my apps into alphabetical order and losing all of my folder groups.<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup> I would have had to do it all over again–and maybe not for the last time, if Launchpad didn’t have its bugs worked out yet.

## The idea

I was looking for an excuse to make a Mac app anyway.

I’ve always wanted to make native apps. Even having grown up in the ‘boom’, and being a self-taught web developer myself, I would tell people that what I really wanted to do was make 'real’ software someday. And they would laugh. 'Web apps are the future, silly kid!’ But while making web apps has been fun and useful, even the best web UIs have always felt to me like they lack the stability and consistency of a native app. So I’m glad to see the tide turn somewhat back towards native apps in recent years, which affords me an excuse to pursue making them. Anyway.

Once I found out that the Launchpad data is just a simple SQLite3 database, I decided to give a try at making a simple app to manipulate it, such that I could get the job done faster, and with less annoyance, than using Launchpad itself. All it would really need to be is a list view that synchronises to a database, so I thought it would be educational but not too daunting.

## Building it

Reading the database was simple: I just used Gus Mueller’s excellent [FMDB](https://github.com/ccgus/fmdb). I had to figure out the database schema, since it’s not documented anywhere (with a little help - thanks, [Andreas](http://chaosspace.de/launchpad-control/)!), but it was surprisingly straightfoward. Curiously, it doesn’t look like a database that was generated using Core Data (which was why I didn’t attempt to use Core Data for this either), which makes me wonder Apple _is_ using: straight SQLite C calls? _Shudder._

The main challenge was in learning how to do things in AppKit, after I had only just recently learned to use UIKit for making an iPhone app. But they both use similar patterns, the major example being the data source/delegate pattern, so I was pleased to find that I could use many of the concepts I already knew. And when I was having trouble finding documentation on certain subjects, the people in #macdev on Freenode were very helpful, for which I’m very grateful.

One thing I _didn’t_ have to worry about (much) was… memory management! After having to learn retain/release the hard way for my last project, [automatic reference counting](http://developer.apple.com/library/mac/#releasenotes/ObjectiveC/RN-TransitioningToARC/_index.html#//apple_ref/doc/uid/TP40011226) was a breath of fresh air. It would be hard to overstate how pleased this made me: it allowed me to focus on my application logic, rather than getting constantly distracted by what seems like bookkeeping.

And now it’s done!<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">4</a></sup> Did I mention you can [get it here](http://horizon-nigh.org/launchpad-editor.html)? Since I couldn’t put it in the App Store (for obvious reasons), I made it open-source [on GitHub](https://github.com/dmdeller/launchpad-editor).

## Future

I expect that Apple will improve Launchpad in the future, hopefully by 10.8, making my app unnecessary. It’s typical of Apple to release a minimal-but-polished first version, then add more features later.

Or not. Maybe Launchpad is only for 'halo effect’ former Windows users brought over to the Mac via their iPhones, who aren’t going to have many apps anyway, and thus maybe Apple doesn’t think anything needs to change. In that case, perhaps I’ll eventually attempt to reinvent the original Launcher myself. (Unless someone else does it first.)

In the meantime, I’m looking forward to making more apps.

* * *

1. That reminds me: I never wrote a blog post about [my first iPhone app](http://horizon-nigh.org/laundry-minder.html). Perhaps I’ll come back to it.&nbsp;[↩︎](#fnref:1)

2. Not that there’s anything wrong with that. I know a bunch of smart people who use Terminal as much as possible. It’s just a different way of thinking.&nbsp;[↩︎](#fnref:2)

3. I think this happened on or around the time of the 10.7.2 update.&nbsp;[↩︎](#fnref:3)

4. Well, shipped. Software is never really done, only acceptable enough to release. I still have more ideas than time, so if anyone wants to chip in, [here are some places to start](https://github.com/dmdeller/launchpad-editor/blob/master/Todo.txt)…&nbsp;[↩︎](#fnref:4)

