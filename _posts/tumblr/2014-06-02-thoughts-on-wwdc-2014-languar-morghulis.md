---
layout: post
title: 'Thoughts on WWDC 2014: Languar Morghulis'
date: '2014-06-02T22:02:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/87654173562/thoughts-on-wwdc-2014-languar-morghulis
---
### Surprise, Surprise

In my [wish list](http://blog.horizon-nigh.org/2014/06/01/wwdc-2014-wish-list.html), I put a bunch of things that I thought were unlikely but still hoped for. But the theme of today’s keynote, for me, was things that I had been having problems with for years, but I thought were so far out of the realm of possibility that it didn’t even occur to me to _wish_ for them. Which is not to say that I got everything I wanted–far from it. But many of the things they did announce were genuinely delightful.

### [Swift](https://developer.apple.com/swift/)

‘Objective-C without the C.’ That’s all they really needed to say.

I, and many others, have been hoping for such a thing for years. In fact, it seemed inevitable: all languages must die, and Objective-C has surely been showing its age. And yet, something that you know must be coming someday is nevertheless surprising when that day suddenly turns out to be… today. In typical Apple fashion, no-one had the slightest clue beforehand. A programming language, developed in secret over years, and unveiled with Apple-level presentational polish and marketing flourish: that has to be a first, right?

I’ve only just barely had a chance to skim the [book that Apple published](https://itunes.apple.com/us/book/the-swift-programming-language/id881256329?mt=11) about the language, but so far I like (most) of what I see. Of course, I have some complaints already: some poorly-named keywords (`let`, `func`) and questionable whitespace choices in the example code. But there’s a lot to like–for example, the type inference system looks great, a terrific compromise between the desire to avoid writing types all the time, but still having (optional?) compile-time type checking of method parameters. Overall, I like what I see. I’m extremely excited and ready to start writing in this language **_now_**.

It’s become an old trope now to contrast Apple with Google, but people are already pointing out Swift’s similarity to [Go](https://en.wikipedia.org/wiki/Go_language). I’ve never programmed in Go, so I wouldn’t know. But, just look at the difference in how the two were developed: Google decided to boil the ocean and start with something completely from scratch, free of any ties to all existing platforms. Apple started by taking their existing language, Objective-C, and writing a new compiler for it. Now having expertise in the realm of compiling the language, they looked at what they could do to improve the most common pain points in the syntax and developer tools. Finally, they took that expertise to leave the existing syntax behind, resulting in something with concepts and mechanics that made Objective-C great, but (hopefully) none of the baggage. Swift, rather than being entirely new (although it looks that way on first glance), is simply the latest round in a very long series of iterations. It’s a huge iteration, much larger than anything previously seen from the company, but an iteration just the same.

And the result is the magic feature that will make this all work: Swift seamlessly interoperates with existing Objective-C and C code. Developers don’t have to throw away all of their existing code. They can, from their shiny new Swift code, continue calling and using useful external Objective-C libraries (_à la_ the increasingly-ubiquitous [CocoaPods](http://cocoapods.org), no doubt). They can dip their feet in, and learn as they go, while continuing to produce useful work the entire time. It’s almost impossible to see how there would be any possibility of widespread developer adoption, were this not the case.

And where to go from here? The biggest question on my mind is whether or not the compiler is going to be open-source. I know it’s built on [LLVM](http://llvm.org), which already is. But just imagine the possibilities: We could be writing in the same language on both iOS and server-side… and maybe even other platforms?

The future’s an exciting place to be.

### OS X Adirondacks

Please sit back and relax. For your comfort and convenience, I have translated the product name into another awkward plural.

I’ll confess: last night, I got the fear. I was remembering iOS 7’s launch, and I broke out in a cold sweat. _I saw what happened last year_, I grumbled to myself as I paced around my living room at midnight, shaking my head and sighing. _You guys keep your hands off of my Mac!_

But…it’s okay. I looked at it today, and I felt okay. I’m looking at it now, and I still feel okay.

I’m not a designer (a fact that is constantly frustrating). I can’t tell you the right amount of shadows to put on something, or which colours will go right together. The best I can do–and I really try hard at this, to an often absurd degree–is to take a frame of reference, like Apple’s design guidelines…and imitate them as closely as possible. I am a programmer, and I know how to read a spec, and to adhere to that spec like the cruellest, most exacting drill sergeant you’ve ever seen. I can see when a single pixel is off. And I know how to pick up on _conventions_, when the best apps all come together to agree on rules without ever writing them down or even verbally discussing them, and to replicate those same ideas in my work. But I have absolutely no eye for _art_; for creating something new and visually-pleasing out of nothing. I never could do it.

What I’m trying to get at is that I can’t tell you _why_ OS X 10.10 looks good or not, and even if I could, you shouldn’t listen to me. But I _do_ know when I look at something whether I like it or not. And, now that I can look at this instead of just worrying about it, I’m not afraid any more.

Also, these smart people seem to agree:

> Awesome features. Color. Shadow. Depth. Friendly and not garish. Great work by everyone at Apple who designed Yosemite and made it work.
> 
> — Sebastiaan de With (@sdw) [June 2, 2014](https://twitter.com/sdw/statuses/473520868811751425)

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

> (The new icons seem to have balance iOS 7 should’ve. Flatter, but still with some texture and life. Shadows, ok. Rich leather, no. Color. 👍)
> 
> — Cabel Sasser (@cabel) [June 2, 2014](https://twitter.com/cabel/statuses/473551930242138113)

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

So there you have it.

_OS X: It’s going to be okay.™_

> I am ok with this.
> 
> — Steven Frank (@stevenf) [June 2, 2014](https://twitter.com/stevenf/statuses/473515515801899008)

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
### Everything Everywhere

When I’m working, I use my Mac. When I’m out, I use my iPhone. When I’m home relaxing, I use my iPad. And yet… even inside my home, I carry two devices around with me at all times: the iPhone and the iPad. _Just in case_ I were to receive a phone call or one of those infernal green-bubbled messages. I should really only need one device at a time, but… this is one of those things that it just never occurred to me that Apple would try to solve. Sure, the technology is all there, but it’s just one of those intractable the-way-it’s-always-been type things. So I’m happy that it’s getting solved, even if it wasn’t really a huge deal.

The rest of the Handoff stuff doesn’t sound like it’s solving a problem that I personally have very often, but it makes sense, I suppose.

[iCloud Photo Library](http://www.apple.com/ios/ios8/photos/) is so very late in coming that I thought we would never get it, to the extent that I didn’t even put it on my wishlist. But I am glad it’s here. [Picturelife](https://picturelife.com) (which I currently pay for, though probably not for much longer) just got [Sherlocked](https://en.wikipedia.org/wiki/Karelia_Watson); it seems photo management startups must be [cursed](http://www.theverge.com/2013/11/5/5039216/everpix-life-and-death-inside-the-worlds-best-photo-startup). Anyway, Apple is being extremely cagey about pricing options, and I’m not sure why; the prices shown during the keynote are nowhere to be found on Apple’s web site, as far as I can tell. It looked like you would still only get 5 GB of total iCloud storage for free, which is shared with Photo Library and all other iCloud features. I worry that many users will fill this up very quickly and then refuse to pay anything, unknowingly putting themselves at risk of losing their photos when they lose/break/replace their iPhone. Google, of course, is happy to keep all of your photos forever for free, because Google wants your photos. Apple doesn’t want your photos; they’re doing this as a favour to you, or because they feel like they have to provide this feature in order to remain competitive. This reluctance does not bode well.

And finally, [Family Sharing](http://www.apple.com/ios/ios8/family-sharing/) is yet another thing I thought we’d never see. The situation with iTunes purchases has been stuck in impractical metaphor of '1 purchase = 1 person = 1 ID’ for so long, and it was surely mired in legal problems courtesy of movie studios and record labels that seemed far beyond Apple’s ability to fix. But here it is, and yet…there’s a worrying disclaimer in the fine print of that page, to the effect that maybe not everything actually can be shared. We’ll just have to see, I guess. Oh, and under the same product banner, are we also replacing Find My Friends? If it makes people less likely to forget that that functionality exists (which, in my experience, everyone does), then I guess it’s a good thing.

### Grab Bag

What else did I get?

- Per-app battery power usage: [Yep.](http://www.macrumors.com/2014/06/02/ios-8-tidbits/)
- Inter-app communication: [Yep.](https://developer.apple.com/ios8/)
- T-Mobile Wi-Fi calling: [Surprisingly yes!](http://www.macrumors.com/2014/06/02/ios-8-tmobile-wifi-calling/)
- DuckDuckGo in Safari: Even more surprisingly yes! Well… [on OS X, anyway](https://twitter.com/duckduckgo/status/473548816239824896). But maybe also iOS?

I’ve seen nothing public either way about a bunch of the other stuff, so it’s possible more info will come out in the coming months. (Of course, I have developer access to the betas, but I’m prohibited from writing about it.)

It seems like there’s a lot of new stuff with iCloud, but I’m not quite sure what to make of it yet. CloudKit in particular is somewhat baffling, as it seems to overlap with parts of Core Data, but is incompatible with Core Data. Is Core Data being deprecated? Or merely the interaction between Core Data and iCloud? Hopefully someone who understands this can write up an explanation, or perhaps I can get a better understanding from a WWDC session. In any case, iCloud still doesn’t have a very good reputation with developers at this point, so it’s difficult to get very excited about it.

I didn’t really expect Apple to do anything about the sad state of App Store games. To the contrary, the very first thing they showed, an introduction video, specifically singled out Candy Crush by name for praise. I don’t know what else to say about this that hasn’t already been said. It’s just really unfortunate that Apple doesn’t seem to recognise this problem.

As for Apple TV, well… there was so much other stuff today. But I haven’t forgotten.

