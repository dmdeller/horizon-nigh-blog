---
layout: post
title: Downloading albums from Kodak Gallery
date: '2009-08-01T14:40:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/153759044/downloading-albums-from-kodak-gallery
---
Like [many](http://www.shutterfly.com/) photo sharing services, [Kodak Gallery](http://www.kodakgallery.com/Welcome.jsp) holds your friends’ photos hostage, in a short-sighted attempt to make you buy things from them. Despite [a misleading ad campaign](http://ofotopop.custhelp.com/cgi-bin/ofotopop.cfg/php/enduser/olh_adp.php?p_faqid=471&p_olh=1), if your friend uses the service to share photos with you, they make it impossible for anyone but the person who originally uploaded them to download the original, full-resolution copies. (Aside: what is the point of that? If you uploaded them in the first place, you presumably have the files already.)

I don’t have a solution for this, but I cooked up a workaround that may be better than nothing: [this script](http://gist.github.com/159766) will automatically discover and download 640x480 copies of every photo in a Kodak shared album. This resolution is very far from ideal, but it is the best I could figure out how to hack out of their system (if anyone knows of a better way, please do let me know).

First, log in to Kodak, go to the shared album, and download the page that has thumbnails of every photo (just the plain HTML file will do). The script can’t do this automatically because it requires authentication.

Then run the script as so (you need PHP installed):

php kodak-steal.php saved-page.html

Hopefully this little trick helps someone else out there on the interwebs.

P.S.: [Flickr](http://flickr.com) and [Picasa](http://picasaweb.google.com) let you download the full-resolution files (or the highest resolution that the person has chosen to upload).

**Edit:** [it’s worse than I knew.](http://twitter.com/dmdeller/status/3317338067)

