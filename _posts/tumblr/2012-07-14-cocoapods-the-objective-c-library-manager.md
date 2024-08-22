---
layout: post
title: 'CocoaPods: The Objective-C Library Manager'
date: '2012-07-14T16:25:35-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/27211747452/cocoapods-the-objective-c-library-manager
---
[CocoaPods: The Objective-C Library Manager](http://cocoapods.org/)  

Found this today when I was troubleshooting some Xcode linker problem. If only I had known about it sooner!

Ruby on Rails developers will be immediately familiar with the concept: It’s basically [Bundler](http://gembundler.com) for iOS and Mac development, even down to the fact that it’s written in Ruby<sup id="fnref:1"><a href="#fn:1" class="footnote-ref" role="doc-noteref">1</a></sup>. In fact, after I learned Rails, Bundler was one of the things I realised was painfully absent from my Cocoa workflow, and I have been wishing for something like it for some time now.

For the uninitiated, here’s the gist: Instead of downloading random code from all over the internet and copying it into your Xcode project, you specify the name and version of the library you want in a config file, and CocoaPods does the rest.

The advantages of this are:

- You know where your libraries came from, and which version they are currently on.
- It’s easy to automatically update to newer versions of the libraries. Or not; you can specify on a per-library basis which ones should be updated, or even that some of them should receive minor updates only, but not major updates, based on the version number. So you can get the benefit of bug fixes, without worrying about the API changing under you.
- CocoaPods does all of the Xcode configuration for you. If you’ve ever tried to set up a static library in a multi-project workspace, you know what I’m talking about with this: It’s one area where Xcode is still really buggy and randomly blows up for no discernible reason. The CocoaPods people have apparently figured out how to work around these bugs and make it Just Work.

The main difference between Bundler and CocoaPods is that Bundler saves you from having to check all of your libraries into source control; the only thing you need to check in is Bundler’s config file. This allows you to keep your repository a clean, sacred sanctuary, reserved solely for the purpose of your code. This is possible because Bundler is part of the standard Rails toolchain and workflow, and Rails developers know to run `bundle install`, which re-downloads all of the libraries from their original web sites, immediately after checking out a project. CocoaPods, on the other hand, is obviously not standard or included with Xcode, and many people don’t know about it yet, so it’s still advisable to check in all of the third-party code to your repository. This will allow even developers who don’t know about CocoaPods to check out, compile and run your project, without needing to learn about or do anything extra<sup id="fnref:2"><a href="#fn:2" class="footnote-ref" role="doc-noteref">2</a></sup>, at the cost of continuing to have a bunch of code that doesn’t belong to you in your repository.

* * *

1. I mean… what else are you going to write it in? Objective-C? Ha!&nbsp;[↩︎](#fnref:1)

2. If you work with a team of developers, you probably know how difficult it can be to get everyone to use any given developer tool that isn’t part of the standard toolchain. This is also one of the reasons I like [git-subtree](http://blog.horizon-nigh.org/post/22064187559), although it looks like CocoaPod just replaced the majority of my use cases for git-subtree, at least as far as Objective-C is concerned.&nbsp;[↩︎](#fnref:2)

