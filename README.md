# Heroku
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
<p> Push your Repository on github </p>
