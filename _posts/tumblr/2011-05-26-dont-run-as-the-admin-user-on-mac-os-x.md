---
layout: post
title: "'Don't run as the admin user' on Mac OS X"
date: '2011-05-26T13:12:00-07:00'
tags:
- mac
- security
- longer post
tumblr_url: https://blog.horizon-nigh.org/post/5869002005/dont-run-as-the-admin-user-on-mac-os-x
---
I’ve been hearing this advice repeated a lot since the [Mac Defender](http://www.webcitation.org/query?url=http%3A%2F%2Farstechnica.com%2Fapple%2Fnews%2F2011%2F05%2Ffake-mac-defender-antivirus-app-scams-users-for-money-cc-numbers.ars&date=2011-05-26) stuff has broken out, mainly from Windows users/sysadmins. Since this is (or used to be) good advice on the Windows platform, they reason that it should apply anywhere.

The only thing that ‘being the admin user’ on the Mac gets you is the ability to make changes to common, non-system areas. For example: it allows you to place new files or software in the /Applications or /Library folders, without entering a password.

What it does not do is allow you to arbitrarily make changes to /System or other areas that are owned by root; those will still require a prompt for your password. That’s why Software Update, or installers that have to place things outside of /Applications, require your password even when you are an admin user.

Creating a new user account without admin permission, using it for day-to-day stuff, and entering your (other) admin user account’s name and password whenever you need to do something administrative, does not get you any additional security. Assuming you are the person who administers your own machine, you’ll just get the same password prompt that you would get even if you were an admin.

True, it will mean that you will now have to enter a password to drag stuff into /Applications. But it doesn’t mean you have to enter a password _to install software_; on the Mac (or even on Windows), you can just as easily install and run the software from any location on your hard disk, such as your home folder. Not only would this be trivial for malware to adapt to, it’s what [Mac Defender is already doing](http://www.webcitation.org/query?url=http%3A%2F%2Fwww.macrumors.com%2F2011%2F05%2F25%2Fnew-macdefender-variant-installs-without-admin-password-requirement%2F&date=2011-05-26).

There is one situation where I can see it might be useful: if you’re setting up a Mac for your parents<sup id="fnref:parental"><a href="#fn:parental" class="footnote-ref" role="doc-noteref">1</a></sup> or someone else whom you don’t trust to make educated administrative decisions. You could give them a non-admin account, set up a separate admin account and don’t give them the password. However, obviously if you do this, you also take on the considerable responsibility of administering their computer for them in perpetuity<sup id="fnref:updates"><a href="#fn:updates" class="footnote-ref" role="doc-noteref">2</a></sup>, which is not something to be taken lightly.

But if you’re the admin of your own Mac, there’s not much benefit to running as a user that doesn’t have admin permission.

* * *

1. In [the latest episode of The Talk Show](http://5by5.tv/talkshow/44), Gruber claims that the name of the 'Parental Controls’ pane in System Preferences is an in-joke with a double meaning amongst Apple employees; that most people think it’s there for parents to control their children, but it’s actually more useful for adults to keep their parents out of trouble.&nbsp;[↩︎](#fnref:parental)

2. Otherwise, they’ll never be able to run Software Update, even if they wanted to, and a remote [privilege escalation](http://www.webcitation.org/query?url=http%3A%2F%2Fen.wikipedia.org%2Fwiki%2FPrivilege_escalation&date=2011-05-26) exploit is going to come along someday and the machine won’t be protected. You’ve possibly made the machine even less secure than it was.&nbsp;[↩︎](#fnref:updates)

