---
layout: post
title: How to use an iPhone with a prepaid plan (in the US)
date: '2012-09-30T22:26:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/32626272716/how-to-use-an-iphone-with-a-prepaid-plan-in-the-us
---
1. [AT&T GoPhone](#att)
2. [T-Mobile Monthly4G](#tmo)
3. [Virgin Mobile](#vmobl)
4. [StraightTalk and other MVNOs](#mvno)

## AT&T GoPhone

GoPhone is how AT&T brands their prepaid service.

### Why you’d want this

If you have somehow obtained an AT&T or unlocked iPhone which is off-contract, you may want to use it without signing a contract. As of current writing, AT&T has a surprisingly inexpensive prepaid plan for smartphones:

$25/month for 250 minutes and unlimited texts + $25/month for 1 GB data = $50/month total

That’s less than even their cheapest and most useless on-contract plan, and you can cancel or switch to someone else at any time. It’s not rocket science.

[More about this plan here](http://www.att.com/shop/wireless/plans/prepaidplans.html). Note that the $50 ‘unlimited data’ plan is NOT for smartphones like the iPhone. Typical AT&T - they’ll sell you 'unlimited’ only if your phone can’t do anything with it. As for voice plans, you can _only_ buy data if you have at least the $25 voice plan, so forget about trying to go cheaper there. You could buy a smaller amount of data, but the next step down is 200 MB for $15, which hardly seems like enough for anyone. There is apparently no tier higher than 1 GB, but if you use up the 1 GB, you should be able to pay $25 again for another 1 GB (I haven’t tested this).

### What to know beforehand

AT&T hates you.

Officially, this plan is not available for iPhones, because AT&T are jerks and they want you to sign a contract. If you ask anyone at AT&T about it directly, they are likely to tell you this, as it’s the party line and they could get in trouble for saying otherwise. You can, however, get it to work (see below).

You will not have Visual Voicemail. If you tap Voicemail in the Phone app, it will dial into the voice-prompting robot, and you’ll be able to use it just like your old dumbphone. It will also correctly indicate how many voicemails are waiting for you.

MMS also reportedly may not work. I haven’t tested this myself, because I don’t care about MMS.

All other features of the phone, including voice, text, internet and iMessage, should work.

If you have a 4S or a 5, you will have access to AT&T’s fastest 3G (which they sometimes refer to as '4G’). You will not have access to LTE because currently, GoPhone is completely excluded from LTE. This may change in the future. This was a business decision by AT&T; there is no technical reason for it.

### A bit of background

Technically, there’s no reason for GoPhone data not to work, even on a locked iPhone, except for one important detail: APN settings.

GSM, the technology that AT&T and T-Mobile (in the US) use, was designed to be brilliantly simple: get any SIM card from a carrier, put it in any GSM phone, and it just works. No setup. No configuration.

Except when data came along, they had to go and screw that up with APN settings. No longer is it enough to just put in a SIM card; that will still get you instant voice and text service, but for data, you need to manually type in a bunch of settings.

Obviously, this is not the Apple way. So Apple has made APN settings for all of their official carriers built-in to iOS. But here’s the thing about AT&T: they require _different_ APN settings for their postpaid customers, vs. their prepaid customers.<sup id="fnref:0"><a href="#fn:0" class="footnote-ref" role="doc-noteref">1</a></sup> And since prepaid AT&T isn’t officially supported, the iPhone will automatically use the postpaid APN settings, resulting in no data for you, even if you buy the prepaid data plan.

Well then. Easy fix, right? Just change the APN settings.

Nope. If your iPhone is locked, you have no way to manually edit the APN settings. (If your iPhone is unlocked, these settings magically appear. Unless you put an AT&T SIM card in there, in which case they disappear again, even on an unlocked phone. Why? Because AT&T hates you, that’s why.)

Luckily, there is a workaround, which is only intended for system administrators at large corporations, but anyone with the right knowledge can use it: configuration profiles. Basically, you just type the APN settings into a specially-formatted data file, and load it onto the iPhone; it will obey the settings in this file, even if it’s a locked phone and you can’t otherwise edit them. This is not hacking; it is a legitimate feature of iOS that Apple provides and has continued to provide, and it survives iOS updates etc.

The most well-known site for finding pre-made configuration profiles is unlockit.co.nz, which has profiles for almost every known carrier. If you visit that site on an iPhone, it offers you the ability to download and install them.

### How to do it

Caveat: if you’re trying to do this with an iPhone 5, it probably won’t work because (as of writing) AT&T does not have GoPhone nano-SIM cards. They do have GoPhone mini-SIMs (for 3GS and earlier) and micro-SIMs (for 4 and 4S).

**Update 2012-11-30:** Now that [Apple is selling unlocked iPhone 5](http://www.macrumors.com/2012/11/29/apple-now-selling-unlocked-gsm-iphones-in-the-u-s/), I can confirm that this does indeed still work. The AT&T staffer was happy to move my GoPhone service over to a nano-SIM for me (and even happier when I told him about unlockit.co.nz, which he did not know about). Contrary to what I previously said, I now believe there is no such thing as a 'prepaid’ or a 'postpaid’ SIM card at AT&T - it seems like any SIM card can be used for anything, the staffer just has to activate it the right way for you.

1. If you have any data on the iPhone, back it up now using iTunes or iCloud. Then erase the entire phone. (The specific steps for this are outside the scope of this how-to. Search Apple’s support site if you need help.)
2. Go to an AT&T store. I suggest an official one, not an authorised reseller - they’re more likely to have a clue.
3. Tell them you want the $25 GoPhone voice plan. If they give you trouble about activating it for an iPhone, just tell them that you understand that data won’t work, that you don’t care about data, and that you will only be using the iPhone on Wi-Fi.
4. Follow the AT&T agent’s directions in order to activate the iPhone while you are in the store. Make sure it works by placing a test call.
5. If you previously backed up your iPhone, you can restore it now.
6. From the comfort of your home, use a computer to log in to AT&T’s prepaid web site: [paygonline.com](https://www.paygonline.com). Unless the AT&T agent gave you a PIN, you will need to use 'forgot password’ the first time in order to log in.
7. Add the $25 data plan to your account. (If you are worried about whether it will work, you can add a smaller amount of data to test it first.)
8. Using your iPhone (connected to your home Wi-Fi), open Safari and go to: unlockit.co.nz
9. Choose 'Create APN’ on the web site, and select GoPhone for the carrier.
10. Follow the prompts to install the configuration profile.
11. Power your phone all the way off by holding the power button on the top, then slide the control. **Update:** No need to power off, just go into Settings \> General \> Mobile Data, and toggle it off and on again.

You should now have voice, text and data fully working.

## T-Mobile Monthly4G

First of all, when T-Mobile says '4G’, they mean what the rest of us know as 3G. Got it? It doesn’t have to make sense. Just go with it.

### Why you’d want this

T-Mobile loves you. (Given their financials, they’re also pretty desperate right now.) They will bend over backwards to have you and your iPhone as a customer–postpaid or prepaid. They have the most inexpensive plans of anyone, including [one for $30](http://prepaid-phones.t-mobile.com/monthly-4g-plans) with 100 minutes, unlimited texts, and 5 GB data<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>. Even though they don’t sell iPhones and aren’t an Apple-approved carrier, their staff are specially trained on how to activate iPhones on their network.

### A quick detour about unlocking

Your iPhone needs to be unlocked in order to work with T-Mobile.

In general, the iPhone is unlocked only if it was purchased from Apple at full price, or the carrier has granted an unlock. [AT&T will unlock an iPhone](http://www.att.com/deviceunlock) only after the 2-year contract has been completed, and \_only for the original owner of the phone\_<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">3</a></sup>. So if someone is giving you a phone, get them to unlock it first, if possible; if someone is selling you a phone, be very suspicious.

Serendipitously, all Verizon iPhone 5’s come unlocked out of the box–[more info about this here](http://www.macrumors.com/2012/09/24/verizon-leaving-iphone-5-sim-slots-unlocked-as-required-by-fcc-network-access-regulations/)–but see the important caveat about LTE below.

This section about unlocking could easily turn into an entire article, so I’m not going to say any more about it–search for more elsewhere if you need to.

### What to know beforehand

The reason not to go with T-Mobile is that their 3G network has historically been incompatible with the iPhone’s 3G, which means you’d be limited to the slower EDGE/2G speed (similar to dialup, if anyone still remembers what that is).

The good news is that T-Mobile is 'refarming’ its 3G network to be compatible with all iPhones by the end of 2012, so if they are to be believed, it will no longer be an issue after that. You can check the status of this effort on [this unofficial web site here](http://airportal.de).

However, as of writing, T-Mobile currently has no LTE network at all. Moreover, only the AT&T model iPhone 5 is compatible with T-Mobile’s planned LTE frequencies; the Verizon (or Sprint, if you can somehow unlock it) iPhone 5 will work on T-Mobile 3G, but not LTE. If LTE isn’t that important to you right now, read on.

Like with GoPhone, you will not have Visual Voicemail. MMS might work; I haven’t tested it.

### How to do it

If you have an iPhone 3GS or earlier, [order this SIM card](http://prepaid-phones.t-mobile.com/prepaid-phone/T-Mobile-Prepaid-SIM-Activation-Kit) and activate it on the web when it arrives.

If you have an iPhone 4 or 4S, you need a micro-SIM, which isn’t available online. **Update:** [These are now available online too!](http://prepaid-phones.t-mobile.com/prepaid-phone/T-Mobile-Micro-SIM-Card-Activation-Kit)

If you have an iPhone 5 (lucky you!), you need a _nano-SIM_ card, which isn’t currently available _anywhere_. **Update:** They do have these in official T-Mobile stores now, but the store I went to refused to give me a SIM unless I activated it on the spot, which I wasn’t interested in doing. This might not be a problem for you, unless you want the $30 web-only plan, in which case… good luck arguing with the retail staff about it, because I wasn’t able to find any nano-SIMs on the web site.<sup id="fnref:up1"><a href="#fn:up1" class="footnote-ref" role="doc-noteref">4</a></sup> You can also try mutilating a larger SIM to fit in the iPhone 5, but I wouldn’t recommend it because not only are the dimensions wrong, but a micro-SIM is too thick - you’d need to file it down with sandpaper - and if you don’t get it precisely right, you risk damaging your phone.

No need for me to waste more words explaining how to set it up, because [T-Mobile has a detailed guide right here](http://support.t-mobile.com/docs/DOC-4771). Like I said, they’d love to have you, unlike AT&T.

Aren’t you glad that merger didn’t work out? A competitive marketplace for all! (As if.)

## Virgin Mobile

I have only this to say about Virgin Mobile: you pay the full, unlocked price<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">5</a></sup> for a locked phone, and they will never ever unlock it for you, for any reason.

Their service prices are about the same as T-Mobile. If you’re considering Virgin Mobile, just buy an unlocked phone directly from Apple and activate it with T-Mobile.

Virgin Mobile’s network is certainly no advantage: they don’t have one. They use the spotty Sprint network, but at least postpaid Sprint customers can roam onto Verizon’s network at no extra charge when the signal drops; Virgin Mobile customers are not allowed to roam at all, so when it drops, it just drops.

I used a Virgin Mobile MiFi (3G data device) for about two years, and the network was pretty terrible most of the time (Boston area). And they kept screwing around with the prices and terms the entire time.

If for some reason you’re still convinced that Virgin Mobile is the way to go, you don’t need any 'how to’ information from me–just go ahead and buy the phone from them, since they won’t accept any phone onto their network except one they sold you directly.

## StraightTalk and other MVNOs

StraightTalk (a Mobile Virtual Network Operator, or MVNO) has become somewhat popular with prepaid iPhone customers because of their $45 unlimited plan (where 'unlimited’ means 2 GB of data).

The nice thing about StraightTalk is that they operate on AT&T’s network, so the SIM cards even appear to the phone as if they were AT&T SIM cards - hence, you can even use it with a locked AT&T iPhone.

The main problem with StraightTalk is their customer service. If you go to [HowardForums](http://www.howardforums.com) (my source for almost everything I know on this topic), you’ll see many tales of woe. Basically, if it works, it works fine; if anything goes wrong, good luck getting it fixed, because they will blame you, give you wrong information, and generally be completely unhelpful. Personally, I wouldn’t want to risk porting my number to them and possibly never getting it back, unless I had no other choice.

There are a bunch of other, smaller MVNOs as well. You can find them by searching, or looking around at HowardForums. If you don’t mind putting the time to research and experiment into it, they’re out there.

* * *

1. Other carriers, such as T-Mobile, do not do this; all of their customers use the same APN settings. One reason that AT&T likely does this is to segregate prepaid customers onto a separate section of their network, so as to give postpaid customers priority in the event of any clogged tubes. That’s right, move over to make room for the real customers, you prepaid moochers. Incidentally, if you’ve read the section about MVNOs, they are even lower down on the AT&T food chain than AT&T prepaid customers.&nbsp;[↩︎](#fnref:0)

2. T-Mobile refers to almost all of their data plans as 'unlimited’, because you don’t get cut off or charged more after you hit the limit (in this case 5 GB), it just slows down to sub-3G speeds. But it is, in no uncertain terms, limited. This deceptive marketing is the one thing I hate about T-Mobile right now.&nbsp;[↩︎](#fnref:2)

3. I know there is a 'non-customer’ option on that page. I’ve tried it. When you select that option, they demand the original sales receipt for the phone. Good luck.&nbsp;[↩︎](#fnref:1)

4. Here’s what I would suggest trying: order a micro-SIM online, activate it without porting your number, and sign up for the $30 plan that isn’t available in stores. Then bring the micro-SIM into a store and tell them you already have service and just want it transferred onto a nano-SIM. This will probably look pretty weird considering you never even put the micro-SIM in an actual phone. Only after you know this works in your iPhone 5, port your old number over (to avoid losing it if something goes wrong) - most carriers can do a port even after the new service is already active. Note, this is entirely speculative, I have not tried this and have no idea if it would really work!&nbsp;[↩︎](#fnref:up1)

5. Or more than full price: Virgin Mobile currently sells both the iPhone 4 and 4S for $100 _more_ than the unlocked price from Apple. (They don’t have the 5 yet.) For shame.&nbsp;[↩︎](#fnref:3)

