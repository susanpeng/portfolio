---
title: "Deploy Node.js to Heroku"
date: 2022-02-03T01:37:56+08:00
lastmod: 2022-02-03T01:37:56+08:00
draft: false
tags: ["Heroku", "Node.js", "RESTAPI"]
categories: [""]
author: "Susan"
---

I used the folder "Desktop/restful" as my REST API folder. 

First, create a free Heroku account.

Then, create a new app "morning67890" on Heroku.


Download the Heroku Command Line Interface(CLI)
```shell
$ brew install heroku/brew/heroku
```

I copyed all files of my RESTAPI from my old RESTAPI folder to the folder "Desktop/restful". 

Under "Desktop/restful" folder: 
```shell
$ heroku login
```
Check node version:
```shell
$ node --version
```
The noder version shoulde be higher than 10.

Check npm version:
```shell
$ npm --version
```
Check git version:
```shell
$ git --version
```


**Make sure the node.js is runing locally without problem**
```shell
$ npm install nodemon --save-dev
```
Try to run my API:
```shell
$ node server.js
Error: Cannot find module 'swagger-ui-express'
```
I should install swagger-ui-express.

```shell
npm install swagger-ui-express
```
Try to run my API again:
```shell
$ node server.js
Error: Cannot find module 'joi'
```
Then install joi:
```shell
$ npm install joi
```
After installed swagger-ui-express and joi, server.js runs successfully.

**Deploy the app**

Create an app on Heroku. You can careate on the Heroku web site or from local computer.

To create the new app locallly, open Terminal and type:
```shell
$ heroku create
```
To delete/destroy a Heroku application:
```shell
$ heroku apps:destroy
```
**Create a new git repository - morning67890 from heroku website**

Open Terminal and type:
```shell
$ cd my-project 
$ git init
$ heroku login
$ heroku git:remote -a node.js-new-website
```
Deploy your application:
```shell
$ git add . 
$ git commit -am "make it better"
$ git push heroku master
```
That is it.
If it doesn't work, check logs to find out the reasons:
```shell
$ heroku logs
```