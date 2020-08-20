---
title: "Opencore Mac"
type: post
date: 2020-06-27T19:44:42-05:00
url: /opencore-mac/
image: /images/2020-thumbs/opencore-mac.jpg
categories:
  - macOS 
tags:
  - OpenCore
---
This goes over how to install macOS on pretty much any piece of hardware.<!--more--> OpenCore is a relatively young project, but is by far my favorite. It teaches you the proper way to setup your system to work long term in the macOS ecosystem.

# OpenCore Wiki
Source for the content in this post is from [https://dortania.github.io/](https://dortania.github.io/).  
This knowledge base is fantastic for any information I glaze over or troubleshooting that isn't covered. It is much more indepth than this article, but can be confusing in parts. This article is meant to get you acquainted with OpenCore and fill in any missing gaps. 

## Why I Use OpenCore?
I use opencore for compatibility and everything can be setup in a non macOS environment. It also injects drivers support (kext) differently than past methods and is far more stable.
This also means updates are far less likely to break your system and boot times are just as fast as a regular mac, if not faster. 
I also find a larger amount of hardware is supported and the finished product is all contained neatly in an EFI partition.

## Hardware Compatibility
Even with OpenCore supporting a lot more hardware there is still some hardware that simply will not work on macOS no matter what you do. Here is a definitive guide [https://dortania.github.io/Anti-Hackintosh-Buyers-Guide/](https://dortania.github.io/Anti-Hackintosh-Buyers-Guide/).
The TLDR of that guide is the last two generations of nVidia Graphics Cards and future nVidia Cards are not compatible, and even old nVidia cards will not work past High Sierra (10.13.x). Also, almost every Intel Wireless card will not function properly or work at all. So buying a replacement is needed for laptops. 
AMD CPUs can technically work, but will require more tinkering and are more difficult than the Intel counterparts. 

## Files and Projects you need to download and what they do
Here is a list of all the files and GitHub projects that are used for OpenCore.

  - OpenCore GitHub (Base Project) - https://github.com/acidanthera/OpenCorePkg/releases
  - All Drivers, Kexts, and SSDTs - https://dortania.github.io/OpenCore-Desktop-Guide/ktext.html
  - GitMacOS GitHub (Download Official Apple PKGs) - https://github.com/corpnewt/gibMacOS
  - ProperTree (config.plist editing) - https://github.com/corpnewt/ProperTree
  - SSDTTime (DSDT Dump and SSDT creation) - https://github.com/corpnewt/SSDTTime
  - GenSMBIOS (Generate Serial and UUID) - https://github.com/corpnewt/GenSMBIOS

## Checklist for https://dortania.github.io/OpenCore-Desktop-Guide
1. Check Hardware Compatibility - Document all device IDs and firmware
2. Download All Projects and Files
3. Boot Into Linux and do a DSDT dump followed by creating SSDT files for your computer (DO NOT USE PREBUILT!)
4. Delete all files that your system doesn't need
5. Put all Your Drivers in the EFI Folder *Note: I swapped AppleHDA for VoodooHDA on an old sound card. Do NOT just put every kext you find in one folder.*
6. Build config.plist and configure EVERY SINGLE Fold in the config.plist file to your computers specifications
7. Boot to Installer! *Note: This will probably fail the first couple times, it is very important to follow the config.plist guide and full auditing enabled*

## Contact Me

I live stream on [Chris Titus Tech YouTube Channel][1] every Friday at 10 AM CST and archive clips to [Titus Tech Talk][2]. I also regularly publish to [christitus.com][3], but if you'd like to contact me directly or want to contribute to help keep these articles and videos being made consider joining the CTT members. 

Two Memberships exist:
- [ChrisTitus.com Members Section][4] (_CC Only_)
  - Full Archive of All Unlisted Live Streams
  - Direct Members Only Email
  - Monthly Members Only Video
  - Starting at $2 Per Month (_100% of Proceeds goes to Chris Titus Tech_)
- [YouTube Chris Titus Tech Membership][5] (_All Payments Accepted_)
  - YouTube Emojis for Comments and Live Chat
  - YouTube Badges that changes based on membership time for comments and chat.
  - All YouTube comments are highlighted when I review comments daily. 
  - Immediate Access to Full Live Streams
  - $4.99 Per Month (_70% of the Proceeds goes to Chris Titus Tech_)

 [1]: https://www.youtube.com/c/ChrisTitusTech
 [2]: https://www.youtube.com/c/ChrisTitusTechStreams
 [3]: https://christitus.com/
 [4]: https://christitus.com/members
 [5]: https://links.christitus.com/join