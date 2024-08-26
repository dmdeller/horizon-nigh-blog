---
layout: post
title: Script to search DuckDuckGo from the Safari search bar
date: '2011-11-06T12:22:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/12424404395/script-to-search-duckduckgo-from-the-safari-search-bar
---
_ **Update:** There’s now an [easier way to do this](/2011/11/28/an-easier-way-to-search-duckduckgo-from-safari.html)._

[DuckDuckGo](http://duckduckgo.com) is a promising new search engine, especially if the way Google is [bubbling](http://dontbubble.us) and [tracking](http://donttrack.us) you is starting to drive you crazy like it is to me.

Only one problem, if you’re a Safari user: Apple doesn’t provide a way to change the engines used in the search bar, beyond the three provided by default (Google, Yahoo!, and Bing). Boo, Apple.

There are several ways around this, as suggested by DuckDuckGo themselves:

- One of several Safari extensions that provide search functionality. These tend to be ugly and don’t actually integrate with the search bar you’re used to using, because Apple’s extension API doesn’t allow it. DuckDuckGo suggests [this one](http://vaporstun.com/files/duckduckgo-safari-extension/DuckDuckGoBar.safariextz), and [here’s a slightly better one](http://www.opensearchforsafari.com/).
- InputManager hacks (a.k.a. SIMBL) that can make Safari unstable, un-upgradeable, and are [generally a bad idea](http://daringfireball.net/linked/2008/03/19/mdj). I’m not even going to link to these.
- Configurable web proxies that sit between Safari and your internet connection, such as [GlimmerBlocker](http://glimmerblocker.org/) ([with a filter](http://glimmerblocker.org/wiki/Filters)). My main reluctance here is that it’s just something else to install at the system level, and it does more than I need it to.
- [Hacking the binary](http://hints.macworld.com/article.php?story=20030514035516436). You’d have to be pretty crazy and desperate to try this.

I don’t really like any of those options, so I thought of another way. It comes in two steps:

1. Edit /etc/hosts to forward search.yahoo.com to your local web server (assuming you run one)
2. Drop a simple Ruby script in your web root to intercept queries and redirect them to DuckDuckGo.

You can [view or download it here](https://gist.github.com/1343176).

<script src="https://gist.github.com/1343176.js"></script>

I chose Yahoo because that way I can still easily switch back and forth between Google, DuckDuckGo (labelled Yahoo in the UI), and Bing. Since Yahoo gave up on being a real search engine and only shows you Bing’s results anyway, I can’t imagine why I’d ever need to search Yahoo. Still, I made it so that I could still search from Yahoo’s homepage, if I ever wanted to. The script should be easy enough to modify if you’d rather intercept Google or Bing instead. Improvements via GitHub are welcome, of course.

This is still a hack, but to me personally, it strikes the best balance between least intrusion and greatest capability to do what I want. It’s probably not the best solution for everyone, but I’m putting it out there in case it helps someone else.

I might get around to packaging this as a friendlier installer for non-technical users, although I’m not really sure if that’s a good idea; with these sorts of hacks, it’s generally best if the person doing it understands how it works, so they can undo it if it stops working. That’s why I’ve deliberately left some basic concepts (e.g. how to enable the built-in web server, or edit your hosts file) as an exercise for the reader.

Now, if only I had a way to make this work on my iPad…

