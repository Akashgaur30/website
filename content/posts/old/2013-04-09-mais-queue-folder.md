---
title: GFI MailArchiver MAIS Queue Folder has tons of emails stuck
author: Chris Titus
type: post
date: 2013-04-09T16:50:22+00:00
url: /mais-queue-folder/
image: /images/2013/04/MAIS-Queue-Folder.png
short-url:
  - http://bit.ly/10FKCsL
categories:
  - Windows Server
tags:
  - GFI MailArchiver

---
The Import service can get stuck and this will stop all the mail in the MAIS Queue Folder. These are the emails that have not been processed and added to GFI Archiver yet, so do not delete them. Below is the fix on how I restored the import service and processed all the stuck email.<!--more-->

## The Fix

Deleted all files **EXCEPT** for *.eml from `C:\Program Files (x86)\GFIMailArchiver\MAIS\Queue`

Renamed all \*.eml files to \*.txt (Command Prompt: ren \*.eml \*.txt)

Move all files to `C:\Program Files (x86)\GFIMailArchiver\MAIS\Pickup`

## In Closing

This will force GFI Mailarchiver to reprocess all these emails. I&#8217;d highly recommend doing all these operations from a command prompt as the sheer number of files in the folders can potentially lock up your server when using a Graphic User Interface. Once you restart your processes wait for the MAIS Queue Folder to reduce in size before checking again.

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