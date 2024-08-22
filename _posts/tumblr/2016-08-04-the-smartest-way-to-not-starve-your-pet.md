---
layout: post
title: The smartest way to not starve your pet. Hopefully.
date: '2016-08-04T20:51:52-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/148472309637/the-smartest-way-to-not-starve-your-pet
---
Petnet is a [small company](http://petnet.io/about) that makes an automatic pet feeder<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">1</a></sup>. You may have heard about them last week, when their product stopped working<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">2</a></sup>.

> No treat for you: pets miss meals after auto-feeding app PetNet glitches [https://t.co/WrRRfqB2iv](https://t.co/WrRRfqB2iv)
> 
> — The Guardian (@guardian) [July 27, 2016](https://twitter.com/guardian/status/758441102726791168)

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This, naturally, led to some questions.

> can someone explain to me why a pet feeder needs to be online  
> it literally  
> is just a timer
> 
> — Internet of Shit (@internetofshit) [July 27, 2016](https://twitter.com/internetofshit/status/758297570414325760)

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

I have owned this product for about six months, so perhaps it might be interesting to share my experience.

* * *

We live with a cat<sup id="fnref:6"><a href="#fn:6" class="footnote-ref" role="doc-noteref">3</a></sup>, and like many cats, she has very specific opinions about what time of day she should eat, and is not at all receptive to attempts to convince her otherwise. Her schedule often coincides with times that we would rather remain asleep. So one day, I finally, reluctantly, began a search for automatic pet feeders on Amazon, as one does.

There are many different models available, and like most categories of consumer products, the majority appear to be garbage. Reading through the reviews, almost all of them have at least one specific, fatal flaw; usually stemming from how cheaply-made the product is. The ones that dispense food by letting it fall through a hatch tend to dispense very inaccurately, either too much or too little, randomly every time. The ones that have a segmented bowl that rotates to open a different portion tend to be flimsy and break after time, perhaps with assistance from a motivated animal. Many of them aren’t designed to keep food fresh for very long, so they require constant refilling. And all of them have a user interface in the form of a prehistoric 7-segment digital display with one or two inscrutable buttons, and need to be programmed in a similar fashion as the $20 K-Mart digital watch you owned in 1985.

All of them except one.

I wanted something that would improve my life in some small way; not replace one annoyance with another. I can deal with a meowing cat, to a certain extent: she is a force of nature, and expecting her to change would be silly. Nature is a wonder, and compared to it, we are nothing. Our role is to accept and enjoy it for what it is.

But as an engineer, I have a much harder time accepting bad products. Because I know enough to see that there is no good reason for them to be that way. Every time I have to fight with a bad UI, or a product that doesn’t work the way it’s supposed to, it adds a little more to my nagging feeling of existential dread, which accumulates over time until I am finally compelled to remove it from my life. I can’t understand how people who make things for a living could have so little care for their work, and it’s genuinely upsetting to me.

I don’t expect perfection. That would be a recipe for constant disappointment. But if I can spend a little more money in order to get something that looks to have been designed with a little bit of care, then I will gladly make that trade.

* * *

The Petnet isn’t perfect, but it does get some important things right:

- It dispenses the correct amount of food very accurately. (Despite the fact that the brand we buy has oddly-shaped kernels, and this is a fall-through-hatch design.)
- It’s sturdy, and less vulnerable (compared to the competition) against your pet physically hacking it.
- Before last week, it had never missed a scheduled feeding<sup id="fnref:3"><a href="#fn:3" class="footnote-ref" role="doc-noteref">4</a></sup>.
- Setting the schedules, and changing them later, is fairly quick and easy in the iPhone app.
- It includes a battery backup, so it can continue working through a several hours-long power outage.
- If you’re not home, and you want to give your pet a little extra food right now, you can do that by tapping a button in the app. We almost never _need_ this feature, but it’s surprisingly nice to have.

Of course, it is not without downsides. I don’t want to give you the impression that I haven’t been happy with the product; I have. But it’s easier to write in greater detail about what something gets wrong than what it gets right. So here goes:

- Overall, the app is very buggy. It often shows incorrect, outdated, or conflicting information; even immediately after making changes, it will either inaccurately show the change I just made, or continue to show old data. There is no apparent ‘refresh’ button or control anywhere in the app. As a workaround, force-quitting the app tends to result in it refreshing and showing the correct information, most of the time. If not for that workaround, this would be a much larger problem; without it, it is often impossible for me to know whether or not my cat has been fed today (for example).
- Supply level problems:
  - When I add more food to the food bin, the next time I use the app, it asks me to enter a percentage. It’s unclear to me how I should answer this question; is it asking for the current absolute value of the food bin, or how much I added? In either case, there is no way for me to provide an accurate answer. I just have to visually inspect the bin and guess.
  - The app (or device) frequently thinks that I added food when I did not. When this happens, it demands to know how much food I added. There is no way for me to say 'hey, you’re wrong, nothing happened actually’. I am forced to enter a value in order to proceed. This is particularly annoying because I don’t know if, as above, entering 'zero’ will overwrite the existing supply level to think it’s now empty, or if it will tell it that I added 'zero’ to the amount that’s already there.
  - Likely in part due to the aforementioned problems, the device appears to have no idea how much food is actually inside it, and likewise, no idea when it runs out of food. It will sometimes alert me that it is empty when it still has several weeks worth of supply remaining; other times, it will run out and have no idea that there is none left, happy spinning its motors twice a day on schedule to dispense nothing but air.
- Screen resolution problems:
  - The app does not natively support the iPhone 6 screen resolution, instead running in upscaled iPhone 5 mode. Given that the iPhone 6 was released in September 2014 (23 months ago as of writing), this is rather dramatically out-of-date.
  - The app does not support iPad screen resolutions, which means it runs on iPads in iPhone 4S mode.
  - The app UI is partially broken when running in iPhone 4S screen resolution (which also affects all iPads due to the above point).
- The UI is over-designed. It makes use of non-standard UI controls and unnecessarily confusing navigation. Animations are custom, slow, and annoying. While this stuff is a relatively minor detriment to usability (I’ve seen much worse apps, after all), speaking from experience, this kind of design can make an app more difficult and time-consuming for an engineer to maintain. Which might be one reason that it hasn’t received any significant updates in so long. It could also explain why it effectively only supports a single device screen size, frozen in time.
- A user account is required in order to use the app (and therefore the hardware product) at all. There is no mechanism for granting access to family members, other than sharing your account name and password with them. This seems like an obvious oversight.
- For those who need it, the app isn’t available on Android at all. Nor is there any web UI. You must own an iPhone.

* * *

So what’s missing from my long list of complaints? The requirement of a persistent internet connection. I had precisely this concern before I bought the product: What if we’re not home, and the power or the internet goes out? The built-in battery is supposed to take care of the former case.

I feel almost certain that I read somewhere before making the purchase that the device was supposed to continue to function in the event that it lost its network connection. But now (perhaps for good reason), I can find no such claim on the Petnet web site. In any event, it would only make sense to design the product this way: The device should have an internal timer that decides when to dispense food, and periodically synchronise with either the app or a server in order to make changes to that schedule. It’s hard to fathom how any engineer would implement it any other way, such that a server going down would result in a complete failure of the device. Engineers are _terrified_ of servers going down. There’s just no way they couldn’t have thought of this.

Which leads me to speculate about alternative ways this could have happen. Perhaps there was some kind of sync bug in the servers, that accidentally told the devices to erase their schedules, in a way that couldn’t quickly be fixed. Or perhaps the logic in the device firmware failed to properly handle a certain kind of network error (such as a timeout resulting from a server outage), in that instead of continuing as normal after an error, it simply hung and refused to do anything else. These aren’t the only possibilities, only the first ones I thought of.

* * *

This brings me to what is currently my single biggest complaint about the product: **Their corporate communication.**

We still don’t know what went wrong, or why. We don’t know what they did to fix it. We don’t know if it’s likely to happen again. And going by their responses so far, we’ll probably never know.

Petnet’s communication about this problem (on Twitter, on their blog, and in emails) has been noticeably devoid of anything like an honest attempt to explain what happened. And that, in itself, is a bigger problem than the technical one. It makes it feel like they’re trying to hide the true scope of the problem - _whether or not that is their actual intent_<sup id="fnref:5"><a href="#fn:5" class="footnote-ref" role="doc-noteref">5</a></sup>. And that erodes trust. As many have pointed out, the lives of some of their customers’ pets could depend on this product<sup id="fnref:4"><a href="#fn:4" class="footnote-ref" role="doc-noteref">6</a></sup>.

Here is part of their first email to me about the problem last week:

> We are experiencing some difficulties with one of our third party servers. This is currently being investigated and we will provide you with more information as we receive it from our partners.

The wording of this comes annoyingly close to trying to place all of the blame on someone else. Listen, folks. I bought _your_ product. _You_ are responsible for doing whatever it takes to make it work. It’s not _my_ fault who you decided to choose as vendors.

Here’s what they sent after declaring the issue resolved:

> As pet parents ourselves, we recognize that when it comes to our pets, even one hour is too long to wait when it’s time for a feeding. That’s why we were already working on a solution to prevent this issue from happening. The fix was ready, but still needed to be tested when this outage occurred. Our engineers were prepared to implement the solution and get your SmartFeeders back online as quickly as possible. Now that this update has been made, our platform is stronger and more reliable than ever. We have two fail safes in place making it virtually impossible for this to happen again and ensuring your pets will always be fed.

The tone of voice here is almost nauseatingly self-congratulatory. 'We were already working’. 'Our engineers were prepared’. Now is not the time to pat yourselves on the back. This kind of language only makes me feel like you’re not owning up to your mistakes.

And what assurances do we have now? 'Stronger and more reliable than ever’. 'Virtually impossible’. These words mean precisely _nothing_ to me. What did you people actually _do?_ I’m not asking to see your source code, here. But you could at least _attempt_ to give a lay-person’s explanation about what _general category of mistake_ was made, and what you learned from it, and _why_ it’s not going to happen again.

In short, this is unacceptable, and it has lowered my confidence in the product more than the incident itself.

* * *

I have had a few interactions with Petnet’s customer service since I have owned the product.

It comes with a stainless steel bowl insert, that you can remove occasionally and put in the dishwasher, in order for your pet to have a sanitary surface to eat from. The device does not function while this insert is removed, which meant we were needing to plan our dishwasher cycle around the device’s schedule, which was somewhat inconvenient. I emailed them asking if I could purchase a second insert. They replied right away and sent me another one for free. So that was a very nice experience, and I really did appreciate it.

We moved recently from the east coast to the west coast. I noticed that, however I adjusted the schedule, the device would always dispense three hours earlier than I told it to. I searched the app for a way to change the time zone, but could not find one. So I emailed support again, and they remotely accessed my device in order to make the change. While this solved one problem, it raised a new concern for me: I don’t own many other devices that can be remotely accessed by unknown people on a whim, and I don’t make it a general habit of owning such things. Previous to this, I was not aware that the device had been designed to allow for this kind of remote access (by persons other than myself). I won’t get into the full ramifications of this now, as I could easily spend an entire separate blog post doing so, but it did (and still does) give me some cause for concern. The only thing they apparently needed in order to gain access was my email address.

And then, finally, this morning. Before the morning alarm went off, our cat started making more noise than usual. I went to check the feeder, and although it has not missed a feeding since the server problems were resolved last week, this morning the bowl was empty. I checked the app, to find this:

![](http://horizon-nigh.s3.amazonaws.com/blog-media/petnet-fail.jpg)

Well, at least that’s somewhat of an improvement over the often-incorrect information that the app usually shows me. So I emailed support one more time, explaining the situation. After a few hours, they sent me this:

> If happens again please inform us. This seems to a _(sic)_ singular glitch hopefully.

Hopefully.

Again, no information about what went wrong. No information about why it might or might not happen again. No reason to believe that this product will ever be reliable. I just have to trust them. But I already did that, remember? When I bought the product? I took a leap of faith, and since then I’ve been let down. Twice, now. That kind of trust is not easily regained. You have to at least _try_ to work at it a little.

Look. The flaws in this product are, all things considered, not really a deal-breaker to me. The only thing it really needs to do is feed my cat most of the time, so that I can sleep in a little later. If it fails once in a while, then it will be an occasional annoyance, like waking up to find a hairball I have to clean up. And anyway, what else am I going to do? Go back to being woken up on the cat’s schedule every day? Try one of those other awful products? For now, this still seems like it might be the least-bad option. For other people, this whole fiasco might be a much bigger problem, but not for me.

What is a problem for me is that this kind of poor communication is not a reasonable or responsible way to conduct business.

If you go to Petnet’s web site, their motto is 'The smartest way to feed your pet.’ Like their app, I think that motto might need an update.

* * *

1. I can never remember what the actual product name is. Looking it up again just now, apparently it is called 'SmartFeeder’. I’m not sure why I can’t remember this - perhaps it is just too generic? I usually end up calling it 'the Petnet’, but that becomes even more confusing when it’s necessary to distinguish the company from the one product that it makes. I am certainly not a branding expert, and perhaps these problems are unique to me, but it feels like there is room for improvement here.&nbsp;[↩︎](#fnref:2)

2. [Their blog post about this](http://petnet.io/pet_health_blogs/update-regarding-the-recent-petnet-server-outage) says that only 'about 10 percent’ of customers were affected. I am one of those. I guess that means I’m just unlucky? Like everything else they have publicly said about this, all I can do is wonder about what they are basing that figure on, and how accurate it is.&nbsp;[↩︎](#fnref:1)

3. You’ll notice I didn’t say who owns who.&nbsp;[↩︎](#fnref:6)

4. Here, again, I am always searching for a better word. 'Feeding’ isn’t a good noun. It sounds ridiculous in an overly self-important way. But I haven’t thought of an appropriate alternative.&nbsp;[↩︎](#fnref:3)

5. This is, in a nutshell, why writing is important. It doesn’t matter what your intentions are, if you can’t explain yourself.&nbsp;[↩︎](#fnref:5)

6. Even before these problems started, I never would have trusted this product to work properly if I were away from home for an extended period of time (more than a day). I always made other arrangements for a human to make sure that our cat was taken care of, and I will obviously continue to do so. It’s simply not worth the risk, and I know all too well how easy it is for software to fail. Yet, inevitably, some people would and did place that level of trust in the product. And Petnet should have expected that.&nbsp;[↩︎](#fnref:4)

