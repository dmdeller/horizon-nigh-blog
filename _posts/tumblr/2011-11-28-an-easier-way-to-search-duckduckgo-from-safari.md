---
layout: post
title: An easier way to search DuckDuckGo from Safari
date: '2011-11-28T14:37:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/13462195045/an-easier-way-to-search-duckduckgo-from-safari
---
I [previously](/2011/11/06/script-to-search-duckduckgo-from-the-safari-search-bar.html) wrote about a workaround I made to replace the Yahoo search in Safari with DuckDuckGo, my new favourite search engine. ([Other browsers](http://help.duckduckgo.com/customer/portal/articles/216425-browsers) don’t need workarounds.)

An unfortunate complexity of the method I wrote about was that you needed to run your own web server. But I emailed [Yegg](http://ye.gg), the founder of DuckDuckGo, explaining what I did, and he was interested in helping on their end to make this easier.

So, good news: you no longer need to run your own web server for this to work! DuckDuckGo now takes care of that part (which makes sense, since I gather they have a few web servers that they were _already running_).<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>

You now just need to add this one line to your /etc/hosts file, restart Safari, and ‘Yahoo’ will be DuckDuckGo from now on:

    184.72.115.86 search.yahoo.com

To make this even easier for people who don’t know how to edit their hosts file, I’ve put together a simple Mac app which does this for you. [Download it here.](https://github.com/dmdeller/ddg-safari/downloads) Patches welcome via GitHub.

You can also read [the support doc on DuckDuckGo](http://help.duckduckgo.com/customer/portal/articles/255650-hosts-file), which explains in more detail. Of course, there are still [other ways](http://help.duckduckgo.com/customer/portal/articles/216447-safari) to accomplish this, but I think mine is the best way.

It’s really cool to use a search engine that’s so responsive to user requests, and even willing to collaborate with me. I’m making an effort to do most of my searches with DuckDuckGo now, and only falling back to Google when I can’t find something. (Will you take the [DuckDuckGo Challenge](http://www.reddit.com/r/duckduckgo/comments/lweg1/dear_redditors_take_the_duckduckgo_challenge_if)?) I hope to see DuckDuckGo give Google some much needed competition.

* * *

1. For the curious, [here’s how we did it](https://gist.github.com/1401727). (You don’t need to know/understand this to use it.)&nbsp;[↩︎](#fnref:1)

