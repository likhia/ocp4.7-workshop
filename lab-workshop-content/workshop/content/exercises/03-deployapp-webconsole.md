### Introduction

There are different ways to deploy workloads to an openshift cluster. Here we will explore deploying a simple web application using OpenShift developer console.

What happens when we deploy an application?

OpenShift creates a bunch of objects when you deploy an application. Some key objects:

* **Build Configuration**: If you are starting with source code or a dockerfile, the build configuration shows you where the source code is and the strategy to build the application, parameters to be passed to your build and more. You can explore and edit openshift build configuration YAML using web console, if you desire to change it. Each time you start a build, it runs a pod inside which the application build happens. The result of the build is typically a container image that gets saved in a container registry (integrated registry on your openshift cluster by default)
* **Deployment** or **Deployment Configuration**: DeploymentConfig is an openshift concept that predates kubernetes deployment. You can use either of these. These are the configurations for how your application is deployed, the environment variables to be passed to our container, external configurations to be passed via configmaps, storage mounts etc. This defines the configuration for your running application. OpenShift runs a deployment pod that executes deployment and once your application pod stands up, the deployment pod completes.
* **Service** Kubernetes service frontends a set of pods and proxies traffic to your application pods. 
* **Route** OpenShift route is ingress to your application. Creation of route object results in a URL being added to the OpenShift router which becomes an entry point for your application from outside the cluster.

In addition to the above, it may creates Secrets, ConfigMaps, ServiceAccounts and other objects too.

When you explore a deployed application, make sure you look at the corresponding YAMLs for each of these objects.

### Deploy an application

* Click on the **Console** tab. Make sure the project selected is `%username%-project.

* From the menu, click on `+Add` and choose `Container Image` option
![dev console app 01](./images/03/deployImage-01.png)

* Key in `docker.io/likhia/quarkus` as image name.  It will takes a few seconds to validate the image. Leave everything as default.  Click on [Create]. 
![dev console app 02](./images/03/deployImage-02.png)

* You will navigate back to Topology page and another deployment named Quarkus is added.  Click on it to view its details on the right.  I will cover the monitoring and logging of application in last exercise. 
![dev console app 03](./images/03/deployImage-03.png)

* Please wait till the circle turned dark blue. Click on the icon on the top right corner.  It will open a browser tab.  Add `/demo` to the URL.  You will see a simple `Hello World`.
![dev console app 04](./images/03/deployImage-04.png) 

### Summary
In this exercise, you have learned to deploy the existing application image into openshift. 
 
