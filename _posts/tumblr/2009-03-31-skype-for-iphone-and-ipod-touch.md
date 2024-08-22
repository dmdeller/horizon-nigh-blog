---
layout: post
title: Skype for iPhone and iPod touch
date: '2009-03-31T23:40:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/91783859/skype-for-iphone-and-ipod-touch
---
[Skype for iPhone and iPod touch](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=304878510&mt=8)  

If I take out my iPod touch in public, someone inevitably asks me ‘is that an iPhone?’ To which I answer, 'no, it’s an iPod touch.’ After the resulting blank look, I elaborate: 'it’s like an iPhone, without the phone. It does many of the same things, like browse the web, check e-mail, and of course play music; but it does not make phone calls.’ I used to add something like, 'it runs iPhone OS’, but that did not seem to help get the idea across.

I only mention this because it is sort of remarkable to me that I’ve had this exact same conversation so many times. People are both aware and interested enough in the iPhone as a brand to recognise an iPhone-like device and even enquire about it, and are also surprised to learn that Apple also makes a similar device that is not a phone.

Now, however, my explanation will be complicated somewhat. Together with the aforelinked app, my existing [SkypeOut](http://www.skype.com/allfeatures/callphones/) account, and a pair of [Apple Earphones with Remote and Mic](http://www.amazon.com/Apple-Earphones-with-Remote-Mic/dp/B001NABJ56), the device is in fact an iPod that is not an iPhone but does make phone calls (but does not properly receive them - we’ll have to wait till iPhone OS 3.0 for that). I am not sure how I will explain this in an easily-digestible&nbsp;form the next time I am asked. And don’t even get me started on cellular vs. WiFi, because by that point I am no longer answering a simple question but delivering a lecture.

But all of this is neither here nor there. My iPod makes phone calls now. That’s pretty cool.

However, the plot thickens:

> Please note: Skype is not responsible for errors or crashes which result from changes in the underlying iPhone OS.

An odd thing to say. Two possibilities come to mind:

1. Skype have very little confidence in Apple’s software; perhaps they have been reading too much of the sensationalist side of the web-o-tron. They only begrudgingly came out with this app at all since their users&nbsp;[just wouldn’t stop nagging them for it](http://news.bbc.co.uk/2/hi/technology/7971673.stm), and their you-asked-for-it attitude is reflected in this almost cheeky advisory. In this case, their words are meaningless, and there is nothing to worry about. As long as Skype use only public, documented APIs, like Apple tells you to do and like most developers obligingly follow, it is unlikely (although not impossible) that their software would break in a future version of iPhone OS. The entire point of public APIs is that they are a promise from Apple that the functionality will continue to work indefinitely, or, failing that, developers will have ample advance notice if they do ever change.
2. Skype are using private APIs, and they at least have the foresight to realise that this is probably going to break their app sooner or later (the promise, as above, does not exist for private APIs; on the contrary, private APIs are almost a promise that things _will_ break). Skype have decided to go ahead and do this anyway, for whatever reason, and are trying to shift blame away from themselves. I can only speculate on why they would use private APIs, but my guess would be that it would have something to do with emulating the iPhone’s own native Phone application more closely, which may not be possible with Apple’s sometimes-limiting public APIs. I hope this isn’t the case, because in this light, the 'note’ as worded would be downright dishonest: using private APIs or not is a conscious choice on the part of the developer, and the responsibility for this choice very much lies with those who make it.

Either way, I am surprised that Apple let this slip without comment, although stranger things have come out of Apple’s review process.

**Edit:** [this Ars Technica article](http://arstechnica.com/apple/news/2009/04/review-skype-finally-does-voip-right-on-the-iphone.ars) brings up another possibility, which admittedly is the most likely of them all:

1. If you ['jailbreak’](http://en.wikipedia.org/wiki/Jailbreak_(iPhone)) your device and install non-Apple-sanctioned software, it can apparently cause Skype to crash or behave strangely. You’d be a complete moron to complain to Skype if you do this, but of course people will do it and then complain anyway. I would suggest that Skype be more clear about what they’re talking about in this case, but I’m sure there’s a line in Apple’s agreement that says you can’t even acknowledge the existence of 'jailbreaking’, or something.
