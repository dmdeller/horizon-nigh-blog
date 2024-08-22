---
layout: post
title: iOS 7 displays Retina versions of iPhone apps on non-Retina iPads
date: '2013-07-09T21:07:05-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/55045121168/ios-7-displays-retina-versions-of-iphone-apps-on
---
[iOS 7 displays Retina versions of iPhone apps on non-Retina iPads](http://www.macrumors.com/2013/07/09/ios-7-leverages-retina-iphone-app-assets-to-improve-2x-mode-on-non-retina-ipads/)  

The comments attached to this article<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup> express bemusement on why such a seemingly simple thing wasn’t done sooner. The answer, of course, is that it’s not simple.

Here’s the problem domain: A non-Retina iPad has a screen that’s physically about twice as big (by single dimension) as an iPhone, yet has half the pixel density as a Retina device, for an overall total of roughly the same number of pixels of a Retina iPhone. Therefore, you want to be able to show Retina graphics when an iPhone app is running in 2x mode, but not when it’s in 1x mode.

There is no way to do this. iOS apps rely heavily on bitmap graphics, which are are loaded when a view first appears, and then not again, unless the app specifically wants to. You have to start the app either in Retina mode, or non-Retina mode, and then stay in that mode as long as the app is running; you can’t change midway, because the signals to tell an app that this kind of a change has occurred don’t even exist<sup id="fnref:1.5"><a href="#fn:1.5" class="footnote-ref" role="doc-noteref">2</a></sup>. The reason they don’t exist is because in the context of an iPhone, it makes no sense: Retina status is an aspect of the physical hardware, and is therefore immutable. And it wouldn’t be worth the engineering resources to add this kind of Retina-mode-change-signal into the frameworks now, nor would it be worth the developer outreach efforts and compatibility frustrations to get every single App Store developer on-board with the change–look how many apps still don’t even support iPhone 5!<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">3</a></sup>. Would that many developers rush to support such an iPad-specific edge case, especially considering these are developers who apparently haven’t bothered to support the iPad within the past three years?

In theory, you could always start in Retina mode, and then shrink everything by 50% for ‘1x’ mode (in reality, it would be an 0.5x-of-Retina mode). But the entire point of having Retina graphics is that you can optimise all of the artwork for the actual pixels of the screen. Remember, this is iOS, where everything is bitmaps! A good icon designer will not simply draw an icon once at the highest resolution and then scale it down; they will actually manually draw from scratch–or at least heavily tweak–each and every one of the different sizes, so that they look ideal at every possible resolution. And now you want to destroy their carefully crafted work by turning all of those one-pixel lines into a blurry, anti-aliased mess? Not on Apple’s watch.<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">4</a></sup>

This is why the solution that Apple went with in iOS 7 completely removes the 1x/2x toggle button on non-Retina iPads–you either get Retina mode always, or never. In iOS 6, it was never; in iOS 7, it’s always. There is no middle ground.

For Retina iPads, I surmise, the behaviour is unchanged from iOS 6–they’ll show Retina graphics at 1x, because why wouldn’t they?–but at 2x, you’ll see pixel-doubled Retina graphics, because there just isn’t any bigger 'x’.

Arguably, the way it was in iOS 6 and earlier was simpler for users to understand: All iPads, Retina or not, had a toggle button that displayed an app at the device’s native resolution at 1x, and pixel-doubled at 2x. This change allows non-Retina iPad users to see better graphics, at the expense of making the overall situation more confusing for everyone. I’m not saying the decision was wrong, only that both solutions have downsides and there is no clear winner.

Not a simple as you thought, is it, dear user? Welcome to my world. Please remember this the next time you’re thinking of beginning a sentence, 'why can’t you just…’

_I haven’t personally tried any of this on iOS 7, so all of the above info is either gleaned from the MacRumors article or from my personal experience developing for iOS 6, which, in either case, may be wrong._

**Edit:** It later occurred to me that this change allows developers to make **Retina-only** apps for the very first time, but only under the following conditions:

1. The app has no native iPad support (iPhone only)
2. The app requires iOS 7

Under these two conditions, a developer can safely remove any and all non-Retina assets or code, and go Retina-only for their iPhone apps, because as of iOS 7, it is guaranteed that iPhone apps will never ever run in non-Retina mode, regardless of device. The same is **not** true of iPad apps.

This is almost certainly the reason why Apple made this change.

* * *

1. Side note about the original, unnecessarily obtuse MacRumors headline: Almost anywhere you see the words 'leverage’ or 'utilise’, you can substitute the much simpler word 'use’, for a sentence that has the exact same meaning yet is much faster for readers (or listeners) to understand. The purpose of language is to communicate, not to make yourself look smart.&nbsp;[↩︎](#fnref:1)

2. In theory, you could just wait for the view to change as a result of a user action (e.g., the user navigate somewhere else within the app) before changing the mode from or to Retina. But in the meantime, the app would look awful until the user just happened to do something to cause a different view to appear, and they likely wouldn’t understand what was going on at all. Not a good experience.&nbsp;[↩︎](#fnref:1.5)

3. Yours truly being only one such egregiously guilty party.&nbsp;[↩︎](#fnref:2)

4. See what I did there?&nbsp;[↩︎](#fnref:3)

