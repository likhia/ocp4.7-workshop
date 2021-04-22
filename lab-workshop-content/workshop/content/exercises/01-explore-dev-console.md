### Introduction

OpenShift 4.x provides a Developer Web Console for anyone trying to deploy and manage applications to the cluster. This GUI is different from Administration Console that is typically used by cluster administrators. Developer Web Console employed by application developers and deployers, application operations, or anyone with an application focus.

### Explore

* Click on the **console** tab. This is the OpenShift Container Platform web console where developers can visualize, browse, and manage the contents of project.  Notice your `username` on the right top corner.    

* You can now toggle to 'Developer' view by pressing on the `Administrator` dropdown and selecting `Developer`. In this exercise,  we will focus on Developer view that allows developers to perform the following: 
   
  * Create and deploy applications on OpenShift Container Platform by importing existing codebases, images, and dockerfiles.

  * Visually interact with applications, components, and services associated with them within a project and monitor their deployment and build status.

  * Group components within an application and connect the components within and across applications.

* Take your time and explore menu options.

  * **+Add** allows developer to deploy workloads using different ways. 
    ![Dev Console 01](./images/01/devconsole-01.png)  

  * **Topology** shows the applications deployed. For now, it is showing the same as +Add as there is no application deployed.  You will see the deployed application in topology in the exercise later.

  * **Monitoring** provides options to monitor your project or application metrics, such as CPU, memory, and bandwidth usage, and network related information.  Please note that there are some error messages as there are issues to access this monitoring from this console.  In the last exercise,  you will be guided to access the openshift console directly.  

  * **Search** allows you to search for all the artifacts in this project.
 
  * **Builds** shows the OpenShift build configurations. Once a build configuration created, you can execute, view, and edit build configuration and view build logs.

  * **Helm** allows deployment of applications and services to Openshift Cluster via Helm Chart.
    
  * **Projects** shows all the projects created by the login user.

  * **ConfigMaps** shows the list of configMaps that are used in the current project. 

  * **Secrets** shows the list of secrets that are used in the current project.   

### Summary
In this exercise, we logged into the cluster using Web Console and understood the layout and navigation of Developer console which is typically used by the application teams (developers, deployers, and builders)


