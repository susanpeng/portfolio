---
title: "Get Started with GitHub"
date: 2017-08-30T01:37:56+08:00
lastmod: 2017-08-30T01:37:56+08:00
draft: false
tags: ["howto", "GitHub"]
categories: ["Howto"]
author: "Wikipedia"

---
<!-->
hiddenFromHomePage: true

this line can be added to the front matter to hide the md file to be displaied on the website.
-->
Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@susanpeng 
susanpeng
/
susanpeng.github.io
Public
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
susanpeng.github.io/writings/documents/howtousegithub.md

susanpeng make change on hot to usegithub.md
Latest commit a893a1f 7 days ago
 History
 1 contributor
77 lines (64 sloc)  4.22 KB
   
How to Start Using GigHub Last Updated: 20220117 （draft, not finished）

Based on this video: https://youtu.be/0Icla6TVNNo

Check if git has already been installed on my Mac computer
git --version (I got "git version 2.30.1 (Apple Git-130)"; that means I have already got git installed on my Mac.)
Download and install git if you haven't got git installed on your computer. go to:https://git-scm.com/

Sign up and create a GitHub account

Add your GitHub email and username to git git config --global user.email "pengyl@email.com" git config --global user.name "susanpeng"

Create a folder on your local computer for you to store your local version of GitHub repository. You can use either of the following ways.

On your Desktop, create a folder git_202201. (CMD+shidt+n, and then change the new folder's name to git_202201)
Go to Terminal: From Terminal, goto desktop (Mac)
cd /Users/yulin/Desktop
mkdir git_202201 or
mkdir /Users/yulin/Desktop/git_202201
Commands Terminal- goto the location of the project folder(In this artical, folder git_202201)

git init Up to now, you have established the gitHub folder on you computer and it is connected to the content in your gitHub account on GitHub website. Tips: "Command + Shift + . " let you see the folder with . (.git)in the front of it; it's a taggle commond shortcut. Use the taggle shortcut, you can make the .git folder visible or invisible.
git status (remember, you're still under the folder of git_202201, NOT git_202201/.git)
touch file1.txt (create a new file)
git status (You can see a new file is not on the stage)
git add file1.txt (Add the new file to the stage)
git status (you can see the new file is on the stage in green - under the line of "Changes to be committed:")
git commit -m "added file1.txt" (commit the new file to the main brunch, with the messag "added... ...")
git status (You can see no file(s) on the stage, all files are commited)
git push (You con't see the new file in GutHub until you run this line)
Delete a file or files (delete from finder folder, I did this first, maybe I didn't need to do it.)
git rm filename(s) (remove files; I found I need to write file one by one, can't use wildcard *)
git status (will show that changes to be committed)
git commit -m "files with filenames are deleted."
git push
==== Get repository on GitHub to local computer ===== To establish the connection between the GitHub repository and the local version of this repository, you have to do one of two things.

If you have all content on your local computer, you need to create a repository on GitHub, get its link, and then execute the following command:
git remote add origin https://github.com/susanpeng/susanpeng.github.io.git (link to the repository of susanpeng.github.io) And then you can push your change to the desired place.
git push -u origin master
git log (to see what you have done earlier)
git --help (to see the command list for git)
If you have your repository on GitHub first, and you have nothing on your local computer, you need to execute the following command:
git clone "location of your repository (get the repository from GitHub website to your local computer)
git remote -v (check if you have the remote repository on your local computer?) after making changes:
git add
git commit -m "message..."
git push (require for personal access token, generated on Jan 2, 20220101, and saved in OneNote for now) only on this point, my changes have been updated on GitHub website.
When I tried to add a file under the images folder, I got the following message: The following paths are ignored by one of your .gitignore files: images/techwriter.png hint: Use -f if you really want to add them. hint: Turn this message off by running hint: "git config advice.addIgnoredFile false"

git add -v -f images/techwriter.png

---- Rename a repository Go to the repository you want to rename. Go to Settings. under Repository name, change the nae, and then click Rename button. It is better to do "git clone "https:// ... address of new repository" and then just delete the old folder of this repository on your local computer. If the repository is not too big, this saves lots of confusion.

© 2022 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
Loading complete


other commond line

git rm --cached <file>: to stop tracking a file