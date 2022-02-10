---
title: "Mac_Commands_Shortcuts"
date: 2022-02-03T01:37:56+08:00
lastmod: 2022-02-03T01:37:56+08:00
draft: false
tags: ["Mac", "Commands", "Shortcut"]
categories: [""]
author: "Susan"
---
<!--hiddenFromHomePage: true-->


| *Shortcut* | *Function* |
| --- | --- |
| ctl+k | Clear the terminal window |
| ctl+t | Open a new tab in the current window |


**Commands**

Find the PID of a process listening on a port (pass the -i flag and the port number to significantly speed up the searching):
```shell
$ lsof -Pi :3000
COMMAND   PID  USER   FD   TYPE            DEVICE SIZE/OFF NODE NAME
node    10832 yulin   27u  IPv4 0xc9491b9285959cf      0t0  TCP *:3000 (LISTEN)
```
Kill this process:
```shell
$ kill 10832
```
Port 3000 is the default port used by Node.

**Delete the .DS_Store file manually**
Get into the folder containing the .DS_Store file you want to delete.
```shell
find . -name '.DS_Store' -type f -delete
```
The .DS_Store file will disappear.

