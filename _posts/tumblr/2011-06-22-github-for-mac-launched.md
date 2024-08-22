---
layout: post
title: GitHub for Mac launched
date: '2011-06-22T23:52:00-07:00'
tags:
- git
- mac
- programming
- longer post
tumblr_url: https://blog.horizon-nigh.org/post/6815461978/github-for-mac-launched
---
[GitHub for Mac launched](http://www.webcitation.org/query?url=https%3A%2F%2Fgithub.com%2Fblog%2F878-announcing-github-for-mac&date=2011-06-22)  

Surprising and delightful. They didn’t even bother to mention the lack of a Windows or Linux client - as if the reason for the absence of such was already obvious to members of their community.

It even works with non-GitHub repositories, although with some limitations<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>.

I love the idea that it has near-automatic sync with the web site, abstracting away details like push and pull. This is one of the first things new users to Git have trouble with: they clone a repository, make some changes, commit and push, only to be rejected with a ‘non-fast-forward’ error because someone pushed commits in the meantime. So they pull, which by (stupid) default, does a fetch-and-merge, making a horrible mess of the timeline<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>. Thus they have to learn to 'git pull –rebase && git push’ every time they want to push - a needless amount of busywork to bother the user with. If only the command-line had a 'git sync’ command that did this automatically.<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup>

GitHub for Mac also has an automatic behind-the-scenes stashing action when you switch branches, which I’ve always found was how users new to Git expected switching branches to work<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">4</a></sup>.

It is a bit [curious](http://twitter.com/ccgus/status/83680833914933248) that they used [Chameleon](http://www.webcitation.org/query?url=https%3A%2F%2Fgithub.com%2FBigZaphod%2FChameleon&date=2011-06-22), a library for easily porting iOS apps to Mac, when no such iOS app yet exists; but I won’t begrudge them that. But on a related note, I can’t help but notice that the app is very iOS-like, in that it has copious animations, and generally only shows one thing in the window at a time. This is a frequent complaint of mine in Git GUIs, even otherwise-nice ones like [Gitbox](http://www.webcitation.org/query?url=http%3A%2F%2Fwww.gitboxapp.com%2F&date=2011-06-22): I’m used to being able to easily flick through diffs of commits with a minimal number of clicks or key presses. With [GitX](http://www.webcitation.org/query?url=http%3A%2F%2Fgitx.frim.nl%2F&date=2011-06-22), my current (but sadly, apparently no longer maintained) GUI of choice, this is done via a split view, where I select a commit in the top list box, and the diff is immediately shown in the bottom; with GitHub for Mac, I have to double-click, and the list of commits is _replaced_ with the diff; Gitbox doesn’t display diffs on its own at all, instead launching FileMerge, which comes with Apple’s developer tools<sup id="fnref:5"><a href="#fn:5" class="footnote-ref" role="doc-noteref">5</a></sup>.

But the biggest thing keeping me from using it is the lack of a stage<sup id="fnref:6"><a href="#fn:6" class="footnote-ref" role="doc-noteref">6</a></sup>; maybe if I were a new user to Git, this wouldn’t bother me, but I’ve become so used to the power of being able to commit _only certain changes_ from a particular file - to shuffle changes back and forth across the stage in order to break things up into separate commits as I change my mind about what I need to do in the middle of my work - that I can’t do without it.

So for now, I suppose I will have to stick with GitX. But I eagerly await an actively-maintained replacement that will improve upon it<sup id="fnref:7"><a href="#fn:7" class="footnote-ref" role="doc-noteref">7</a></sup>. Maybe, eventually, that will be GitHub for Mac. And of course, I continue to use the command line, grudgingly, for things that GitX doesn’t do. While there is unlikely to ever be a GUI app that does it all<sup id="fnref:8"><a href="#fn:8" class="footnote-ref" role="doc-noteref">8</a></sup>, an app like GitHub for Mac seems like it might be able to reach 90% of use cases for most people. That in mind, I will certainly recommend it to new users, even over GitX, and I’m sure GitHub itself will be promoting it. Given the popularity of GitHub, I could see it quickly becoming the most popular version control client _anywhere_.

_This post was written too quickly and tiredly, doesn’t flow well and has way too many footnotes. Bah._

* * *

1. For example, it will only work with a single remote. This seems acceptable, as it is by far the most common use case; people I teach about Git (mostly Subversion converts) are invariably surprised to learn that more than one remote is possible.&nbsp;[↩︎](#fnref:1)

2. When I set up a Git server, I use an update hook I adapted from [the GNOME repository](http://www.webcitation.org/query?url=http%3A%2F%2Fgit.gnome.org%2Fbrowse%2Fgitadmin-bin%2Ftree%2Fpre-receive-check-policy&date=2011-06-22), which refuses a push that contains a merge-pull. It causes a lot of short-term pain, but in the long term it reduces confusion. It also causes angst about having to remember to use the ’–rebase’ switch with pull, but the way to make that work as the default for all branches is so ridiculously convoluted that I don’t bother explaining it.&nbsp;[↩︎](#fnref:2)

3. Yes, I _know_ you could make an alias to do it. Most users never will, nor should they have to. Software should address the most common use cases out of the box.&nbsp;[↩︎](#fnref:3)

4. The Git core team, which develops the command-line, is notoriously insensitive to requests for usability improvement. There is potentially an entire separate post about how dysfunctional it is. For an example, see [this mailing list thread](https://groups.google.com/d/topic/git-version-control/DDevdNxWYFU/discussion). I will also take this time to flaunt my exchange with [Wil](http://www.webcitation.org/query?url=http%3A%2F%2Fgit.gnome.org%2Fbrowse%2Fgitadmin-bin%2Ftree%2Fpre-receive-check-policy&date=2011-06-22) [Shipley](http://www.delicious-monster.com/) about it on Twitter: [[1]](https://twitter.com/wilshipley/status/44659237653184512) [[2]](https://twitter.com/dmdeller/status/44812916104495104) [[3]](https://twitter.com/wilshipley/status/44887323434942464) (Yes, I felt very special indeed.)&nbsp;[↩︎](#fnref:4)

5. This seems like such an obvious omission that I can’t help but think that a built-in diff viewer will appear in Gitbox soon. Perhaps at that time, I will give it another look. However, I can see how programming a diff view could be a difficult project to undertake.&nbsp;[↩︎](#fnref:5)

6. As noted in the thread from the earlier footnote, the 'stage’ concept technically does not exist in Git itself. Regardless, it’s based on concepts from the command-line program, and most other GUI clients offer it - with the notable exception of Xcode 4.&nbsp;[↩︎](#fnref:6)

7. I’ve only mentioned a few GUI clients in this post, but I’ve tried most if not all of the ones currently available for Mac.&nbsp;[↩︎](#fnref:7)

8. Even though the awful official Git GUI does try.&nbsp;[↩︎](#fnref:8)

