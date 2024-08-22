---
layout: post
title: You fix it, you bought it
date: '2011-05-12T22:54:00-07:00'
tags:
- he said she said
- longer post
tumblr_url: https://blog.horizon-nigh.org/post/5440163204/you-fix-it-you-bought-it
---
[VUPEN said](http://www.vupen.com/demos/VUPEN_Pwning_Chrome.php) they found and successfully exploited a ‘zero-day’ (not previously known) vulnerability that defeated Chrome’s reputable 'sandbox’ security model.

[Google said](http://www.computerworld.com/s/article/9216627/Google_engineers_deny_Chrome_hack_exploited_browser_s_code) Chrome was not hacked and was not vulnerable; instead, it was a problem with the Adobe Flash plugin, which is included with every Chrome install.

[Gruber said](http://daringfireball.net/linked/2011/05/12/chrome-flash), along with [many others](http://search.twitter.com/search?q=%40scarybeasts), that because Google bundles Flash with Chrome, even though Google did not write the insecure software (Flash) and cannot fix the insecure software (Flash), they still are responsible for the problem because they included it with Chrome.<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>

Google engineer [Chris Evans said](https://twitter.com/scarybeasts/status/68771254781480960) the reason Google bundles Flash with Chrome is because most users already have Flash installed, but the version they have installed is, more often than not, an old and outdated version of Flash, presumably containing more security problems than the latest version. Therefore, even if the latest version has problems (or is likely to have problems in the future), bundling it is still likely to improve the situation for most people.

Let’s assume for the sake of argument that Evans’s explanation is Google’s motivation for bundling Flash<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>.

People like me who have some semblance of knowledge about 'computer stuff’ are familiar with the problem of helping relatives with their computer issues:

_If you help them fix it, they’ll call you the next time it breaks again. And again. And again._

You can try to explain the reasons they got themselves into that mess: they clicked dodgy attachments, they installed smiley packs, or they simply continued to use a machine with Windows on it. But it won’t make any difference; by continuing to help them, you continue to enable their bad habits that continue to lead to problems, and they come to depend on you.

Google says that bundling Flash is better than doing nothing, but there is one other thing they could do:

Block Flash in Chrome by default.<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup> Move YouTube to HTML5. The world would follow.

(No, I don’t really expect this to happen anytime soon.)

**Update 2011-05-25:** I recently found out, completely by accident, that Chrome actually has a built-in option to do what I suggested; it’s just off by default. Here’s how to turn it on:

1. Navigate to about:flags
2. Find 'Click to play’ on the page, and click 'Enable’. Oddly, this does not actually enable the feature, it only enables another option which you can use to enable the feature.
3. Restart Chrome.
4. Open Preferences.<sup id="fnref:chrome-prefs"><a href="#fn:chrome-prefs" class="footnote-ref" role="doc-noteref">4</a></sup>
5. Click 'Under the Hood’.<sup id="fnref:bonnet"><a href="#fn:bonnet" class="footnote-ref" role="doc-noteref">5</a></sup>
6. Click 'Content Settings’.
7. Finally, next to Plug-Ins, select 'Click to play’.

* * *

1. This reflects Gruber’s reasoning for why Apple has never included Flash on the iPhone or iPad, and no longer includes it on new Macs: it is beyond Apple’s power to fix when things go wrong; and Flash has a history of things going wrong, especially on their platform.&nbsp;[↩︎](#fnref:1)

2. And not, say, because it gives them a claimed competitive advantage in certain markets against a certain competitor who refuses to have anything to do with Flash as of late.&nbsp;[↩︎](#fnref:2)

3. It doesn’t even have to be as extreme as Apple’s prohibition. Simply putting the Flash content behind an overlay that says 'click to display insecure content’ should do the trick. Most sites’ video content is already in h.264; they just need a little nudge. It’s sad how much the web depends on a plugin it doesn’t even need any more.&nbsp;[↩︎](#fnref:3)

4. Ttry explaining this part to a novice computer user over the phone. On the Mac, Preferences can be found in the usual place. On Windows, you have to explain what the 'wrench’ icon is and where to find it. But then, nothing works the same way as anything else on Windows.&nbsp;[↩︎](#fnref:chrome-prefs)

5. Or if you’re using a Commonwealth English version, 'Under the Bonnet’. Charming localisation.&nbsp;[↩︎](#fnref:bonnet)

