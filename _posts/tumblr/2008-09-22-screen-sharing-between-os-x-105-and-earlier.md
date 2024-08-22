---
layout: post
title: Screen Sharing between OS X 10.5 and earlier versions
date: '2008-09-22T18:55:00-07:00'
tags:
- leopard
- mac
- howto
tumblr_url: https://blog.horizon-nigh.org/post/51303067/screen-sharing-between-os-x-105-and-earlier
---
Here’s something that took me by surprise when I found out: the new ’[screen sharing](http://www.apple.com/macosx/features/300.html#finder)’ feature in Mac OS X 10.5 works not only with other computers running 10.5, but also versions going back to 10.2 (though I’ve only tried with 10.4 and 10.3).

Only 10.5 has the ‘screen sharing’ service in System Preferences \> Sharing, but it turns out that if you enable Apple Remote Desktop in the same location on earlier versions, you can then connect **to** the older computer **from** one running 10.5. (Note that this will not work vice versa.)

Computers running 10.3 or 10.2 will need to install [this update](http://www.apple.com/downloads/macosx/apple/application_updates/appleremotedesktop22client.html) first.

There are several ways to start the session:

- In Finder, if you use the browser view (default), select the computer from the sidebar and click Share Screen.
- In Finder, choose Network from the Go menu. Open the computer’s icon and click Share Screen.
- Browse to System : Library : CoreServices, open the Screen Sharing application, and enter an IP address or hostname. (I made an alias to this application - just don’t move the original.)

This is very handy in the case of my company because we have many machines still running 10.4 and a few running 10.3, but can’t justify $500 for the Apple Remote Desktop administration software. Of course, Screen Sharing has fewer features than ARD, but it basically does the job.

