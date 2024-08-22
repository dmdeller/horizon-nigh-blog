---
layout: post
title: ParcelKit — Seamlessly integrate Core Data with Dropbox
date: '2013-07-18T19:48:15-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/55821604278/parcelkit-seamlessly-integrate-core-data-with-dropbox
---
[ParcelKit — Seamlessly integrate Core Data with Dropbox](https://github.com/overcommitted/ParcelKit)  

After thinking about it some more, I’m no longer as convinced as I was a few days ago of Dropbox’s inevitable dominance in the realm of third-party iOS app database syncing, for several reasons:

1. Dropbox’s [conflict resolution](https://www.dropbox.com/developers/datastore/tutorial/ios#conflicts) looks not great. I see what they’re going for: it’s fully automatic, so the user never has to make any choices. But there’s an obvious problem with that: sometimes, the algorithm is going to choose _wrong_. What then? The correct answer is, ‘the old version of the data can still be retrieved’. But as far as I can tell, the real answer is, 'the data is gone forever’. Hmm.
2. It’s a completely different pattern than Core Data, which is refreshingly simple. However… I happen to like Core Data, and I would miss a lot of the features that Core Data provides for me.
3. I finally found time to watch some of the WWDC '13 videos, and I’m tentatively willing to believe that the iCloud improvements in iOS 7 are a step in the right direction.

However, ParcelKit, if it works, just removed reason #2.

