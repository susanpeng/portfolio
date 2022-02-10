---
title: "Writing Samples Old"
date: 2022-01-31T01:37:56+08:00
lastmod: 2022-01-31T01:37:56+08:00
draft: true
tags: ["UsersManual", "OnlineHelp", "WritingSample"]
categories: ["Samples"]
author: "Susan"
---
My website "ylpeng" uses react.
It's in the Desktop/ylpengreact folder now.

On Friday, February 4, 2022, I uploaded it to GitHub ylpengreact repo. 

To start this app, go to terminal from ylpengreact folder:
```shell
$ npm start
```

It will start using port 3000 by default (node.js app's default port)
the URL is localhost:3000

After I uploaded it to GitHub, I built this react app locally. 
```shell
$ npm run build
```
I copied the **build** folder to Library/WebServer/Documents, Apache's document folder. It can run under Apache Web Server well but can't display larger images.

I also uploaded the build folder to the ylpengreact repo on GitHub. Wonderfully, it runs well there; also, it can't display larger images. It displays small images correctly, correct position and correct appearance.

Then I tried to make the larger images display for a long time but failed. I will do it later.

It has another issue. It will show blank and only work properly after changing the paths in the index.html file by taking away the beginning slash.