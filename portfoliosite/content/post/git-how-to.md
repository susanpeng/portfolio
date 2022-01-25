---
title: "Get Started with GitHub"
date: 2022-01-25T01:37:56+08:00
lastmod: 2022-01-25T01:37:56+08:00
draft: false
tags: ["Howto", "GitHub"]
categories: [""]
author: "Susan"
---
<!--
hiddenFromHomePage: true
this line can be added to the front matter to hide the md file to be displaied on the website.
-->

Check if git has already been installed on my Mac:
```shell
git --version
git version 2.30.1 (Apple Git-130)
```
I got "git version 2.30.1 (Apple Git-130)"; that means I have already got git installed on my Mac.

Download and install git if you haven't got git installed on your computer. go to: https://git-scm.com/, and sign up. Then create a free GitHub account.

Add your GitHub email and username to git:
```shell
git config --global user.email "youremai@email.com" 
git config --global user.name "your-git-username"
```
Create a folder on your local computer for you to store your local version of GitHub repository. You can use either of the following ways:

- On your Desktop, create a folder git_202201. (CMD+shidt+n, and then change the new folder's name to git_202201)
- Go to Terminal. From Terminal, goto desktop (Mac)

    ```shell
    cd /Users/your-username-on-mac/Desktop
    mkdir git_202201
    ```
After creating the project folder (In this article, the folder is git_202201), open terminal and enter the project folder:

```shell
cd git_202201
git init
```
Up to now, you have established the gitHub folder on you computer and it is connected to the content in your gitHub account on GitHub website. 

Tips: "Command + Shift + . " let you see the folder or files with . in the front of it (such as .git); it's a taggle commond shortcut. Use the taggle shortcut, you can make the .git folder visible or invisible.
Check git status:
```shell
git status
```
Remember, you're still under the folder of git_202201, NOT git_202201/.git.
```shell
touch file1.txt
```
Create a new file.
```shell
git status
```
You can see a new file is not on the stage.
```shell
git add file1.txt
```
Add the new file to the stage.
```shell
git status
```
You can see the new file is on the stage in green. Under the line of "Changes to be committed:".
```shell
git commit -m "added file1.txt"
```
Commit the new file to the main brunch, with the messag "added file1.txt".
```shell
git status
```
You can see no file(s) on the stage. All files are commited.
```shell
git push
```
You con't see the new file in GutHub repositary until you run this line.

Delete a file or files. You don't need to delete file(s) or folder from finder first. Just execute the followin command in terminal.
```shell
git rm filename(s)
```
(remove files; I found I need to write file one by one, can't use wildcard *)
```shell
git status
```
You will see the list of deleted files; that is also changes need to be committed.
```shell
git commit -m "files with filenames are deleted."
git push
```
#### Get repository on GitHub to local computer
To establish the connection between the GitHub repository and the local version of the same repository, you have to do either one of the two things:

- If you have all content on your local computer, you need to create a repository on GitHub and get its link; then execute the following command:
    ```shell
    git remote add origin https://github.com/susanpeng/susanpeng.github.io.git 
    ```
    link to the repository of susanpeng.github.io. Then you can push your change to the repository on GitHub:
    ```shell
    git push -u origin master
    ```
    To see what you have done earlier
    ```shell
    git log 
    ```
    To see the command list for git:
    ```shell
    git --help
    ``` 
- If you already have your repository on GitHub, and have nothing on your local computer, you need to execute the following command:
    ```shell
    git clone "location of your repository"
    ```
    to get the repository from GitHub website to your local computer.
    You can check if you have the remote repository on your local computer:
    ```shell
    git remote -v
    ``` 
    After making changes:
    ```shell
    git add
    git commit -m "message..."
    git push 
    ```
When you push the first time, Git will as you for **personal access token**, you need to goto GutHub website to generated your personal access token to do your fist push.
on Jan 2, 20220101, and saved in OneNote for now) only on this point, my changes have been updated on GitHub website.
**Rename a repository**

Go to the repository you want to rename. Go to Settings. Under Repository name, change the name, and then click Rename button. It is better to do "git clone "https:// ... address of new repository" in a new folder, and later just delete the old folder of this repository on your local computer. If the repository is not too big, this will avoid lots confusion.



**Other commond lines**

To stop tracking a file:
```shell
git rm --cached <file>
```

These are some basic commands to get you started. For more specific and detailed information please refer to the documentation from GitHub website.