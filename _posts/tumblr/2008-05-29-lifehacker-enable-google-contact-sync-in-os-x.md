---
layout: post
title: 'Lifehacker: Enable Google Contact Sync in OS X'
date: '2008-05-29T18:18:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/36502414/lifehacker-enable-google-contact-sync-in-os-x
---
[Lifehacker: Enable Google Contact Sync in OS X](http://lifehacker.com/393855/enable-google-contact-sync-without-an-iphone-or-ipod-touch)  

Mac OS X 10.5.3 has a new feature that can synchronise a Gmail address book with the computer’s Address Book. Strangely, this is only available if you own an iPhone. However, removing this limitation is trivial.

The best solution is in the linked comments. Open Terminal.app and type this:

> defaults write com.apple.iPod Devices -dict-add invisibl-eyefown ’{ “Family ID” = 10001; }’

This creates settings for a fake ‘device’ that looks like an iPhone (thus enabling the feature) but won’t interfere with your current iPod or future iPhone.

According to Little Snitch, the sync actually occurs only when you connect an iPod - doesn’t matter what kind, as long as the setting is activated in Address Book.

