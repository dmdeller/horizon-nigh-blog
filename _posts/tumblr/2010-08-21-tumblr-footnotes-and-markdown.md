---
layout: post
title: Tumblr, Footnotes and Markdown
date: '2010-08-21T11:34:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/987877254/tumblr-footnotes-and-markdown
---
[Tumblr, Footnotes and Markdown](http://blog.devin.reams.me/post/654804433/add-foonote-to-tumblr-blog)  

**Update:** Hi, users of a popular search engine! You might be looking for how to use footnotes in Markdown. Here’s the TL;DR on that:

- Footnotes are just like links, except they have a caret (^) before the identifier. Like this:

- Footnotes don’t work in John Gruber’s [original version of Markdown](http://daringfireball.net/projects/markdown/syntax), but they do work in some variants like the one Tumblr uses.

That’s really it!

The original point of this entry was _not_ to answer the above question–it was a long, rambling diatribe on my feelings about Markdown in general–but apparently a popular search engine has decided to show this page when people search for it! I suppose, in the end, we all exist only to serve the algorithm. Have a nice day!

–

**Original entry:**

When I was writing [this post](/2010/08/17/james-goslings-interesting-aside.html), I wanted to insert a footnote about the ‘first-class citizen’ reference. I’ve struggled with this before with [Tumblr](http://www.tumblr.com): there’s no easily apparent way to do this through the [WYSIWYG](http://en.wikipedia.org/wiki/WYSIWYG) editor, and writing the HTML by hand would be so laborious. Eventually, I gave up and posted it without the information I would have put in the footnote, because it was too much trouble.

But I was reading [this blog post](http://www.marco.org/985141775) by Marco Arment, one of the creators of Tumblr, and noticed he had very nice footnotes. A glance at his HTML source code shows they are fairly obviously automatically-generated. So how does he do it?

My first inclination was to ask him directly, because I was sure that Googling for the issue would turn up obscenely hackish methods (later [confirmed](http://jasonwyatt.tumblr.com/post/212507536/footnotes-js-automatic-footnote-creator)). But he’s a popular guy, and who knows if I’ll ever get a reply, and he’s going on vacation, etc. So I eventually<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup> relented and did my Google search, and found the page linked in the header<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>, which indicates that this is only possible if you use [Markdown](http://daringfireball.net/projects/markdown/).

I didn’t even know Tumblr had an option to use Markdown; yet, I’ve always had a strong distaste for Markdown, BBCode, Wiki formatting, and all of their various siblings. They are **programmer languages** <sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup>; written by programmers, for programmers, occasionally under the extremely naive assumption that they can make it 'so easy to use’ that non-programmers could use them.

Just [read this account by Jeff Atwood](http://www.codinghorror.com/blog/2009/10/treating-user-myopia.html), one of the creators of [StackOverflow](http://www.stackoverflow.com). This site has a highly technical audience which is still getting confused by Markdown. I disagree with Atwood’s conclusion, though: he treats this as a **user-interface design** problem, but I think it’s a **user interaction design** problem. In that: _Markdown and similar languages are too much trouble for most people to use, and if you try to force it on them, you will fail._

Please, web developers, read [this quote](http://daringfireball.net/linked/2009/10/23/github-flavored-markdown) from John Gruber (creator of Markdown) over and over again until it finally sinks in (emphasis mine):

> Markdown’s popularity — still growing — is incredibly gratifying. But **I never intended for it to be used by people who don’t actually know the Markdown formatting rules**. I created Markdown for my own use, and, well, I know the formatting rules pretty well.

He goes on to suggest that GitHub’s variant might be improved for this audience–people who don’t know the rules–but the point is that it was never an original design goal, and GitHub and others are trying to fit it into someplace it wasn’t designed to be.

Like any type of design, user interaction design should happen from the ground up.

But, although those feelings of distaste may have contributed to my avoidance of Markdown, it’s not the root cause; I am a programmer, and I can use a programming language. But I also like to write, sometimes, and when I write, the last thing I want to be doing is programming.<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">4</a></sup>

Writing is hard; whether it’s writing an essay or asking a question on a forum, if you want to write well, it takes a considerable amount of effort. Trying to force someone to think about conforming to a logical syntax at the same time as everything else that’s involved in writing is like throwing mental roadblocks in their way. It’s just cruel.<sup id="fnref:5"><a href="#fn:5" class="footnote-ref" role="doc-noteref">5</a></sup>

Tumblr is very well-designed, and I suspect it is for one or more of these reasons that the default is WYSIWYG. But some people do like Markdown, so it’s nice that it’s an option.

In any case, I have tended towards WYSIWYG widgets, even though I know HTML and dozens of other markup languages: I want to write without the hassle of coding.

But I _have_ felt for a while now that I am still spending an inordinate amount of time appeasing the system when I’m trying to write. I have to click to make a link. Click to make a quote. And when I copy and paste a quote, I have to first paste it into TextEdit to remove the font size and colour<sup id="fnref:6"><a href="#fn:6" class="footnote-ref" role="doc-noteref">6</a></sup>, so that it won’t look weird on my site. In a post like this, where I might have nearly a dozen links, it feels like a lot of distractions.

Indeed, sometimes when I have an idea I want to jot down quickly without going through that trouble, I end up putting it in a plain text file and marking up links with [square bracket numbers], with the intention of going back and inserting them later. It ends up being halfway to Markdown anyway.

So I am giving Markdown a chance. I went back and added that crucial footnote to the earlier post. And so far, I have written this post in entirely in Markdown<sup id="fnref:7"><a href="#fn:7" class="footnote-ref" role="doc-noteref">7</a></sup>, and it’s surprisingly bearable. I think I will continue to do so and see how it goes.

Still, I wouldn’t recommend it to any of my non-programmer friends. And, going back to the original point of this post, there really should be some way to make footnotes using the WYSIWYG editor.

* * *

1. This may be obvious, but in case it isn’t: if you’re ever writing to an even somewhat famous person, try to keep your question to no more than 1-2 sentences if at all possible. It drastically increases the likelihood that you’ll get a response.

2. This post I’m writing here is a 'link’ post, which, to me, means its content is principally related to a link to somewhere else on the web. On Tumblr, this means it gets linked as the header text of the post. Yet, often times, the post is a journey of discovery, wherein I don’t end up mentioning this primary link until halfway down the post. At that point, it’s clumsy for me to refer back to the link all the way at the top, and I haven’t figured out a good way of doing it. I could link it again, but that would be redundant. I could just make the post a 'text’ post instead of a 'link’ post, but that would be favouring presentation over semantics.&nbsp;[↩︎](#fnref:2)

3. Not to be confused with **programming languages** , which Markdown is not. Let’s not even go there.&nbsp;[↩︎](#fnref:3)

4. Even if I’m writing _about_ programming.&nbsp;[↩︎](#fnref:4)

5. And if you’re providing a service that you’re making a profit from, it’s a bad way to treat your customers. Spend some extra time and effort on programming and make it easier for them.&nbsp;[↩︎](#fnref:5)

6. Incredibly stupid default. Probably not Tumblr’s fault.&nbsp;[↩︎](#fnref:6)

7. As you can probably tell from the footnotes.&nbsp;[↩︎](#fnref:7)

