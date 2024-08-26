---
layout: post
title: Apple statement about iMessage security
date: '2013-10-18T17:51:49-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/64420084920/apple-statement-about-imessage-security
---
[Apple statement about iMessage security](http://allthingsd.com/20131018/apple-no-we-cant-read-your-imessages/)  

Apple’s Trudy Muller:

> iMessage is not architected to allow Apple to read messages… . The research discussed theoretical vulnerabilities that would require Apple to re-engineer the iMessage system to exploit it, and Apple has no plans or intentions to do so.

It’s fascinating to me that Apple chose to respond to this.

Of course, both Apple and the researchers are correct. The researchers are (from what I can tell) correct in saying that Apple has the cryptographic capability to read messages if they so choose. Apple are (presumably) also correct in saying that their systems do not currently implement this functionality.

The AllThingsD article portrays this as a he-said-she-said ‘someone is lying’ kind of tale, but that’s facile and betrays a lack of interest of the underlying issue. The two parties do not directly contradict each other.

Clearly, Apple struck a balance when designing iMessage. The researchers correctly assert that the only way to verify to a certainty that the encryption is working properly is for the users to verify the public keys being used out-of-band<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>. The average user stopped listening at the phrase 'public key’, if not 'encryption’. It’s totally impractical for a company like Apple and a product like iMessage that is supposed to 'just work’. Security is almost always at odds with usability. It doesn’t matter if someone designs a completely secure system that no-one can understand or is willing to bother using. Likewise, an easy-to-use product that’s full of holes won’t last very long.

So is iMessage secure? Only as much as you are willing to take Apple’s word for it. It is not secure in a way that you can verify yourself.<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup> I’m not trying to imply that that’s good or bad–it’s good enough for some people, and not for others. If this upsets you, take a step back and realise that not everyone has your exact needs.

To me, the more interesting ramifications of this design are in what Apple could be forced to do by the government. There is plenty of [precedent](https://en.wikipedia.org/wiki/Lavabit) for the government forcing a company to let them snoop on some or all of their traffic. However, from what both the researchers and Apple say, it sounds like snooping would not be effective in this case. It’s not enough to simply _look_ at iMessage traffic; one would need to actively _tamper_ with it, and although it would be possible with the right server software, that server software would have to live inside Apple and does not currently exist (according to Apple).

So what I’m getting to is that despite the clear precedent in favour of granting **access to data** , there is much less precedent (at least to my knowledge) in forcing a company like Apple, against their will, to **create new software** solely for the purpose of assisting the government. It would almost certainly be _possible_ for Apple to do so in response to a government request, but Apple could legitimately claim that it would represent a considerable, perhaps unreasonable burden with direct monetary costs. What would the price tag be? What is the government’s budget for this sort of thing? Can the government control and direct a person or company’s creative efforts, or merely their existing digital assets?

I don’t know if this argument would hold up in a secret court, especially against judges who have a poor understanding of technology and are predisposed to accept any argument made by their own government. But, to my knowledge, it is a unique and novel approach that hasn’t been attempted before, at least not at this scale.

Again, it’s fascinating to me that Apple chose to design it this way, when they could have much more easily gone with the same trivial SSL implementation that most other companies use<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">3</a></sup>, which holds up against most third-party attackers, but not government intervention. And they didn’t do it for marketing reasons: nowhere have Apple advertised or even mentioned the security of iMessage, except in direct response to public criticism. We’ll never really know why, of course.

_Previously: [[1]](/2013/10/17/more-on-imessage-encryption.html), [[2]](/2013/06/26/can-apple-read-your-imessages.html), [[3]](/2013/06/19/imessage-and-facetime-are-end-to-end-encrypted.html)_

* * *

1. Crypto-speak meaning that you have to verify the other person’s identity (i.e., public key) using some method of communication _other_ than the one that will _use_ the public key (i.e., iMessage), because otherwise you don’t know for sure who that public key belongs to. The classic dilemma: How do you transmit the public key in a secure way? And if you _did_ have an existing secure way of transmitting arbitrary information, wouldn’t you use that instead of this complicated public key stuff? The typical suggestion is to exchange public keys in a face-to-face meeting involving no electronics–highly secure, but not nearly as convenient to do frequently compared to using the internet. This may be a reasonable step to take if someone really is out to get you, but is much too high a burden for people who don’t know or care about any of this stuff.&nbsp;[↩︎](#fnref:1)

2. Any kind of security is only good to the extent that you can either verify that it works yourself, or that you can trust others to tell you that it works. To someone who really does have people out to get them, it’s probably not a good idea to take Apple’s word for it. But even for those people, using strong, widely peer-reviewed, open-source secure communications software, they will still be forced to use components that they themselves do not have first-hand knowledge of their workings. Even if you read every line of source code of the encryption software and compiled it yourself: there’s still the compiler, and the operating system. Even if you read every line of source code (and assembly) for those two components, there’s still the hardware. Even if you use 'open-source’ hardware designs, you still didn’t etch the circuits onto silicon yourself, nor did you build the factory robots that did the etching. And so on.

3. You can be confident because it’s 'the same technology used by your bank!'&nbsp;[↩︎](#fnref:3)

