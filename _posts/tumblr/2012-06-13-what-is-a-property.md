---
layout: post
title: What is a property?
date: '2012-06-13T09:54:40-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/25020997245/what-is-a-property
---
Brent Simmons has a [plea to use dot notation properly](http://inessential.com/2012/06/11/correcting_the_dots):

> 1. Use dot notation for properties.
> 2. Do not use dot notation for non-properties.

First, I agree that there should be a convention behind one’s use of dot notation, as with other syntax.

However, this plea is predicated on the notion that a property is determined by a particular syntax in Objective-C: in other words, a property is the thing you write by typing ’@property’.

But a property is really a conceptual thing: it represents the state or condition of an object. It’s easy to imagine an Objective-C without ’@property’ syntax; you would simply write all of the instance variables, getters, and setters by hand. Writing ’@property’ is merely a shortcut to doing this.

So what makes a property different than any other pair of methods, one of which takes a value and the other of which returns a value? It is the idea that a property shouldn’t have adverse affects beyond getting or setting the value. This is fundamental to the separation of concerns in object-oriented programming: each method is only concerned with the barest minimum unit of work, and complex software is made of many tiny parts that each do one simple thing very well, instead of long methods that do many various tasks that are only tangentially related.

So what does it mean to say that dot notation should only be used for ’@property’ declarations, and not for other things that conceptually behave as properties? Not very much, really: you’re only saying that the thing you’re calling was defined with a particular syntax; you’re not saying what it actually _is_ or _does_.

Moreover, I disagree that facilitating search-and-replace should be one of the primary goals of structuring code. In principle, code should be written, above all else, to be read and understood by humans, because reading code is harder than writing code; appeasing the mechanical tools should always come after this goal. Tools may come and go, but people might have to read and maintain that code for many years. We can always write new tools to help us refactor code; for example, why couldn’t Xcode have a more intelligent search that finds calls of a given method regardless of which (valid) syntax was used?<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">1</a></sup> If the compiler can understand it, IDE search should be able to as well.

So here’s the rule I use. I’m not saying it’s the best way or the correct way, but it works for me:

_Use dot notation for methods whose primary purpose is to retrieve or modify a discrete, specified element of the state of an object, while having minimal side-effects on other objects._

A simpler way of phrasing it:

_Dots are for **getting** and **setting** ; brackets are for **doing**._

You will notice that this rule includes methods like `count`, because conceptually, it is really just a getter; the fact that the value it returns is likely to have been calculated on-the-fly, rather than retrieved from an instance variable, is an implementation detail that API consumers like myself need not concern ourselves with.

I have also been known to use dot notation on class methods like `NSBundle.mainBundle` and `UIApplication.sharedApplication`, because these too are **getting** methods. Xcode’s auto-completion doesn’t (yet?) recognise these, but they compile and work as expected. But I avoid using dot notation for `removeLastObject` on an `NSMutableArray`, even though I technically could, because that is a **doing** method.

* * *

1. If Apple doesn’t want to make it, someone else can. There are already powerful external code search tools like [ack](http://betterthangrep.com/). And [mogenerator](http://rentzsch.github.com/mogenerator/) is an example of a developer external to Apple improving an area where the Xcode tools are lacking.&nbsp;[↩︎](#fnref:2)

