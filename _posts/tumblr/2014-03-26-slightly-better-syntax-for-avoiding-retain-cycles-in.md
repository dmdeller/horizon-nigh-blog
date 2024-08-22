---
layout: post
title: Slightly better syntax for avoiding retain cycles in blocks
date: '2014-03-26T09:59:04-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/80776997412/slightly-better-syntax-for-avoiding-retain-cycles-in
---
Objective-C programmers who work with blocks are familiar with this Xcode warning: ‘Capturing [some variable] strongly in this block is likely to lead to a retain cycle’. Articles like [this one](http://blackpixel.com/blog/2014/03/capturing-myself.html) explain the problem pretty well, so I won’t recap it here. The solution is also pretty well-known.

My issue is with the syntax. Since it isn’t possible to _reference_ an existing defined variable weakly, it’s necessary to _redefine_ the variable as `__weak` outside of the block, before you can reference it inside the block.

    __weak FooClass weakFoo = foo;

The ` __typeof__ ()` macro can make this a little less brittle, by saving you the trouble of retyping the class name:

    __weak__ typeof__(foo) weakFoo = foo;

But that’s still pretty awful. It’s not just that it’s ugly (although it is–those underscores!), but it feels redundant to type such specific instructions over and over again in order to accomplish the same common task. The more code I have to spend doing the compiler’s busywork, the harder it is for someone reading my code to understand my intent.

So I’ve created the following two compiler macros to try to abstract this away, save myself some typing, and make my intent in the code more clear.

<script src="https://gist.github.com/dmdeller/9534976.js"></script><noscript>
    <a href="https://gist.github.com/dmdeller/9534976">View on GitHub</a>
</noscript>

I would love to see Apple make something like this built-in to the compiler. I suspect it would be possible to eliminate the 'capture’ step entirely and simply use a cast-like syntax such as `(weak)foo` inside the block.

