### Introduction 

Beside deploying application using Openshift console,   you can deploy application using Openshift CLI (oc) too.   In this exercise,  you will use oc commands to do the following: 

* Create new project
* Deploy .net core application

You will create 2 projects for different environment (development and SIT).   You will deploy the application into DEV.  In the next exercise,  you will deploy the same application into SIT. 

### Develop .net core application in Openshift using OC commands. 

* Create 2 projects for this application. 

```execute
oc new-project %username%-dev
```

```execute
oc new-project %username%-sit 
````

* Before deployng the application, make sure we are in the correct project.  

```execute
oc project %username%-dev
```

* Now we are in the correct project.  Let's deploy the .net core application.

```execute
oc new-app dotnet:3.1~https://github.com/redhat-developer/s2i-dotnetcore-ex#dotnetcore-3.1 --name=sampledotnet --context-dir app
```
![dotnet 01](./images/04/dotnet-01.png)

* Application is not exposed.   You need to expose services to the outside world by executing command below. 

```execute
oc expose service/sampledotnet
```
* The application is deployed successfully.   You can access it via the router.   Click on the **Console** tab.  Switch to **Administration**. Make sure that you select `%username%-dev` as project.  Click on **Networking** -> **Routes**. 
![dotnet 02](./images/04/dotnet-02.png)  

* Click on the URL to launch the application.   You will see the application as below.  This application might take a while to deploy. 
![dotnet 03](./images/04/dotnet-03.png)

* Go back to **Console**.   Click on **Builds** -> **ImageStreams**.  This is showing the application image of this .net core application.   You can use to deploy to the next environment. 
![dotnet 04](./images/04/dotnet-04.png) 

* Click on **sampledotnet** and scroll to the bottom.  You will see the image is tagged as latest by default.   In the next exercise,  the image will be tagged to be deploy into the SIT environment.    
![dotnet 05](./images/04/dotnet-05.png)

### Summary

In this exercise,  you have learned to use OC commands to create new project and deploy .net core application into openshift. 

