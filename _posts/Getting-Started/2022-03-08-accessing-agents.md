---
title: "Agent"
toc: false
tag: developers
category: "Getting Started"
menus: 
    gettingstarted:
        title: "Agent"
        weight: 8
        icon: fa fa-wpexplorer
        identifier: accessingportal
---

**APPSeCONNECT** is an iPaaS which lets developer or citizen integrator to build integration solution such that the data could be seamlessly transferred through it. 
It acts as middleware between enterprise applications which transfers data from one business application and updates the same to their respective applications through the aid of agent. 
APPSeCONNECT Agent is a lightweight dynamic runtime engine that can be downloaded on your own server locally or as cloud hosted one and does the actual data synchronization with On-Premise application as well as Cloud hosted applications with the help of adapters. 
The Agent is a background service which runs as per your configuration running on schedule, either automatically or manually, and syncing data between applications. 
The Agent is capable of responding to any configurational changes and can retain that application configuration until the next change. 

APPSeCONNECT supports following kinds of integration modes for data synchronization between various business applications.

**1. On-Premise to On-Premise Integration.**
**2. On-Premise to Cloud Integration.**
**3. Cloud to Cloud Integration.**

To perform data synchronization,you can either use our cloud agent or can install the agent in your local server depending on the applications between which you want to sync data. 
You can download,install and configure the agent locally as well as enable the cloud agent from [here](/deployment/Deployment-Configuration/). 

1. In case of **On-Premise** to **On-Premise** connectivity, the APPSeCONNECT requires an agent dwonloaded on the same network where the application resides. 
The beauty of this On-Premise agent of **APPSeCONNECT** is that the sensitive information like URLs,passwords,application credentials etc. are never getting transfered to our cloud servers.They remain 
secured in there own network where the agent dwonloads the logic and the scripts from cloud portal and executes the integration. 

![agent1](/staticfiles/root/media/agent1.png)
    
In the figure it shows,there is an agent gets dwonloaded in a secure network which is fire-walled from external world. The agent dwonloads all the scripts required,executes them On-Premise and locally calls 
the business applications whenever required. The schedule information is also dwonloaded from server but the actual scheduler which executes the integration happens within the premise. 
 
2. In case of **On-Premise** to **Cloud** connectivity, the applications connects through publicly available APIs. Here main mode of execution happens in your local network using your own resources while the configuration are done in cloud itself. A well-defined 
API dwonloads the configuration in the agent which is capable to schedule and call the application or integrations points. In this case, it is to be noted,that the resources which are used to integrate data in application 
are done through locally installed agent. 

3. In case of **Cloud** to **Cloud** connectivity, going to full cloud solution APPSeCONNECT provides a hosted cloud environment too which is a micro-service oriented cloud engine, where the cloud scheduler can request to execute. 
The cloud engine is capable of handling huge number of request where each of these microservices is also capable of doing the job and they are inter-connected to produce the actual result. Our cloud engine is 
also IP based fire-walled that means cloud environment can only be accessed through our services only and no external user can access it directly. The micro-service uses the credentials defined in the platform 
to communicate with the application through publicly availbale URL. 

![agent3](/staticfiles/root/media/agent3.png)
