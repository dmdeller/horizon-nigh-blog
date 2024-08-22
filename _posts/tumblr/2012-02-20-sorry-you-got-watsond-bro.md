---
layout: post
title: Sorry you got Watson'd, bro
date: '2012-02-20T09:18:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/17945393998/sorry-you-got-watsond-bro
---
I’m showing my age at this point, but Apple has a history of integrating features into the OS that were once third-party utilities. Perhaps the most notable examples of this are [Watson](http://en.wikipedia.org/wiki/Karelia_Watson), which became Sherlock, and [Konfabulator](http://en.wikipedia.org/wiki/Konfabulator), which became Dashboard.<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup> And when I say ‘became’, I mean completely new, clean-room implementations of these features, with no knowledge, involvement, or compensation on the part of the original developers. I think it’s that last part–compensation–that really gets people, because there’s this persistent notion that [ideas are currency](http://blog.horizon-nigh.org/2011/07/30/matt-legend-gemmell-makers-and-takers.html).

On the other hand, there are also examples of Apple hiring or acquiring third-party developers to similar ends: a particularly relevant example would seem to be the hiring of [this guy](http://techcrunch.com/2011/06/03/apple-hires-the-guy-who-hacked-together-a-better-ios-notifications-system/), who wrote a notification system for jailbroken iPhones before Apple’s own version existed, and then ended up (presumably) creating the official version at Apple’s invitation. There’s also the story of how Steve Jobs [tried to acquire Dropbox](http://www.forbes.com/sites/victoriabarret/2011/10/18/dropbox-the-inside-story-of-techs-hottest-startup/) when creating iCloud, even though it turned out that Apple’s plans for iCloud were very different from what Dropbox was doing.

So I can see why it would be frustrating for the Growl team to see Apple copy their product<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>, after it has been almost a de facto first-party system component for so many years, and after they’ve reportedly<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup> implored Apple for years to integrate Growl into the OS proper. But Apple never seemed to care how many people used Growl, or think it was a necessary UI feature, until after it showed up in iOS and they started the 'back to Mac’ strategy. So I can see how a measure of flippancy might be in order. Yet still, I’m a bit surprised by the 'full steam ahead’ tone in [Chris Forsythe’s response to Apple’s announcement](http://growl.posterous.com/growls-response-to-notification-center-welcom) of Notification Center; it seems obvious to most people not invested in the situation that Growl is over.

Despite the fact that, only just recently, I spent many hours learning Mac Cocoa in order to write Launchpad Editor<sup id="fnref:6"><a href="#fn:6" class="footnote-ref" role="doc-noteref">4</a></sup>, it’s my hope that Apple improves Launchpad enough to make my app unnecessary. Perhaps I would feel differently if I actually made any income from Launchpad Editor, but the way I see it, there are always new and more interesting things to work on.

## Don’t let the man

There was some further drama about a rumour that Notification Center would only be available to apps on the App Store. I thought I remembered seeing this in Forsythe’s post, but either the post has been edited to remove this assertion, or I remembered incorrectly. Regardless, the rumour turned out to be wrong, as [AnandTech explains](http://www.anandtech.com/show/5545/mac-os-x-mountain-lion-developer-preview/4):

> There’s been a bit of confusion about the new notifications API (NSUserNotification) and whether or not it’s available to applications not in the Mac App Store. Local notifications using the new API are available to third party apps regardless of their distribution model (they don’t need to be in the Mac App Store). Push notifications on the other hand currently require that the application is distributed only through the Mac App Store.

This makes perfect sense to me, as a developer: the API is part of the OS, so why not let any developer use it? It doesn’t cost Apple anything to do so; it would actually be _more_ work to limit use of the API to only certain types of apps.

But Push Notifications are something different. It’s not just a hook into the OS; all Push Notifications go through Apple servers before reaching their destination.<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">5</a></sup> These servers have a monetary cost associated with them for Apple to maintain. Now, Apple makes money on the App Store, so it’s reasonable that they have some left over to reinvest in the servers that make this work. Even if an app is given away for free or doesn’t make much profit, Apple still at least has the $100/year for the developer program. Over the entire App Store, it probably balances out.

But why should Apple provide this service, which makes apps more appealing to users, for _free_ to developers who aren’t contributing anything at all? Keep in mind that these developers don’t have to go through app review, and don’t have the technical restrictions inherent in App Store apps either; it would be entirely feasible for such developers to make their own Push Notifications service that doesn’t go through Apple, and run a background daemon on the Mac which listens for messages and forwards them to Notification Center. (It’s up to the user to decide whether they like the idea of yet another background daemon.)

The same arguments could be made about iCloud, for that matter. As a user, I’m very sensitive about what’s happening to my ability to run any software I want on my Mac. But for the moment, the outrage about certain features only being available to App Store apps seems overblown to me.

## Hey, listen! Hey! LISTEN!

Personally, I find there are very few things I actually need or want notifications for. I’ve developed a habit of saying 'no’ at first to all notification dialogs on iOS, and then going back and turning them back on later if it turns out I need them–not least due to the increasing prevalence of their use for spam. And on the Mac, I’d have uninstalled Growl completely, if not for the fact that so many apps bundle Growl and continue to use it to display notifications internally even if it’s not installed, thus making installing Growl the only way for me to access UI controls for actually _turning the notifications off_.<sup id="fnref:5"><a href="#fn:5" class="footnote-ref" role="doc-noteref">6</a></sup>

But I find I’m quite content with the fact that, on the Mac, Mail _doesn’t_ pop up a summary of the email I just received, and iChat _doesn’t_ constantly overlay last five messages from my friend on top of whatever else I was in the middle of. A single bounce of the dock icon and a number badge is enough to let me know that there’s something waiting for my attention. I can go and look at it when I’m good and ready. If I want to see new iChat messages as they come in, I can leave the window open on the side of the screen; or, if I want to focus on something else, I can hide that window. There’s no need for me to be constantly pulled away from what I’m doing for… well, just about anything.

The only apps I really find Growl useful for are the ones that lack any UI for telling me certain types of things: for which Growl is the _only_ way I would know about certain information, because the developer did not build any alternative. But that seems more like a failing of the app developer, not a benefit of Growl. I think Growl (and similar systems) were always intended to be a secondary source of information presentation for an app, never the primary.

On iOS, the situation is a little different: I can’t keep my instant messages in a window off to the side, because there are no windows on iOS. And I have no complaints about that. But it does mean I’m a little more tolerant of notifications; just only in very limited cases.

* * *

1. It’s somewhat amusing that of these two examples, Sherlock no longer really exists in any form resembling the original Watson–it sort of morphed into Spotlight, while losing most of its recognisable features–and Dashboard has long been on its way out. I somewhat suspect the only reason Dashboard still exists in current versions of the OS is because Apple printed a dedicated key for it on the keyboard for so long (newer keyboards omit this key in favour of one for Launchpad). The fact that there is no Dashboard Widgets category on the App Store seems enough to seal its doom.&nbsp;[↩︎](#fnref:1)

2. Perhaps significantly, Growl was given away free of charge for most of its life, and only recently made a $1.99 purchase at the App Store. It remains open-source, so anyone who wants to can avoid paying for it by downloading the source code and compiling it with Xcode.&nbsp;[↩︎](#fnref:2)

3. I should have a citation for this, but I don’t. So it might be rumours, or my faulty memory, or I might have just made it up. Take that for what you will.&nbsp;[↩︎](#fnref:3)

4. Admittedly not even comparable to how many hours have been collectively put into Growl over the years.&nbsp;[↩︎](#fnref:6)

5. The original reason for this was to save battery life on iOS devices, by only connecting to a single central notifications server rather than keeping many connections open at all times. It’s debatable whether or not that’s necessary on Macs, but it may well make more sense in terms of Apple’s development efforts to just reuse the existing service, rather than make something new just for Mac that works only slightly differently.&nbsp;[↩︎](#fnref:4)

6. In the past, it was also common for apps to [silently reinstall Growl](http://growl.info/thirdpartyinstallations.php) on the system if it wasn’t present. I think this isn’t as common now, but the problem I described is almost worse: careless developers continuing to use their internal bundled version of Growl, while not presenting any UI for disabling it.&nbsp;[↩︎](#fnref:5)

