---
layout: post
title: Oh, HSBC, how do I hate thee?
date: '2007-05-22T16:52:23-07:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/2282561/oh-hsbc-how-do-i-hate-thee
---
Let me count the ways.

1. The entire premise behind your ‘virtual keyboard’ concept is flawed, as it presents only a false sense of security. It is designed so that a keylogger (a program that subversively records every keystroke that you make) is unable to capture critical login details, as they are entered with this tool via the mouse instead of the keyboard. However, if one of your users has a keylogger installed in the first place, they certainly have much larger security problems and are going to have their identity stolen one way or another. Account numbers? SSN? Mother’s maiden name? All of these are so easily captured and can do so much harm to the exact same accounts you are purporting to protect, _if the user’s machine is already compromised._ And if it is not compromised, then your virtual keyboard provides absolutely no benefit. It does, however, provide considerable annoyance to all of your users.
2. The overwhelming majority of your users do not understand how the virtual keyboard is purporting to help them, making even the illusion of protection utterly useless.
3. There was a bug in the original implementation of the virtual keyboard that resulted in a double letter entry being mis-recorded as a triple letter. Unluckily for me, the password I chose ended in two of the same letter, which was recorded in the initial setup process as three of the same letter.
4. This bug was later silently fixed, rendering all of my subsequent login attempts with what I thought was the correct password impossible. Luckily for me, I eventually figured this out on my own. I don’t even want to think about how (un)helpful my bank’s outsourced customer service would have been, since even the people implementing this system are apparently oblivious to the implications of what they’re doing.  
5. Both the 'old style’ password (which you can actually type into with your keyboard) and the 'virtual keyboard’ are required to login, and they are both presented on the same page. When the page loads, the text insertion point (you know, the blinking vertical line) is automatically shifted to the 'old style’ password field, indicating that it is ready to accept the typing of your password. But wait! As soon as you begin typing, an alert box pops up telling you you’re using the virtual keyboard wrong… even though you weren’t trying to use the virtual keyboard at all! In short, the designers of this system cannot even grasp basic concepts about how a graphical user interface works.
Is there any bank these days that has a clue? I’ve heard that more and more of them are doing similar things.
