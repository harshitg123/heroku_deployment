# Heroku  <img src="heroku/heroku.png"/> 

Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

## Prepare Your Application.
<p> You have to make modification in two files for able to deploy your application on heroku. </p>
 
1. In your  `server.js`  file. Add below mentioned code where your port is defined, This will randomly generate the port available on heroku.

```
  let port = process.env.PORT
      
  if(port == null || port == ""){
    port = 3000;
  }
```   

2. In your  `package.json`  file add the following command in `scripts` object, Follow this step if you want to deploy from github, Otherwise skip this step.    

```
  "scripts": {
    "start": "node app.js"
  }
```

## Deploying from GitHub
<p> On your git bash run following command to push your project on github repo. </p>

```
  git remote add origin https://github.com/<username>/<repository name>.git
  
  git add .
  
  git commit -m <commit msg in quotes "" or ''>
  
  git push origin main
  
```
### Now follow these six simple steps.

Step 1: Loggin to heroku and click on `New ^`|  Step 2: Click on `Create new app`
:-------------------------------------------:|:-------------------------------------------:
![](heroku/1.jpeg)                           |  ![](heroku/2.jpeg)

Step 3: Give your app name and click on `Create app`|  Step 4: Click on `GitHub`
:-------------------------------------------:|:-------------------------------------------:
![](heroku/3.PNG)                           |  ![](heroku/4a.jpg)

Step 5: Search the repo you want to deploy & click on `Connect` | Step 6: Scroll down & click on `Deploy Branch`
:-----------------------------------------:|:-------------------------------------------:
![](heroku/4.jpeg)                         | ![](heroku/5.jpeg)

If you have followed these six steps ☝️ to deploy, you would have successfully deployed your web application or website. After that heroku will give you the option to see your deployed app on the top & bottom.  

# Deploying from heroku CLI & command Line.

## Enviroment variables `.env` file
Now, If you are having some type of secrets / environment variables in `.env` file then you might come up with unsuccessful deployment i.e whenever you open your app, may crash.


