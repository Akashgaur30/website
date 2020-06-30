---
title: Cannot Rename Folders on mapped drive
author: Chris Titus
type: post
date: 2013-04-15T21:46:08+00:00
url: /rename-folders-mapped-drive/
image: /wp-content/uploads/2013/04/map-network-drive-windows.png
categories:
  - Windows
  - Windows Server

---
This error message is displayed and I cannot rename folders on the mapped drive. By making a group policy change I was able to make this error go away.

`The drive that this file or folder is stored on does not allow long file names, or names containing blanks or any of the following characters: / : , ; * ? < > |`

## Solution: Create a GPO to fix

To resolve this problem, turn off Fast Logon Optimization. I recommend creating a GPO in your domain controller to achieve this. If its an isolated instance to one PC, you can use gpedit.msc to enforce it on that one PC.

### Group Policy Settings to Change

```
Computer Configuration\Administrative Templates\System\Logon\Always wait for the network at computer startup and logon
User Configuration\Administrative Templates\System\Scripts\Run logon scripts synchronously
```

I live stream on [Twitch][1] and encourage you to drop in and ask a question. I regularly publish on [YouTube][2] and [christitus.com][3], but if you need immediate assistance, check out our discord channel at [Chris Titus Tech Discord][4].

 [1]: https://twitch.tv/christitustech
 [2]: https://www.youtube.com/c/ChrisTitusTech
 [3]: https://www.christitus.com/
 [4]: https://www.christitus.com/discord
