---
layout: post
title: In defence of Duplicate
date: '2012-08-05T11:09:00-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/28767125851/in-defence-of-duplicate
---
Since Lion was released with a Duplicate command instead of a Save As command, there has been a lot of consternation. Mountain Lion has tried to assuage the concerns of those who miss the Old Way somewhat, by [bringing back Save As, hidden behind a modifier key](http://arstechnica.com/apple/2012/07/os-x-10-8/5/#document-model). Much of what I’m reading still expresses bewilderment that Apple ever tried to get rid of Save As in the first place, but I think it made sense, and still does.

The problem with Save As is that it has no real-world analogue. The only reason we’re all used to it is because it has been part of graphical computers for 28 years.

Consider the traditional Save As workflow:

1. Open an existing document
2. Make a bunch of changes to it, _without saving the original_.
3. Choose ‘Save As’ from the File menu, which simultaneously does three things:
  - Creates a new copy of the file
  - Saves your most recent changes in the new copy
  - Replaces the file you were looking at on the screen, which until now was the old copy with unsaved changes, with the new copy–although, given that the old copy with unsaved changes (which now no longer technically exists) looked the same as the new copy with your new changes, the only indication of this on the screen is the change of name in the title bar

How would you do this with a piece of paper? You couldn’t. For starters, step #2 is impossible to do in the real world - there is no concept of 'saved’ or 'not saved’. If you scribble on a piece of paper, you have immediately committed those changes to permanent storage. There’s no way not to. But the even bigger problem is step #3, which does several things at once - this is very confusing to someone who has limited or no concept of the computer’s file system.

So here’s a modified workflow that works with a physical piece of paper in the real world:

1. Take an existing document out of your file cabinet
2. Walk it down the hallway to the copying machine, and make a copy
3. Scribble some changes on the new copy

Much simpler, and it just so happens, this is the workflow that Apple is trying to use for the 'Duplicate’ functionality:

1. Open an existing file
2. Choose 'Duplicate’ from the File menu (now, both your original file, and the new file are still on the screen in separate windows)
3. Make a bunch of changes to the new file
4. Choose a name for the new file

Notice what’s missing in this? Just like in the real-world example, the concept of 'saved’ or 'not saved’ is _gone_.

However, something else got added: a fourth step. That, in a nutshell, is what people seem to be so bent up about: Apple made the same operation take longer. Apple broke their muscle memory.

## Disrupt all the things

Save As was always too abstract, too automatic, too hard to see what’s going on unless you have already learned something about the file system. Apple’s goal always has been that _you shouldn’t need to learn how a computer works in order to use one._

At this point in computing history, I feel like I shouldn’t really have to justify that the pros of being easier for new users outweigh the cons that the smaller pool of seasoned veterans will experience. Isn’t this a given by now?

Like every other trivial software (or hardware) change we’ve ever collectively thrown a tantrum about over the past three decades, I think we’ll all find that after we get used to it, we won’t even notice it any more. Just like switching from Windows to Mac, or from the command line to a GUI, there is very little about the old way that was actually 'better’, aside from the fact that we were used to it and already understood it.

So, [try finding a way to disrupt your workflow today](http://blog.horizon-nigh.org/post/8518693917), and see if you’re not better off for it. Make a radical change just because. Unlearn what you have learned. Maybe you’ll decide it’s better, and maybe you won’t; the process of experimentation, not the end result, is what matters. Train yourself to adapt to changes. That way, when the world changes out from under you, you will be able to see things for how they are, not for how they always used to be.

## I dub thee

You’ll notice that I put the 'choose a name’ step at the end, when technically you can do it at any point after step 2. If you try to close the duplicate file without choosing a new name, the app will give you a choice between picking a name immediately, or deleting the file. Mountain Lion tries to streamline this somewhat by, immediately after step 2, highlighting the titlebar and allowing you to type a new name _right then and there_, suggesting that, y'know, maybe it would be a really good idea to do so. However, it is still optional at that point: if you decline to type a name, you will be prompted as soon as you try to close the file–the same as in Lion. But if you do make any change to the highlighted titlebar, you will not then later see a prompt; it will be saved automatically to the same location as the original. And it’s worth noting that, in Lion or Mountain Lion, regardless of whatever choices you make about naming or not naming, you can quit the app or yank out the power cord at any point, and when you launch the app again, everything will be right back where it was.

The point is that choosing a name _still_ doesn’t require you to know anything about the 'saved’ or 'unsaved’ state of the file. The fact that you still have to choose a name at all is the only remaining part of this process that has no real-world analogue, since pieces of paper don’t have metadata (the justification for which is another topic entirely).

## Re-skewed

'Skeumorphic’ is a term that’s been widely used lately to describe how Apple’s apps, like Contacts, Calendar and Notes, are taking on more of the visual appearance of their real-world equivalents. But this effort culminates in more than just a graphical veneer.

Design is the way it works.

