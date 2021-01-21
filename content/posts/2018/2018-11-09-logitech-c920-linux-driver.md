---
title: Logitech C920 Linux Driver | Fix Lag and Disable Auto-Focus
author: Chris Titus

date: 2018-11-09T20:36:56+00:00
url: /logitech-c920-linux-driver/
image: /images/2018/11/c920-pro-hd-webcam-refresh.png
categories:
  - Linux
tags:
  - Logitech
  - C920 WebCam

---
With my webcam, I was having major issues and tried looking for a Logitech C920 Linux Driver, as I have a Logitech C920 Webcam that is very laggy in Linux, but in Windows, I don&#8217;t have any issues. I found out that the autofocus and exposure were causing a ton of issues. After following this guide, you will be able to fix this issue. <!--more-->

## Logitech C920 Linux Driver Problem

So there isn&#8217;t a Logitech program to control and optimize your Logitech camera in Linux, like the Windows counterpart. However, there is a command line program that will allow you to change ANY setting on the Logitech camera. This is, in my opinion, way better than the Windows clunky Logitech Application. So let&#8217;s get our program to do just that and fix these horrible default settings.

### Install v4l-utils

**Ubuntu/Debian:**
  
`sudo apt-get install v4l-utils`
  
**Fedora/Centos:**
  
`sudo yum install v4l-utils`

### Change Settings using v4l-utils

Find your C920 Webcam or other webcams you need to switch the default settings on.

**Command:**
  
`v4l2-ctl --list-devices`
  
**Output:**
  
![c920-selection2](/images/2018/11/Selection_002.png)

### List controls for the Logitech C920

`v4l2-ctl -d /dev/video6 --list-ctrls`
  
**Output:**
  
![c920-selection3](/images/2018/11/Selection_003.png)

### There are two values we need to change to get the best performance from our webcam.

**Here is the command syntax:**
  
`v4l2-ctl -d /dev/video6 --set-ctrl=exposure_auto=1`  
`v4l2-ctl -d /dev/video6 --set-ctrl=focus_auto=0`

### Video Walkthrough

[![iscsi-ya](https://img.youtube.com/vi/7SZBQ5bqaWU/0.jpg)](https://www.youtube.com/watch?v=7SZBQ5bqaWU)  
_Note: YouTube Video - Hold Ctrl + Left Click to open in new window_

Now that you know about the Logitech C920 Linux Driver support and how it functions, you can fix it. I hope this helps you as it took me quite a while to hunt down this information.

## Chris Titus Tech

#### Social

- Twitter - <https://twitter.com/christitustech>
- YouTube - <https://youtube.com/c/ChrisTitusTech>
- Twitch - <https://twitch.tv/christitustech>
- Odysee / LBRY (Privacy) - <https://links.christitus.com/lbry>

#### Exclusive Content

- [ChrisTitus.com Members Section][1] (_CC Only_)
  - Digital Downloads with Guides and Pre-Built Images
  - Monthly Members Only Video
  - $5 Per Month (_100% of Proceeds goes to Chris Titus Tech_)
- [YouTube Chris Titus Tech Membership][2] (_All Payments Accepted_)
  - Monthly Members Only Video
  - YouTube Emojis for Comments and Live Chat
  - YouTube Badges that changes based on membership time for comments and chat.
  - All YouTube comments are highlighted when I review comments daily. 
  - $4.99 Per Month (_70% of the Proceeds goes to Chris Titus Tech_)

 [1]: https://portal.christitus.com
 [2]: https://links.christitus.com/join