---
title: "Deploy Node.js to Heroku"
Date: 2022-01-25
---
Upload node.js to Heroku How to


restful folder: Desktop/restful


Create a free heroku account.

Ceate a new app "morning67890".


Download: heroku Command Line Interface(CLI)
```shell
brew install heroku/brew/heroku
```

?clone the restapitest




In restful folder: 
```shell
heroku login
check node version: node --version; shoulde be higher than 10
check npm version: npm --version; should be higher than
check git version: git --version
```
node version shoulde be higher than 10.

npm version should be higher than ??.

**make sure the node.js is runing locally without problem**
```shell
npm install nodemon --save-dev
```
Try to run, got:
```shell
node server.js
Error: Cannot find module 'swagger-ui-express'
```
Install swagger-ui-express.

```shell
npm install swagger-ui-express
```
After install, run; got:
```
node server.js
Error: Cannot find module 'joi'
```
Then install joi:
```shell
npm install joi
```
After install joi, server.js runs successfully.

**Deploy the app**
Create an app on Heroku. You can careate on the Heroku website or from local computer.

Create new app locallly. Open Terminal:
```shell
heroku create
```

How to delete/destroy a Heroku application
```shell
heroku apps:destroy
```



Create a new git repository - morning67890 from heroku website.

Open Terminal.

```shell
cd my-project 
git init

heroku login

heroku git:remote -a node.js-new-website
```
deploy your application
```
git add . 
git commit -am "make it better"
git push heroku master
```
That is it.
If it is not working, check logs to find out the reasons:
```shell
heroku logs
```

