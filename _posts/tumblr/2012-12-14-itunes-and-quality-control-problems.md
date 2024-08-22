---
layout: post
title: iTunes and quality control problems
date: '2012-12-14T11:37:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/37913350748/itunes-and-quality-control-problems
---
As loath as I am to link to [Business Insider](http://www.marco.org/2011/09/23/business-insider), Henry Blodget shares [this interesting anecdote](http://www.businessinsider.com/why-amazon-is-one-of-the-most-successful-companies-in-the-world-2012-12), as an email he received from Amazon:

> Hello,
> 
> We noticed that you experienced poor video playback while watching the following rental(s) on Amazon Video On Demand:
> 
> Casablanca
> 
> We’re sorry for the inconvenience and have issued you a refund for the following amount(s):
> 
> $2.99
> 
> …We hope to see you again soon.
> 
> Amazon Video On Demand Team

The customer had a minor problem with his purchase, Amazon noticed, Amazon made it right - all without the customer ever saying a word. That’s impressive.

* * *

This made me think about my experiences with the iTunes Store.

### 1. Doctor Who, Season 1 (2005)

I purchased this a year or two ago, after noticing that the Netflix version of it had been inexplicably converted to 4:3 pan-scan (despite it originally having aired on the BBC in 16:9).

The iTunes version was in the correct aspect ratio, but the video quality was absolutely abysmal. Based on the amount of visible compression artefacts and pixellation, it looked like it had been [nearest-neighbour](https://en.wikipedia.org/wiki/Image_scaling#Scaling_methods) resized and converted from some kind of awful 1990s codec<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>. I can only imagine that this is the result of someone at BBC America thinking something along the lines of ‘all web video is the same’.

I requested a refund through iTunes Support, and received it, along with a form letter reminding me that this was an exception to the rules and they didn’t have to do this for me because 'all sales are final’. How incredibly generous of them.

The purchase has since disappeared from my iCloud library. I would like to own this season, if they ever fix the quality issues, but I have no way of knowing if or when that will ever happen, or if it has already happened.

### 2. The Dark Knight

I purchased this a few weeks ago in anticipation of the new one coming out soon. Overall it was fine, but during the 'bat sonar’ scenes, the aspect ratio kept switching back and forth to 16:9, even though the rest of the film was presented in 2.40:1.<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>

I didn’t consider this enough of a problem to contact support, but it seems like a clumsy oversight, and it makes me wonder how this could even happen.

### 3. The Lord of the Rings - Extended Edition Bundle

I haven’t actually purchased this one yet, but I was thinking about it - until I saw the [reviews](https://itunes.apple.com/us/movie-collection/lord-rings-extended-edition/id443949050).

Apparently, Fellowship is missing the subtitles in the spoken Elvish scenes, making it impossible to know what the characters are saying, unless you’re a much bigger Tolkien nerd than I am.

As for Two Towers and RotK, reviews report that the soundtrack is in mono - even in the 'HD’ versions.<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup> And this is supposed to be a premium offering? It’s priced to suggest as much.

Again, I have no way to know if or when these problems are ever corrected, and whether it is 'safe’ to buy these now. Many reviews that still show up on the top of the page complain that there is no HD version, when in fact this has since been rectified. But I can easily confirm the existence of an HD version by looking at the store page; the same can’t be said for video and audio problems.

**Edit 12/22:** [Here is a long forum thread about these problems.](https://discussions.apple.com/thread/3804474?start=0&tstart=0) It appears the mono problems may have been resolved, at least for some people, but if you read through it all, you can see what an awful mess it was to get through to someone who could do something about it. The subtitles problem is mentioned on page #6. Going by that, as well as reviews that are still coming in from the past few days, it looks like the subtitles problem still exists and nobody is doing anything about it.

* * *

As soon as Apple announced both TV shows and movie purchases would be available for streaming in iCloud, I decided that all of my future purchases would be through them instead of in the form of physical objects. I am totally on board with this cloud-based future: the instant gratification of watching purchases immediately, the ability to access my entire collection from anywhere, nothing to take up space on my shelves or hard drives, etc. I am so enthusiastic about this that I am willing to overlook the serious flaws, like DRM (which only hurts paying customers, not pirates) and the possibility that if Apple ever discontinues the service, I could 'lose’ everything<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">4</a></sup>.

I have not made very many purchases to date: only a small handful, which makes these problems seem like an overall, systematic quality-control issue. It’s possible I’m just unlucky, but these are some fairly well-known titles.

Who’s to blame for this?

As an iOS developer, I’m somewhat familiar with iTunes Connect, the web site that developers use to submit apps to the App Store. It has 'iTunes’ in the name because it was originally created for record labels to upload music to the iTunes Store, which predates either apps or movies being available for sale.

I think it’s fair to assume that movie distribution works the same way: the publisher applies for an iTunes Connect account, Apple creates the account, then the publisher does the rest. The publisher uses the web site to create movies in the database, fills in the textual and promotional information, encodes the video files according to Apple’s guidelines, then uploads them. It wouldn’t surprise me if Apple doesn’t even review these videos before making them available for sale, like they do for apps; there are only a small handful of very big companies that publish movies, and they necessarily have close business relationships with Apple (due to the negotiations that must take place), unlike app developers.

For whatever reason, it seems like the publishers, who are encoding the videos and doing such a poor job of it, are just not putting as much effort behind their iTunes versions of the movies as the DVDs and Blu-rays. I’m guessing at the executive level, they still see iTunes as just some annoying short-lived fad, and if people really want movies they know they should be buying Blu-rays, and people will continue to buy Blu-rays forever because that’s what Hollywood told them to do; and that they therefore don’t allocate as many talented engineers and quality-control people to the department responsible for encoding the iTunes versions, versus the Blu-ray and DVD versions.

* * *

It’s unrealistic to expect meaningful change or awareness from Hollywood. They’re too big and stupid. Apple has to solve this problem.

It’s really quite simple: when a bunch of people report the same problem to support, have someone from Apple look at the video and observe the problem. If Apple can confirm it, pull the video from sale, and tell the publisher it doesn’t get to go back on sale until it’s fixed. That should light a fire under them. Sound familiar? It’s pretty much what already happens on the App Store.

Then, to go a step further, when the publisher fixes the problem and Apple confirms it, and it goes back on sale: email everyone who purchased it (whether or not they have already been refunded) to apologise and let them know the problem has been fixed. And if there are any public reviews mentioning the problem, add a response that indicates it has been resolved. (For the love of all that is decent, don’t just simply delete the reviews! That makes it look like you’re trying to _hide_ the problem rather than _solve_ it.)

Notice that my plan doesn’t even involve refunding the affected people. I don’t think that’s strictly necessary, although it would make customers happier and I certainly think Apple could afford to do it. But personally, I’m less concerned about getting my money back (or a 'free’ movie) as I am about actually watching and enjoying the thing I wanted to watch.

Anyway, nothing will change until someone high up at Apple understands that this is a problem, and I’m not sure they do.

* * *

1. I’m not the kind of person who usually notices these things. I happily watch DVDs on my HDTV. I don’t own a single Blu-ray. If it was bad enough for me to notice, then it was quite bad.&nbsp;[↩︎](#fnref:1)

2. 16:9 is the aspect ratio of 'widescreen’ HDTVs, which is not the same shape as the screen in a cinema - those are 2.40:1, which is even wider. That’s why many 'widescreen’ movies you watch on your HDTV still have black bars at the top and bottom, even though both the movie and the TV are supposed to be 'widescreen’ - they’re different types of 'widescreen’. Other movies are either made in 16:9 to fit your TV at the expense of looking good in the cinema, or are made in 2.40:1 and then the edges are clipped off to fit your TV - just like the bad old days before HDTVs. TV shows are almost always made in 16:9 these days. The TV industry had a chance to fix this aspect ratio nonsense once and for all when HDTVs started becoming popular a few years ago, but they chose not to, and why that is remains a mystery to me. But then, so are a lot of things the TV industry does, like keeping around interlacing and overscan.&nbsp;[↩︎](#fnref:2)

3. For a while, I was puzzled as to how the people leaving reviews could be so certain that this was the case, as opposed to some other kind of audio problem - do they all have exceptional hearing ability? Then I remembered that some high-end sound systems actually have LED lights indicating what type of audio signal they’re receiving (e.g.: DTS, 5.1, stereo, or indeed, mono). Or, I suppose, you could download the film to your Mac, open it in QuickTime and do a Get Info.&nbsp;[↩︎](#fnref:3)

4. Scare quotes because nothing is ever really 'lost’ on the internet. The movies will still exist somewhere. I am throwing Hollywood a bone here and making a conscious effort to play by their rules. In return, I expect them to not screw me over. If they do, I’m sure I’ll find some way to make my media collection whole again; but I would prefer it if it didn’t come to that. This is the tenuous arrangement I am making with them: they have this one chance to make this work right and have me as a paying customer, and it’s up to them now, as to whether they’re going to keep a good thing going, or ruin it somehow.&nbsp;[↩︎](#fnref:4)

