### Introduction

Red Hat CodeReady Workspaces uses Kubernetes and containers to provide any member of the development or IT team with a consistent, security-focused, and zero-configuration development environment. The user experience is as fast and familiar as an integrated development environment (IDE) on a laptop. CodeReady Workspaces encodes development projects as code that is checked into the Git repository and exposed via a Uniform Resource Locator (URL) or command-line interface (CLI) command. It creates all the containers needed to run the project, clones the sources where needed, and adds development tools (such as debuggers, language servers, unit test tools, and build tools) as sidecar containers so that the running application container continually mirrors production. Users can employ the included browser-based IDE if they do not have an IDE already set up, or they can opt for a local IDE.

In this workshop,  we have deployed CodeReady Workspace in Openshift Cluster for attendees to experience how easy to develop services and deploy it into openshift cluster. 

### Create a spring boot application. 

* Open a new browser tab with the url as [CodeReady Workspace](https://codeready-openshift-workspaces.apps.cluster-19dc.19dc.sandbox811.opentlc.com).  Login as `%username%` and password as `openshift`.

* Click on [Allow selected permissions].
![CodeReady Workspace 12](./images/02/crw-12.png)

* Key in your email address, first name and last name.  Click on [Submit].
![CodeReady Workspace 01](./images/02/crw-01.png)

* Click on Java Spring Boot as hightlighted in red box below.  This might take a few minutes.   This will auto-create a `Hello World` service with Spring Boot.  
![CodeReady Workspace 02](./images/02/crw-02.png)

* If you are interested to see the code, you can navigate to src/main/java/dev/snowdrop/service/GreetingEndpoint.java 
![CodeReady Workspace 03](./images/02/crw-03.png)

* CodeReady Workspace provides scripts by default to build / run / deploy spring boot application to openshift.   Click on the box icon on the right.  Click on `Build` to build the application.  This might take a few minutes.
![CodeReady Workspace 04](./images/02/crw-04.png)

* `Build Successful` will be showed in the Terminal if successful.   If you encounter error,  please check with the instructor or lab assistant.
![CodeReady Workspace 05](./images/02/crw-05.png)

* Click on 'Run' to run the application.  Click on [Open in Preview].  
![CodeReady Workspace 06](./images/02/crw-06.png)

* You will see the spring boot application open in preview pane. Click on [Invoke] button.  You will see the result as `{"content":"Hello, World!"}`.   
![CodeReady Workspace 07](./images/02/crw-07.png)

* The application is working fine.  Next step is to deploy the application into openshift.   Click on the box icon on the right.  Click on `New Terminal`.  Type **oc login `https://api.cluster-19dc.19dc.sandbox811.opentlc.com:6443` -u `%username%` -p `openshift`** and `Y` when prompt. 
![CodeReady Workspace 08](./images/02/crw-08.png)

* Type `oc new-project %username%-project` to create new project to deploy application. 
![CodeReady Workspace 09](./images/02/crw-09.png)

* Click on `Deploy to Openshift`.   
![CodeReady Workspace 10](./images/02/crw-10.png)

* After it is successful, click on **console**.  You will see the application deployed successfully into `%username%-project` project. Please wait till the circle turned dark blue as shown below.  Click on the icon on top right corner to access the application.                   
![CodeReady Workspace 11](./images/02/crw-11.png)

### Summary
In this exercise, you have learned to build a simple spring boot application using CodeReady Workspace and deploy into Openshift. 



