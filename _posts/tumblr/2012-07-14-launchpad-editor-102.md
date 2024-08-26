---
layout: post
title: Launchpad Editor 1.0.2
date: '2012-07-14T18:12:00-07:00'
tags:
- launchpad editor
tumblr_url: https://blog.horizon-nigh.org/post/27217760126/launchpad-editor-102
---
[Launchpad Editor 1.0.2](http://horizon-nigh.org/launchpad-editor.html)  

Changes in this version:

- Fixed a bug that would sometimes result in a crash or freeze when dragging an item to the last position in a page or group
- Fixed compatibility with Launchpad on OS X 10.8 Mountain Lion
- Added compatibility with Gatekeeper

Update note: Some people have had issues with the ‘check for updates’ menu item ([Sparkle](http://sparkle.andymatuschak.org)) in the past. It seems to be working now, but if you don’t see the update, you may need to download the new version manually.

Developer note: The source code for this version is not yet public, because the 10.8 GM is still NDA’d. When 10.8 is released to the public, I will upload the source code to GitHub.

## The gated road to the future

Let’s talk about that last change.

Developer ID is Apple’s new program that allows Mac developers to sign apps for Gatekeeper without going through the Mac App Store. As we know, 10.8’s Gatekeeper feature will, by default, only allow users to install apps that are either (1) from the App Store, or (2) signed with Developer ID. This has been widely hailed as a developer-friendly move, allowing us to continue to create apps (such as this one) which are not possible in the App Store and do not go through Apple’s review process. [(Much more in-depth explanation here from Steven Frank.)](http://www.panic.com/blog/2012/02/about-gatekeeper/) Up to this point, I have felt that it is a good solution.

But for some reason, I was under the impression that Developer ID was available to anyone with a free Apple Developer account<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>. In making my app ready for Gatekeeper, I discovered that this is not the case; it requires a $99 annual Mac Developer Program membership, which is the same program that allows you to publish to the Mac App Store. I have not seen it reported anywhere, but it seems significant that Apple has quietly started requiring $99 from all Mac developers who publish free apps, including those outside of the App Store.

This presented a quandary for me: I was not already a member of the Mac Developer Program, only the iOS Developer Program, which is a separate $99; I have no plans to put anything in the Mac App Store; and I obviously don’t make any money from Launchpad Editor. Is it worth it to me to pay $99 to have my silly hobby app keep working for a year? This is a question I imagine many other developers are asking themselves right about now.

I could do nothing, and allow my users to see scary blocking errors when they try to download my app; this will surely be the case for many existing free apps that are floating around out there and will never see another update. I could even give specific instructions on how to override the errors and install it over the operating system’s protestations–I am sure some developers will try this technique, too, and test their users’ trust in Apple versus their desire for free stuff. Or I could just leave to the user to figure out on their own–considering Launchpad Editor’s primary audience (technical users), this probably isn’t a giant leap. But either way, I would consider the result to be an unacceptably bad user experience. I decided I would rather remove the app entirely than allow this to happen.

So it was kind of a toss-up, but in the end I decided that $99 isn’t a terrible expense for a hobby<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">2</a></sup>…for now.

Curiously, the Developer ID certificate I was issued lists an expiration date five years from now–this is in contrast to the App Store certificates (for both Mac and iOS), which expire after one year. My Mac Developer Program membership, however, expires in one year. So I’m not entirely sure what will happen if I let the program membership expire and then try to use the certificate again. In theory, it should still work, but I have not been able to find any documentation about this.

So, honestly, I don’t know what will happen a year from now. I joined the program mainly to avoid feeling like I was losing the work I have already put into it, but at some point, it’s not going to be worth it any more.

## Planned obsolescence

Finally, as a registered Apple developer, I can’t yet talk about what I may or may not have seen in Mountain Lion, since that’s still under NDA. But I will say, based on [what Apple has publicly revealed about Launchpad in 10.8](http://www.apple.com/osx/whats-new/features.html#launchpad), I’m disappointed to see very little apparent progress–only one change is listed on that web page, and it’s only a search feature, which is redundant to Spotlight. The whole reason I use Launchpad is because I don’t want to type! [I was hopeful](/2011/12/20/launchpad-editor-10.html) last year when I first created Launchpad Editor that the need for my app was temporary, and it would soon be made unnecessary. Sadly, that does not seem to be happening. It’s hard to imagine that Apple can’t think of any way that Launchpad could be improved, so I guess the other explanation is that they just don’t care very much about the feature.

* * *

1. This is one of those maddening times where I’m sure I read this somewhere, maybe even just on Twitter from someone whom I considered a reliable source of information–but I can’t find any trace of it any more. (Of course, Twitter’s horrible search combined with their lack of anything resembling an archive doesn’t help.) If anyone can find a citation for this, it would make me feel less crazy.&nbsp;[↩︎](#fnref:1)

2. Insert Apple TV joke here.&nbsp;[↩︎](#fnref:4)

