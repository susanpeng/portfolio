---
title: "Deploy Node.js to Heroku"
Date: 2022-01-25
---
upload node.js to Heroku How to

Procfile
web: node app.js


restapi folder: Desktop/restapi

create a free heroku account
create an app restapitest
download: heroku cli

clone the restapitest




restapitest folder: heroku login
check node version: node --version; shoulde be higher than 10
check npm version: npm --version; should be higher than
check git version: git --version

### Deploy the app
create an app on Heroku

```
heroku create
```

How to delete/destroy a Heroku application
```
heroku apps:destroy
```



create a new git repository
```
cd my-project 

git init

heroku git:remote -a node.js-new-website
```
deploy your application
```
git add . 
git commit ps, "make it better"
git push heroku master
```
when push the first time I got:
! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'https://git.heroku.com/restfullapitest1.git'

Then I run
