---
layout: post
title: How I handle errors in iOS apps
date: '2019-04-03T15:26:21-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/183919472337/how-i-handle-errors-in-ios-apps
---
The way that an app handles errors can really make or break the user experience: It can be the difference between ‘does what I need’ and 'buggy mess’, even if nothing else is different! It’s reasonable to assume that every user will encounter an error at some point, but hard to predict which ones will be encountered the most. Therefore, handling all errors consistently is important.

When handling an error, I place it into one of three categories:

## 1. Programmer error

The app’s own internal logic, without any influence whatsoever from the user or from any external system, has gotten into a state that should never happen. In this case, I think it is appropriate to crash the app ASAP, whether through a `fatalError()`, or a force-unwrapped optional (`!`), or otherwise. This is **not** a general endoresement of force-unwrapping; it should be used sparingly and with extreme caution, however in this one very specific case, it may be appropriate. The reason I think it is appropriate to crash is so that the bug can be discovered by the programmer, or by QA, as soon as possible. Otherwise, the error may snowball into larger and more complex errors that will ultimately be much more difficult to debug.

## 2. External system error

Typically, this means a network request, or possibly an operating system API call, returned something unexpected. In this case, we have two choices, depending on how essential the task at hand was:

- If it was relatively inessential, try to continue without notifying the user (but do log a console message so it can be debugged if noticed by the programmer). For example, if a blog post is missing the author’s name, it’s better to display as much of the post as possible rather than throwing away the whole thing - even if the UI appears slightly broken without the author’s name displayed. The blog post is likely still useful to the user in some way, so there is no reason to deny it to them. Falling short of perfection is better than completely failing the user.
- If some essential functionality is missing that was fundamental to the task a user is attempting to execute, then it may be appropriate to inform the user with an error message and suggest trying again. Since the conditions that caused the error are outside of the app’s control, trying again may help (but don’t suggest it if we’re sure that it wouldn’t help). In any case, avoid using modal dialogs whenever possible, as frequent dialogs can become very frustrating and annoying for the user. **Never** display immediately consecutive modal dialogs. Find a way to integrate the error message into the UI in a non-intrusive way, if possible.

## 3. User error

If we think the user made a mistake, we should of course inform them so that the mistake can be corrected. But be careful (and empathetic) in how we communicate this: our assumptions may be wrong or incomplete, and the user’s point of view may be that the mistake was ours. Avoid using words that sound like assigning blame (either by blaming the user, or by blaming the software); not only is it distracting, it has a surprisingly high likelihood of being wrong. Integrating the error message into existing UI elements, rather than a modal dialog, is always less intrusive and generally a better experience. Follow [Apple’s HIG](https://developer.apple.com/design/human-interface-guidelines/ios/views/alerts/), and avoid being flippant or using words like 'oops’ or 'sorry’, which only serve as irritations when encountered repeatedly.

