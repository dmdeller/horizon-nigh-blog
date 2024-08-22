---
layout: post
title: iPhoto Feed with Picasa Web Albums
date: '2008-10-12T21:35:00-07:00'
tags:
- apple
- google
- howto
- iphoto
- mac
- picasa
- rss
- hack
- url
tumblr_url: https://blog.horizon-nigh.org/post/54271065/iphoto-feed-with-picasa-web-albums
---
Here’s a how to get a feed that works with iPhoto from someone’s Picasa Web Album.

Go to the person’s Picasa Web Albums home page. This is the page that shows all of their albums at once. Click the ‘RSS’ link at the bottom of the page. This will give you a URL like:

> [http://picasaweb.google.com/data/feed/base/user/dmdeller?alt=rss&kind=album&hl=en\_US&access=public](http://picasaweb.google.com/data/feed/base/user/dmdeller?alt=rss&kind=album&hl=en_US&access=public)

But don’t do anything with it just yet. This feed only has one tiny thumbnail for each album, which is not what you want.

Where it says 'album’ in the URL, change that to 'photo’.

> [http://picasaweb.google.com/data/feed/base/user/dmdeller?alt=rss&kind=photo&hl=en\_US](http://picasaweb.google.com/data/feed/base/user/dmdeller?alt=rss&kind=photo&hl=en_US)

(I also removed the ’&access=public’ part. This doesn’t currently have any effect, because it will only show you public albums anyway; but I figured, asking for more is better.)

Copy the modified URL. In iPhoto, go to File \> Subscribe to Photo Feed… and paste the URL.

Now, you can get automatic updates of a friend’s photos, right from the comfort of iPhoto.

**Addendum** : if you want to link to this on a web site somewhere so that it will automatically open in iPhoto (without requring your visitors to copy/paste), just change the 'http://’ part to 'photo://’. This will probably only work for people who have iPhoto installed (namely, Mac users), so you should also provide the normal HTTP link.

