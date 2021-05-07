### Introduction

Developer need to monitor the application deployed and access the logs for investigating issues.   You will learn how to monitor and access log for your deployed application. 

### Monitor your application an accessing logs 

* Please open another brower tab for [Openshift Console](https://console-openshift-console.apps.cluster-19dc.19dc.sandbox811.opentlc.com).  Login as `%username%` and password as `openshift`.

* Switch to `Developer` mode.  Select `%username%-dev` project.  You see the applications that you have deployed in exercise 4.  

* Click on `sampledotnet`.  Click on the `Details` tab. You will see the details of this deployment.  
![Monitoring 02](./images/07/monitor-02.png)

* Click on `samepledotnet`.  Click on the `Resources` tab.  You will see the pod / the build / service and route for this deployment.    
![Monitoring 01](./images/07/monitor-01.png)

* Click on `View logs` of the pod. This is where you can view the logs of the application.
![Monitoring 03](./images/07/monitor-03.png)

* Click on 'Details' tab to view the Memory usage, CPU usage, Filesystem, Network In, Network out and other details about the pod running the application. 
![Monitoring 04](./images/07/monitor-04.png)

* Click on **Monitoring** on the left. Click on `Dashboard` tab.  You will see graphs depicting the CPU, memory, and bandwidth consumption and network related information.
![Monitoring 05](./images/07/monitor-05.png)

* Click on `Metric` tab.  Select `CPU usage` from dropdown list.  Click on `Show PromQL`. You will see the CPU utilization for this application and also the Prometheus query for this chart.  
![Monitoring 06](./images/07/monitor-06.png)

* Please refer to https://docs.openshift.com/container-platform/4.7/applications/odc-monitoring-project-and-application-metrics-using-developer-perspective.html#odc-monitoring-your-project-metrics_monitoring-project-and-application-metrics-using-developer-perspective for more details. 

### Summary
In this exercise,  you have learned how to monitor application and also access the logs of your application. 
