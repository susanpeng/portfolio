---
title: "Hugo How To"
date: 2022-01-24T01:37:56+08:00
lastmod: 2022-01-24T01:37:56+08:00
draft: false
tags: ["Howto", "Hugo"]
categories: [""]
author: "Susan"
---

this is the video I use to do it successfully finally
https://youtu.be/LIFvgrRxdt4
use hugo to generate a static website
mac
install hugo

create folder

pick and download theme

change config file

write your ocntent

hugo new post/my-first-post.md : create a new .md file in the post folder

hugo -t theme-name - generate static files

git remote -v: 

note!!

"you have to already created susanpeng.github.io repo, and push to main at lease once before"

create repo "portfolio"
on local computer
git clone https://github.com/susanpeng/portfolio.git
cd portfolio
hugo new site portfoliosite
cd portfoliosite
 get theme
 add content: hugo new post/my-first-post.md
run hugo server: hugo server
stop hugo server: ctl+c

create submodule:
git submodule add -b main https://github.com/susanpeng/susanpeng.github.io.git public

"public" is the folder under susanpeng/github.io, which is th submodule of io from "portfolio" repo


When get into the public folder, you will see: it is connect to the susanpeng.github.io repo.
yulin@Yulins-Mac-mini portfoliosite % cd public
yulin@Yulins-Mac-mini public % git remote -v
origin	https://github.com/susanpeng/susanpeng.github.io.git (fetch)
origin	https://github.com/susanpeng/susanpeng.github.io.git (push)




hugo command : 20220124

hugo new site mysite : create a new site locally
cd mysite: get into the site folder
hugo server: start a development server on this computer on 1313 port
-- getting a theme
ctl+c stop the hugo server
goto hugo site to pick a theme