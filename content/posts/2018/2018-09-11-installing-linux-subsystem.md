---
title: Installing Linux Subsystem for Windows 10
author: Chris Titus
type: post
date: 2018-09-11T19:56:07+00:00
url: /installing-linux-subsystem/
image: /wp-content/uploads/2018/09/winubuntu.png
categories:
  - Linux
  - Windows
tags:
  - Powershell
  - Ubuntu Server
  - Windows 10
---
The following video goes over installing Linux Subsystem on Windows 10. Most notably it allows you to run Linux terminal commands in Windows 10 without having a virtual machine or dual boot into a Linux operating system. <!--more-->

[![WSL](https://img.youtube.com/vi/RriP3LmuKNA/0.jpg)](https://www.youtube.com/watch?v=RriP3LmuKNA)  
_Note: YouTube Video - Hold Ctrl + Left Click to open in new window_

## Enable Linux Subsystem Feature

`cd ~
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`  
_Note: Perform in PowerShell_ 

### PowerShell Installation Method

`Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
Rename-Item -Path ~/Ubuntu.appx -NewName Ubuntu.zip
Expand-Archive ~/Ubuntu.zip ~/Ubuntu cd Ubuntu ./ubuntu.exe` 

### Microsoft Store Installation Method

  * Open the Microsoft Store
  * Browse to Ubuntu-1604 and subsequently click the Install button

## Conclusion

In Closing The Linux Subsystem is a welcomed addition to Windows 10 because most things that come from the Microsoft store are garbage. Above all using this will give you the ability to check out and compile many GitHub projects. It is now one of the first options I enable when I do fresh installs of Windows 10 due to the fact Linux is not practical all the time. Leave any Questions and Comments below and I’ll get back to you. I regularly publish on 

## Contact Me

I live stream on [Chris Titus Tech YouTube Channel][1] every Friday at 10 AM CST and archive clips to [Titus Tech Talk][2]. I also regularly publish to [christitus.com][3], but if you'd like to contact me directly or want to contribute to help keep these articles and videos being made consider joining the CTT members. 

Two Memberships exist:
- [ChrisTitus.com Members Section][4] (_CC Only_)
  - Full Archive of All Unlisted Live Streams
  - Digital Downloads with Guides and Pre-Built Images
  - Monthly Members Only Video
  - $5 Per Month (_100% of Proceeds goes to Chris Titus Tech_)
- [YouTube Chris Titus Tech Membership][5] (_All Payments Accepted_)
  - YouTube Emojis for Comments and Live Chat
  - YouTube Badges that changes based on membership time for comments and chat.
  - All YouTube comments are highlighted when I review comments daily. 
  - Immediate Access to Full Live Streams
  - $4.99 Per Month (_70% of the Proceeds goes to Chris Titus Tech_)

 [1]: https://www.youtube.com/c/ChrisTitusTech
 [2]: https://www.youtube.com/c/ChrisTitusTechStreams
 [3]: https://christitus.com/
 [4]: https://portal.christitus.com
 [5]: https://links.christitus.com/join