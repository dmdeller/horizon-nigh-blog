---
layout: post
title: Bundles, e-mail and you
date: '2007-08-07T17:28:05-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/7969292/bundles-e-mail-and-you
---
Playing around with Pages, I noticed that its file format (.pages) is a Mac OS X [bundle](http://en.wikipedia.org/wiki/Bundle_(NEXTSTEP)) - that is, a folder with multiple files inside that is itself treated by the operating system as a single file rather than a folder. This is also how Mac OS X applications (.app) are.

Of course, this presents several interesting technical hurdles when dealing with other operating systems, much like the old Mac OS resource fork used to. For example, you can’t download a bundle through your web browser; the web server will treat it as a directory with multiple files, and there’s just no way to download an entire directory at once over HTTP. (This also has a sort of interesting inherent security benefit, as it’s just not possible to directly download a bare Mac OS X application. It has to be inside a single-file format like .zip or .dmg.)

Anyway, I was wondering how this would work with e-mail, so I opened up Apple Mail and tried to send myself a .pages bundle. Mail let me choose the file and attach it just as though it were any normal file, and when I got it back on the other end, Mail let me view it or download it just as though it were any normal file. Iiiiinteresting. But from what little I know about MIME (the magic that makes e-mail file attachments work), this should be impossible. So I had a look at the raw e-mail source:

`--Apple-Mail-1--92203827Content-Transfer-Encoding: base64Content-Type: application/zip; x-mac-auto-archive=yes; name=untitled.pages.zipContent-Disposition: attachment; filename=untitled.pages.zip`

Keep in mind that I never zipped the file, and I when I looked at it on the receiving end, it didn’t look like a zip file, and saved to my desktop as an uncompressed .pages bundle. It looks like that ‘x-mac-auto-archive’ bit is what makes it work. Of course, this would be ignored on other operating systems, and so the attachment would show up for them as a .zip file (with contents that are not likely to be useful to them).

I guess it’s one of those things that I shouldn’t be surprised Just Works™, but I still find it neat.

