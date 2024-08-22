---
layout: post
title: Google is forking WebKit
date: '2013-04-03T18:46:33-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/47056788380/google-is-forking-webkit
---
[Google is forking WebKit](http://www.chromium.org/blink/developer-faq)  

I honestly have no idea what Apple was thinking with the WebKit2 multi-process model. When a Chrome tab crashes, it’s isolated to that one tab. When a Safari tab crashes, it takes down _all of the other tabs with it_. This is better than the WebKit1 behaviour of taking down the entire browser UI, but still… kind of missing the point, isn’t it? What good is the browser UI if none of the tabs are working?

At first, I thought maybe this was just a limitation in the initial version of Safari that shipped right after WebKit2 was released, and that it would quickly improve to be more like Chrome. But no. Nearly three years later, Safari still has the same problem, and I still see it happen several times a week<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>.

Not only is this multi-process model worse than what Chrome had already been doing for years, but Apple wasn’t content to keep the code in Safari; they pushed it upstream into WebKit itself. What did they expect Google to do, switch to a worse model in Chrome in order to stay in line with WebKit?

Nah: Apple’s typical relationship to other companies is one of indifference. Most likely, Apple simply didn’t care what would happen as a result of increasing Google’s maintenance burden in this way. Well… this is what happens.

The entire internet is currently arguing over whether this is a good thing or a bad thing. LOL, internet. History will be the judge of that.

* * *

1. Usually this happens when I try to open an ‘Auto-Click’ bookmark, which I guess is Safari’s name for a tab group - it’s a bookmark folder that, when clicked, opens every bookmark simultaneously in separate tabs.&nbsp;[↩︎](#fnref:1)

