---
layout: post
title: iPhone's broken user-agent
date: '2007-06-20T16:21:10-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/3927762/iphones-broken-user-agent
---
A [user-agent](http://en.wikipedia.org/wiki/User_agent) string is how a web browser identifies itself to a web server.

Here’s the user-agent for Safari, running on the iPhone: Mozilla/5.0 (iPhone; U; CPU like Mac OS X; en) AppleWebKit/420+ (KHTML, like Gecko) Version/3.0 Mobile/1A538a Safari/419.3

There are soooo many things wrong with this.

1. Let’s start off easy: it’s perpetuating the ‘Mozilla’ spoof originated by Microsoft years ago in order to kill Netscape. Not to mention being a downright lie (both then and now) in that neither one has anything to do with Mozilla, it’s completely unnecessary these days. They should remove it completely and put the 'Safari’ string out front.  
2. 'KHTML, like Gecko’. This is similar to the above, in that it is designed to pass a test by stupid web developers who will only consider your browser compatible if it uses Mozilla’s Gecko rendering engine (used by Firefox, et al). It’s not even technically true any more, because while KHTML is sort of similar to Gecko, Safari uses WebKit, which was originally based on KHTML but is now something different from KHTML, because it does some things differently than KHTML does. 'AppleWebKit’ is the only accurate description.
3. 'CPU like Mac OS X’. Is this supposed to be some kind of running joke based on the above? Forgive me for stating the obvious, but _Mac OS X is not a CPU!_ So how can the iPhone’s CPU be 'like’ Mac OS X? This is likely here because of the tradition of putting the CPU type in the user-agent. Strangely, little more than a week before its launch, Apple has still refused to reveal what kind of CPU is in the iPhone. Whatever, guys… so why not just leave this part out?
4. 'Version/3.0’. ARGH WTF. The entire format of every other user-agent, including this one, so far, is: Product/version. So tell me, exactly which product do you have that’s named 'Version’?
5. 'Mobile/1A538a’. See above.
6. 'Safari/419.3’. This is where the '3.0’ should go: Safari/3.0. There, that’s not so bad, is it? Oh, okay, I know, Apple really loves their internal build numbers, even though you can already get that information from the AppleWebKit string. So look, if they really want the build number in there, fine, this isn’t a difficult problem to solve; even Microsoft was able to figure it out: Safari/3.0.0.419.3.
Such a mess. (via [Ars](http://arstechnica.com/journals/apple.ars/2007/06/19/iphone-development-details-leaking-out-of-the-internet-tubes))
