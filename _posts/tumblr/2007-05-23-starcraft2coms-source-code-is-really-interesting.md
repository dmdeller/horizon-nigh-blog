---
layout: post
title: starcraft2.com's source code is really interesting
date: '2007-05-23T01:41:45-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/2300600/starcraft2coms-source-code-is-really-interesting
---
To a web designer, I mean. I got curious when I saw that their pages all end in ’.xml’. I figured they were just being cheeky, but when I checked, they’re actually throwing XML (not XHTML!) documents at you!  
  
For a page such as [http://www.starcraft2.com/faq.xml](http://www.starcraft2.com/faq.xml), the entirety of the source code is this:  
  
\<?xml version=“1.0” encoding=“UTF-8”?\>  
\<?xml-stylesheet type=“text/xsl” href=“/layout/faq.xsl”?\>  
  
\<page lang=“en\_us”\>  
&nbsp; \<faq/\>  
\</page\>  
  
&nbsp;Then in [/layout/faq.xsl](http://www.starcraft2.com/layout/faq.xsl), you’ve got stuff like this (just an excerpt):  
  
&nbsp;&nbsp; &nbsp;\<dt\>\<xsl:value-of select=“$loc/strs/str[@id=‘sc2.faq.basics.q1’]”/\>\</dt\>  
&nbsp;&nbsp; &nbsp;\<dd\>\<p\>\<xsl:value-of select=“$loc/strs/str[@id='sc2.faq.basics.a1’]”/\>\</p\>\</dd\>  
&nbsp;&nbsp; &nbsp;  
&nbsp;&nbsp; &nbsp;\<dt\>\<xsl:value-of select=“$loc/strs/str[@id='sc2.faq.basics.q2’]”/\>\</dt\>  
&nbsp;&nbsp; &nbsp;\<dd\>\<p\>\<xsl:value-of select=“$loc/strs/str[@id='sc2.faq.basics.a2’]”/\>\</p\>\</dd\>  
  
&nbsp;…which references stuff in [/layout/includes.xsl](http://www.starcraft2.com/layout/includes.xsl), which references stuff elsewhere… the rabbit hole just keeps going down.  
  
I know some of the basic concepts about XML and XSL, so I can only just begin to understand how it works. It’s really fascinating, though, because I’ve never seen web design like this before.

