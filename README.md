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
     
    
  

## Deploying from GitHub
<p> Push your Repository on github </p>
