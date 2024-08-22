---
layout: post
title: Convenience vs. security in China
date: '2014-10-22T10:21:41-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/100667800267/convenience-vs-security-in-china
---
[Convenience vs. security in China](http://www.nytimes.com/2014/10/22/technology/china-attack-aims-at-apple-icloud-storage-service.html?_r=0)  

This story rather fascinating to me, to see how different the basic realities of using the internet are when in China.

## A bit of background about SSL failure UIs

Invalid SSL certificates, generally speaking, are not a new problem. I would guess that most internet users, no matter where they are in the world, will come across this problem at least a few times a year. Most of the time, this is due to a temporary misconfiguration on the web server, or possibly someone in charge of the web site forgetting to renew the certificate before its expiration date<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>. In either case, if the web site has any non-trivial number of visitors, the web site owner usually quickly learns about the problem and corrects it. There is nothing the user needs to do or really should do, other than stop trying to use the web site and try again at a later time.

As I’ve said, usually, the problem is because of an innocent mistake on the part of the web site owner; however, there is always the possibility that it is the result of an attack. The browser cannot distinguish between these two cases.

And so it was, that in the early days of web browsers, when the internet was smaller and users were assumed to be more likely to have some technical knowledge, a browser encountering an SSL problem when trying to access a web site would simply present a dialog asking the user whether they wanted to stop or continue. After all, the browser didn’t know what the reason for the problem was, so it left it up to the user to figure it out.

The problem was that users didn’t know what the reason for the problem was _either_, and in most cases had no understanding of the problem at all. And therefore, the browser was presenting a nonsense choice to them. It may as well have said:

> Uh, we came across some kind of problem, here’s a bunch of gibberish, I dunno, did you want to visit that web site you asked for or should we just give up?
> 
> [More Info] [Cancel] [Continue]

Obviously, the user still wants to visit the web site they asked for, and doesn’t know what any of the rest of that means. So they’re going to click ‘Continue’. Every time. This is not a good thing, because, as above, it _may_ be the result of an innocent mistake, but it _may_ instead be an attack.

Some of the web browser makers eventually figured out their users’ habits in relation to this, and so they changed their UIs. You can see examples in [this Apple support document about the problem](http://support.apple.com/kb/HT6550), which shows screen shots of Firefox and Chrome, as well as Safari.

Presently, when encountering this situation, Firefox and Chrome will show a blocking error page (similar to what happens if your network is down), attempting to explain in simple terms that something is very wrong and there’s not much else that can be done about it. There is still a way to continue despite the error, but it is harder to find in the UI. This is a good thing, because continuing in the face of an SSL failure is something that really only system administrators with specific knowledge of exactly what caused the problem should be doing.

Unfortunately, Safari never implemented similar improvements, and still shows the simpler message that unwittingly encourages the user to make the wrong choice. I hope this changes. But I’m optimistic. I would think the fact that Apple needed to create a support document to explain not to click a button in their UI should be enough for them to realise that the UI should probably be changed.

## And now, China

I said earlier that an SSL failure is usually the result of an innocent mistake. This has been true in my experience (as far as I know), but my experience is limited to that of a person living in the US<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>. China, on the other hand…

From the various reports I’ve been reading about this, it sounds like SSL failures are extremely common when visiting any web site in China, either foreign or domestic. No-one seems to know for certain, but the general assumption is that the [Great Firewall](https://en.wikipedia.org/wiki/Golden_Shield_Project) is involved; this is the very definition of a [man-in-the-middle attack](https://en.wikipedia.org/wiki/Man-in-the-middle_attack), in no uncertain terms. But according to some<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup>, this has also led to a more widespread lack of concern about security, to the extent that many domestic web sites don’t even bother properly configuring SSL, because their users are so used to continuing after seeing the errors, so they see little point in doing so.

But here’s a UX problem. Firefox and Chrome have, in recent years, become so assertive about discouraging users from continuing after an SSL failure, that as a practical matter, these browsers must be almost impossible for everyday use, for an ordinary user in China. What is the user supposed to do? They don’t know if the problem is being caused by the government or the web site owner, and even if they did know, there’s nothing they can do about it and it’s unlikely to change. So what do you do? Just not use the internet? How frustrating that must be.

It turns out, there is a company called [Qihoo](https://en.wikipedia.org/wiki/Qihoo) in China who provide a number of free (ad-supported) products, including anti-virus, and an apparently very popular web browser. Based on what I’ve read, it seems like this browser, as a general rule, may do _absolutely nothing at all_ in terms of warnings or errors when it encounters an SSL failure; in other words, it simply continues to the web site as if nothing happened.

Whether Qihoo’s behaviour is a result of government mandates or simply an attempt to provide a better UX, you can see why it might be an appealing option for users. After all, if you’re generally aware that the government is probably intercepting everything, and there’s nothing you can really do about it, and you want to use the internet anyway… I’m not saying it’s what I would do, but you can see why many people would make the choice to use that product.

As far as I can tell, it doesn’t seem like Qihoo have a Mac version. But that probably doesn’t matter much–most of the people visiting icloud.com worldwide are likely using Windows, as there isn’t much of a need to visit it in a web browser if you do have a Mac. Therefore, Safari’s UI problem (explained above) probably isn’t going to make much of a difference either way to the situation in China. And even if Apple do make the Safari UI for SSL failures more like Firefox or Chrome, that may only serve to push people away from using Safari, and ultimately, away from using Apple products.

What is the solution? I’m not sure. An SSL failure is kind of an ultimatum. You’re served a compromised connection, and you can either take it or leave it. Neither option is good. More advanced users may know how to use an overseas VPN or something, but that’s likely out of reach for most people.

* * *

1. A third reason this can happen is that internal corporate networks, due to arcane policies I won’t even attempt to explain, can sometimes have very complicated and unusual SSL setups that must be configured manually in the user’s web browser or OS. This is mostly not relevant here, because it does not generally apply to web sites on the public internet.&nbsp;[↩︎](#fnref:1)

2. As we all know by now, in the US, we have the NSA snooping on everything they can. But, for better or for worse, the situation remains different here. The NSA are more sneaky about what they do. They are unlikely to attempt something as clumsy as an SSL MITM attack on a large scale, because this would be quickly noticed by security researchers and reported in the mass media. The same can’t be necessarily be said of China. There’s no doubt in my mind that the NSA do similar things, but they are more careful to try to remain undetected.&nbsp;[↩︎](#fnref:2)

3. Yes, I am using a lot of [weasel words](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style/Words_to_watch#Unsupported_attributions), and I am doing this quite deliberately, to let you know that my information about what exactly is going on in China is not at all reliable or verified and could very well be entirely wrong. Perhaps it would be best for me to avoid writing about it entirely, but that is hard to do when it is so interesting to me. I strive to be accurate, but I also strive to let you know of cases when I’m not sure of my own accuracy.&nbsp;[↩︎](#fnref:3)

