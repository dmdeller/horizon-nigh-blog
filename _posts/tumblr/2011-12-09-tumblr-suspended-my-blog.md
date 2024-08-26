---
layout: post
title: Tumblr suspended my blog
date: '2011-12-09T17:59:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/13985745470/tumblr-suspended-my-blog
---
Around 5 PM yesterday, I went to post a quote, and discovered that my blog (this) had been suspended by Tumblr. Attempting to post using [MarsEdit](http://www.red-sweater.com/marsedit/) gave an API error; attempting to get to the blog homepage gave a 404; and attempting to get to any part of the main Tumblr web site got me caught in an infinite redirect loop.

As instructed on the 404 page, I sent an email to support@tumblr.com with everything I knew. And then I waited.

This was a particularly bad time for this to happen to me, because I had intended to pass along my web site URL to some new professional contacts that very evening. There is more to my web site than just the blog, but still: it doesn’t look very professional if following a link on your home page leads to a 404.

To Tumblr’s credit, they replied and fixed my blog within two hours, outside of normal business hours (their main office is in NYC, as far as I know):

> Hello David,
> 
> Your content has been restored. We are sorry that this problem occurred and will ensure that it does not happen again.
> 
> Try deleting your web browser’s cookies for Tumblr.com and see if that helps. Let me know if you still have a problem.
> 
> Info on how to delete cookies is at:
> 
> [http://www.aboutcookies.org/Default.aspx?page=2](http://www.aboutcookies.org/Default.aspx?page=2)
> 
> Please let me know if there’s anything else I can help you with.
> 
> Thanks for using Tumblr!

Quick resolution and an apology, but no explanation. I guess that’s 2 out of 3.

Reading between the lines here, with some relatively unfounded assumptions, here’s my best guess as to what happened:

1. Tumblr has some kind of automated spam detector, and my blog got flagged. Presumably they don’t have a human reviewing these as it would take too long, so they just automatically suspend the blog immediately. Perhaps it’s because of all of my recent writing about certain [braaands](https://twitter.com/marcoarment/status/145139084975804418)? Who knows.

2. The support person reverted the ‘spam’ flag on my blog, and set some kind of new flag that prevents me from being automatically flagged as spam again.

The above is entirely speculation - I could be wrong about all of it. But, for lack of an explanation from Tumblr, it’s one possible story that fits what I saw.

But this incident made me realise some other troubling things about my use of Tumblr.

## The will to back up

I didn’t have any backups of my Tumblr blog. When they suspended it, four years of writing, as far as I knew, was _gone_. Granted, this is mainly my fault. Tumblr even provides [a Mac app that will back up your Tumblr blog to your computer](http://staff.tumblr.com/post/286303145/tumblr-backup-mac-beta), which I immediately used after my blog was restored. However, this has some further problems:

- The app has only had a single beta release, which is two years old. This makes sense once you know that [the co-founder who wrote it](http://www.marco.org) doesn’t work there any more, and in fact [doesn’t even use Tumblr any more](http://www.marco.org/secondcrack). But it doesn’t speak well to how long this app will be officially supported by Tumblr. I calculate an [85% probability](http://zeldawiki.org/Fi) that it will suddenly and permanently stop working at some point in the future.
- Even now, the app fails cryptically sometimes. Retrying immediately a few times in a row will eventually get it to work. But that’s worrisome.
- Backing up is a manual process. Every sysadmin knows that one the cardinal rules of backing is that it _must_ be automatic, otherwise it simply will not get done.
- It’s Mac-only. This isn’t a problem for me, but it might be for some people. Or it might be a problem for me in the future.

In sum, it would be much better if this app were written in a well-supported, portable scripting language, and open-source, so that there was some reasonable assurance it will continue to work in the future, and so that it could be configured to run automatically. I’m usually a strong proponent of native apps, but in this case, a great UI is not a meaningful advantage and does not outweigh the disadvantages.

## Bureaucratic loop

I mentioned before that visiting any Tumblr page while my blog was suspended resulted in a redirect loop. I couldn’t even get to the support site to see if that had any information. I wasn’t even sure to a certainty that I was suspended: my only clue was the URL, which didn’t tell me much.

As a web developer, this is a fairly rookie mistake that I myself have made at least once. It happens when you set up a rule like this to be executed on every page request (in [pseudocode](http://en.wikipedia.org/wiki/Pseudocode)):

    if (user is suspended) then
      redirect user to "your account is suspended" error page
    else
      show the page the user requested
    end

See a flaw in this logic? What happens when the user requests the error page?

The same thing that happens when the user tries to visit any page: they get redirected to the error page. Even though that’s the page they requested in the first place. Because there’s nothing in the above logic to handle the case in which the error page was where they were trying to get to. The flow goes like this:

1. System sets user status to suspended
2. User requests home page
3. System checks if user is suspended
4. System redirects user to error page
5. User requests error page
6. Go to line 3

This type of mistake is fairly common, to the point where most web browsers will stop after receiving several redirects in a row from the same site, and display an error message. (Safari’s [looks like this](http://cl.ly/0c0D170o1j023r421Q1m).)

The fact that this mistake exists isn’t enough to bother me, because I know how easy a mistake it is to make. But it’s also an easy mistake to fix, and the fact that it’s remained unfixed [after at least three years of Tumblr being aware of it](http://getsatisfaction.com/tumblr/topics/cannot_login_to_tumblr_firefox_redirect_loop_help) suggests something else about Tumblr.

Indeed, the support response above suggests a lack of understanding about why the redirect loop is happening, and the likely conclusion that it must be some kind of 'cookies thing’ that is probably the user’s fault, probably based on someone’s past experience that cookies can cause mysterious problems that are nobody’s fault and things just start working if you clear them.

Either the bug report about the redirect loop never made it to the bug team, or it was incorrectly bounced back as 'user error’.

Unfortunately, the advice for clearing cookies is not going to help anyone. To illustrate why, here’s a truth table showing the different states the user can be in (suspended or not, logged in or not) and the result of their actions.

<table> <tr> <th style="padding: 0.5em;">State # </th><th style="padding: 0.5em;">Suspended?</th> <th style="padding: 0.5em;">Logged in?</th> <th style="padding: 0.5em;">Result of requesting any page</th> <th style="padding: 0.5em;">Result of clearing cookies</th> </tr> <tr> <td>1</td> <td>No</td> <td>No</td> <td>Success</td> <td>None</td> </tr> <tr> <td>2</td> <td>No</td> <td>Yes</td> <td>Success</td> <td>Go to state #1</td> </tr> <tr> <td>3</td> <td>Yes</td> <td>No</td> <td>Success</td> <td>None</td> </tr> <tr> <td>4</td> <td>Yes</td> <td>Yes</td> <td>Redirect loop</td> <td>Go to state #3</td> </tr> </table>

As you can see, telling a logged-in, suspended user (state #4) to clear their cookies will only result in logging them out (state #3). As soon as they log in again, they will be in state #4 again and the problem will occur again, which is not helpful because presumably they want to be logged in. Whereas, if the user is not suspended (state #1 and #2), they will not experience the problem anyway, so there’s no reason to tell them to clear cookies. Clearing cookies does _nothing useful_ in any of these cases.<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>

So not only have Tumblr _not_ fixed the redirect loop in three years, but instead of fixing it, they seem to have institutionalised some kind of [cargo-cult](http://en.wikipedia.org/wiki/Cargo_cult) non-fix in their support responses to this problem, which allows the development team to avoid responsibility for the problem.

Ordinarily, as a user, I would shrug something like this off, since it’s a problem that will only ever affect a small number of users, and only those who needed to contact support anyway. But [a post today from Rachel By The Bay](http://rachelbythebay.com/w/2011/12/09/techtypes/) made me think more about it, after noticing the similarity to what she describes. I would categorise this as somewhere in between a 'replay’ and a 'ramrod’ response, as support in this case may be trying to replay a solution to an unrelated problem that happened in the past, despite lack of reasoning or evidence to suggest that it actually works.

Overall, the redirect loop was a minor problem compared to the larger problem of account suspension that I was having. But it still gives me pause because it’s a bureaucratic problem, rather than a technical problem, and the former are the most annoying kind because they’re so hard to work around.

## What now?

I don’t mean to pick on Tumblr too much; it’s still commendable that, for a free service that owes me nothing, I received better support from them than almost every service I pay for, especially those from big corporations.

But it’s clear that I’ve placed too much trust in Tumblr, compared to the importance I place on the data I let them keep for me. My resolution of this problem hinged on the fast and (mostly) accurate response from a support person; but as a technical user, I’m used to fixing problems on my own. I can’t predict what’s going to happen to Tumblr as a company, and I’m not comfortable assuming that I will get an equally good support response in the future, for problems caused through no fault of my own, which I am unable to fix myself.

So it seems like it’s time to move back to a self-hosted blog. This will not be fun.

For one thing, I love Tumblr’s clean and simple UI design; I have never seen any compelling alternatives. On the other hand, I mainly use MarsEdit to post these days, so I rarely see Tumblr’s UI any more anyway. Of the ones I know about:

- [Chyrp](http://chyrp.net/)’s main goal is to replicate Tumblr’s core functionality, including the Tumblr post types. It can even import Tumblr blogs. However, it seems lightly maintained (it was dead and resurrected at one point) and not very compatible with MarsEdit. And there are time costs related to using software that isn’t widely-used, as you’re more likely to run into problems that nobody has encountered before. Like Marco Arment says, you never want to be the biggest user of any software.
- [WordPress](http://wordpress.org/) is the popular behemoth, but it’s famous for its security holes and performance problems. It seems like every time I read about it, there’s a different caching plugin you’re supposed to use just to get decent performance; this alone seems like something that should be a Solved Problem, built-in to the core functionality. The fact that it’s apparently not is very concerning.
- [Movable Type](http://movabletype.org/) is also fairly popular behind WordPress, and (if I recall correctly) uses static HTML pages for ideal performance. I still get the impression that it has way too much in the way of features and clutter than I need, but it’s looking like the best option right now.
- Or I could just write my own, but that’s just so cliché at this point, and there are more interesting things I could be working on.

Migrating data to another system is usually difficult and tedious, especially when you’re as concerned as I am about preserving the original data as closely as possible (including the original URLs, design, etc.) There seem to be very few existing ways to move data from Tumblr to something else, so I will probably have to write my own.

Clearly, it’s not something I’ll be able to do quickly or easily, but having control over my blog should make it worthwhile.

* * *

1. Of course, there may be more cases than the ones I know about, in which case, my analysis would be incomplete.&nbsp;[↩︎](#fnref:1)

