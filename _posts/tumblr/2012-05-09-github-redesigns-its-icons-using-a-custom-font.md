---
layout: post
title: GitHub redesigns its icons using a custom font
date: '2012-05-09T23:27:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/22761621054/github-redesigns-its-icons-using-a-custom-font
---
[GitHub redesigns its icons using a custom font](https://github.com/blog/1106-say-hello-to-octicons)  

It’s an interesting and novel technical approach, but I can’t help but ask: why?

The obvious answer, and the one GitHub gives in their blog post, is that with newer higher-resolution screens becoming popular (namely, iPhone and iPad), it’s necessary to have higher-resolution icons that look good on those screens.

But that still doesn’t answer: why a font, as opposed to some other way of accomplishing the same thing?

The approach Apple itself takes is to create two sets of images: a ‘normal’ size and an ’@2x’ Retina size. 'But wait’, I can just imagine the engineers saying, 'surely there will be more than just two different sizes in the future! We should be able to support any arbitrary size!’

## Count the resolutions, count 'em!

_Any_ size? Well, actually, probably not, no. Device makers have been trying to support arbitrary-depth resolutions for ages. Have you ever tried to use Windows in something other than its default DPI? It’s a miserable experience. From what I hear, the variety of screen resolutions on Android, along with that OS’s handling of them, has created a similarly messy situation.

Mac OS X has had rudimentary support for arbitrary DPIs since near the beginning, but it was never enabled for or accessible by ordinary users for good reason; and now it looks like Apple is abandoning that approach entirely, not just on iOS (where shipping Retina devices already exist) but on the Mac as well, actually _removing_ support for arbitrary DPIs in favour of having two modes only: 'normal’ and HiDPI (pixel-doubled, same as Retina).

It’s pretty clear where Apple is going with this: pixel-doubling or nothing. But isn’t it possible that we might someday pixel-double the Retina screens, to get ’@4x’ versions? Well, probably not. Certainly the technology will advance to this point, but the human eye is unlikely to improve. It’s called Retina for a reason: it’s already (if you believe the marketing) at the limits of human perception. There’s no reason to increase the resolution further, because you wouldn’t be able to see it.

So, Apple is limiting themselves to multiples of two, while the rest of the industry fumbles and can’t seem to get anything to work right. We can safely assume that eventually ’@2x’ will become the normal ’@1x’ and we’ll be back only needing one size of icons for everything, and due to the human eye remaining constant, we’re unlikely to double the resolution again.<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>

## Pros and cons

But, for the sake of argument, let’s throw out everything I wrote under the previous sub-heading and posit that for some reason, we really do need arbitrary-resolution images. Or maybe it’s not even that we _need_ them, we just really _want_ them, because engineers love the idea of vector images: vectors have a certain purity of essence, made from a mathematical formula that is capable of scaling to any size, just like your Rails app (_cough_).

Why not just use SVG?

Maybe browser support for SVG isn’t great; I haven’t looked recently. But I’m sure there are polyfills and fallbacks.

Maybe your designers complain that vector images look mushy at small sizes (a legitimate complaint that any engineer working with icons should be aware of!). I believe that font rendering may have a built-in advantage here, as font designers have had to deal with this issue for quite some time; but I’m also quite sure that you could cook up some not-too-complicated combination of JavaScript and CSS to swap in bitmap images at smaller sizes, while using the equivalent vector once it grows beyond a certain threshold, similar to the approach Apple uses for @2x images on apple.com, giving your designers total control.

In short, maybe it’s just _easier_ to implement as a font. To an engineer, easier means less code, and less code means _cleaner_, and cleaner means more pure, and is very appealing. I can understand this.

But using fonts has one huge drawback:

_You can’t use colours._<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>

## Black and white

Maybe this started as a design decision: that the new icons would be completely monotone because the designers simply preferred it that way. But even if that was so, it’s incredibly limiting to your future design choices to allow your technical system to lock you into forever using monotone icons. As an engineer, you _always_ have to be thinking of how the evolving needs of the product might require the system to behave differently in the future. And this leads me to wonder if the decision to use monotone icons at GitHub was driven by engineering desires rather than design considerations.

And so the only answer to my original question that I can think of would be: _They used a font simply because it seemed like an interesting and novel technical approach._

And it makes me sad, because I look at the folder icons, and can’t help but think how flat and lifeless they look, and really the only thing they need is some shading to give them depth, and how they looked so much better just this morning, and how they will never be improved as long as they continue with this technical approach.

And so, while I love playing with fun new technology as much as the next engineer, I think products should be driven by design.

* * *

1. Yes, it can be dangerous to make a prediction like that, but consider how long we were all using 72 DPI screens. The original Macintosh came out in 1984, and the iPhone 4 (the first widely-used web-capable Retina-class device; enough qualifiers for you?) was 2010, so we can conservatively say at least 26 years–in all likelihood, probably longer, depending on how much further back than the Macintosh you think it’s reasonable to look.

2. Which is to say that, with a font, you can’t use multiple colours within the same icon. You can, of course, take a monotone font-rendered icon and set its colour to, for example, red or blue, but that changes the _entire_ icon; you can’t have different parts of the icon use different colours, or use shading. This could almost be an advantage: being able to change the colour of an icon in CSS instead of having to go back and edit the source image. And yet, how often do you really need to do this? Not enough for it to be worth the trade-offs, I think.&nbsp;[↩︎](#fnref:2)

