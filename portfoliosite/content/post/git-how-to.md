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
**Install git on the local computer**

Check if git has already been installed on my Mac:
```shell
git --version
git version 2.30.1 (Apple Git-130)
```
I got "git version 2.30.1 (Apple Git-130)"; that means I have already got git installed on my Mac.

If you can see the version information, you need to download and install git on your computer.

**Create a free GitHub account**

Go to GitHub website and sign up to get a free GitHub account.

**Config git on the local computer**

Add your GitHub email and username to git:
```shell
git config --global user.email "youremai@email.com" 
git config --global user.name "your-git-username"
```
Create a project folder on the local computer to store your local version of the GitHub repository. You can use either of the following ways:

- On your Desktop, create a folder git_202201 (you can use your desired folder name). 
Press CMD+shidt+n, and then change the new folder's name to git_202201.
- Go to Terminal. From Terminal, goto desktop (Mac)

    ```shell
    cd /Users/your-username-on-mac/Desktop
    mkdir git_202201
    ```
After creating the project folder (In this article, the folder is git_202201), open Terminal and enter the project folder:

```shell
cd git_202201
git init
```
Now, you have established the git folder on your computer, and it is connected to the content in your GitHub account on the GitHub website. 

Tips: "Command + Shift + . " let you see the folder or file with . in the front of it (such as .git); it's a taogle command shortcut. Using the toggle shortcut, you can make the .git folder visible or invisible.
Check git status:
```shell
git status
```
Remember, you're still under the folder of git_202201, NOT git_202201/.git.
Create a new file:
```shell
touch file1.txt
```
Check the status:
```shell
git status
```
You can see a new file is not on the stage.
Add the new file to the stage and check again:
```shell
git add file1.txt
git status
```
You can see the new file is on the stage in green. Under the line of "Changes to be committed:".

Commit the new file to the main brunch, with the message "added file1.txt":
```shell
git commit -m "added file1.txt"
git status
```
You can see no file on the stage. All changes are committed.

You can't see the new file in GitHub repository until you run this line:
```shell
git push
```


**Delete a file**

You don't need to delete a file or a folder from the Finder first. Just execute the following command:
```shell
git rm filename(s)
```
When removing files, I found that I needed to write each filename, couldn't use wildcard *.

Check the status:
```shell
git status
```
You will see the list of deleted files; that are also changes needed to be committed.

Commit the changes and push to the repo on GitHub:
```shell
git commit -m "files with filenames are deleted."
git push
```
**Get repository on GitHub to local computer**

To establish the connection between the GitHub repository and the local version of the same repository, you need to do one of the following two things according to your situation:

- If you have all content on your local computer, you need to create a repository on GitHub and get its link; then execute the following command:
    ```shell
    git remote add origin https://github.com/yourusername/yourusername.github.io.git 
    ```
    Here, we assume your repository's name is "yourusername.github.io".

    Then you can push your changes to the repository on GitHub:
    ```shell
    git push -u origin master
    ```
    To see what you have done earlier:
    ```shell
    git log 
    ```
    To see the command list for git:
    ```shell
    git --help
    ``` 
- If you already have your repository on GitHub and have nothing on your local computer, you need to execute the following command:
    ```shell
    git clone https://github.com/yourusername/yourusername.github.io.git 
    ```
    Then you will get the repository from the GitHub website to your local computer.
    You can check if you have the remote repository on your local computer:
    ```shell
    git remote -v
    ``` 
    After making changes:
    ```shell
    git add .
    git commit -m "message..."
    git push 
    ```
When you push the first time, you need to use your **personal access token**. You need to go to the GutHub website to generated your **personal access token** to complete your first push.

**Rename a repository**

Go to the repository you want to rename. Go to Settings. Under Repository name, change the name, and then click Rename button. It is better to do "git clone "https:// ... address of new repository" in a new folder, and later just delete the old folder of this repository on your local computer. If the repository is not too big, this will avoid lots of confusion.



**Other command lines**

To stop tracking a file:
```shell
git rm --cached <file>
```

These are some basic commands to get you started. For more specific and detailed information, please refer to the documentation from the GitHub website.