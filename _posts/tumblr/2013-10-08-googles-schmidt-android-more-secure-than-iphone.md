---
layout: post
title: 'Google''s Schmidt: Android more secure than iPhone'
date: '2013-10-08T11:47:26-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/63471567278/googles-schmidt-android-more-secure-than-iphone
---
[Google's Schmidt: Android more secure than iPhone](http://www.zdnet.com/googles-schmidt-android-more-secure-than-iphone-7000021670/)  

To an extent, this is an amusing anecdote about how out-of-touch Schmidt is. But to be fair, there may well be a genuine disconnect between what Schmidt thinks ‘secure’ means, versus what everyone else thinks it means.

Android’s security is based around blaming the user. 'But you _said_ it was okay for this malware to have root access, you clicked OK!’

To wit:

1. When installing an app, Android requires the user to accept the app’s requested permissions before it even starts, as a _precondition_ for installing the app. If the user declines those permissions, the app will not install. This dialog is an interruption–it is getting in the way of what the user wanted to do. The obvious result is that it trains users to click OK just to get past it to the thing that they wanted in the first place.

2. Android requires the user to accept _all_ of the permissions an app asks for, or none of them. There is no way to accept only the permissions the user wishes, while declining others. This allows developers to demand unreasonable permissions that they don’t actually need, because they’re holding the entire app hostage from the user. And so–surprise!–many developers on Google Play do exactly that.

3. iOS simply forbids the most dangerous types of actions, like root access to the file system or access to phone call or SMS data. There is no permission dialog for these; they are simply disallowed, both in terms of the APIs not being available for use, and by Apple’s review policy.

Theoretically, Android may have the best security system in the world. But it all falls apart when you wrap it around a horrible UI that not only allows the users to shoot themselves in the foot by overriding the protections, but trains them to do it _constantly_ as a matter of routine operation. It may as well not even exist.

This is why, in practice, Android has a malware problem. But it doesn’t surprise me that Eric Schmidt wouldn’t see it this way. It’s reflective of Google’s culture as a whole, which seems to champion engineering above all else.

But the more concerning thing should be that the company (or at least their effective spokesperson, Schmidt) doesn’t even acknowledge the existence of the problem. Yes, it was an antagonistic question and he had to answer in a way that paints his company in a positive light. But he could have given any number of placating non-answers to this question<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup> which would have resulted in it being a complete non-story that nobody would be talking about today.

Instead, he drew even more attention to the problem, and the fact that Google doesn’t seem to be fixing it. Because you can’t fix something if you don’t even realise that it’s broken.

* * *

1. I know someone who uses Google Maps on iOS this way, because she doesn’t trust Google to know her location. It makes me crazy to watch her use it this way, but the point is that it’s her choice and that’s what works for her. The device should do what she wants, not the other way around.&nbsp;[↩︎](#fnref:1)

2. The typical corporate P.R. handbook response is to ramble on with a whole bunch of fluff that means nothing, doesn’t address the question at all, and will make your audience fall asleep listening to it. But that’s not the only way. Consider Tim Cook’s response to Sen. John McCain’s off-the-cuff question about why he has to manually update the apps on his iPhone; Tim said, 'We’re trying to make them better all the time.’ Simple and to the point. Keeping the message positive, while acknowledging room for improvement. Was that so hard?&nbsp;[↩︎](#fnref:2)

