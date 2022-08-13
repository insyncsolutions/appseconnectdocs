---
title: "Overview of Deployment"
description: "Deploy your integration ProcessFlows in the location of your choice in a public or private cloud or on-premise or behind the firewall. Schedule sync at an interval or keep it manual as per your need."
keywords: "Overview of deployment, deployment, getting started of deployment, System Requirement for Agent Installation, system requirement"
toc: true
tag: developers
category: "Deployment"
redirect_from: 
     - /deployment/overview/
menus: 
    header:
        weight: 4
        title: "Deployment"
        icon: fa fa-wpexplorer
        identifier: deployment               
---

The APPSeCONNECT Platform either for Cloud or On-Premise integration is a fully integrated solution that enables 
organizations to design, develop, deploy, manage - connectivity apps, APIs and microservices within 
the infrastructure provided and supported. Deployment involves `set of procedures where you move your processes and deployable components` 
into a runtime environment. The Deployment section of this document lets you manage active deployments 
and create new deployments. A deployment consists of some packages that has been deployed to a specified environment. 
This section will provide you with the information of deploying processesflows, its pre-requisites and various components needed to deploy to a particular environment for APPSeCONNECT.

|Sections|Details|
|---|---|
|[System Requirement for Agent Installation, URL & Port Info](/deployment/overview-deployment/#system-requirement-for-agent-installation)| Before the agent setup and installation, you need to know the requirements. This document will list with system requirements for Agent Installation and URL & Port Infos.|
|[Installing & setting up of Agents ](/deployment/Deployment-Configuration/)| This section of the document will help you with the installations of both the Cloud and On-Premise Agent.| |
|[Working with Environments](/deployment/Environment-Management/)| This document will help with the `Environment details page` of portal. Once you have installed your agent, you can view this image in the enviroment section of the portal.| 
|[Detaching and Attaching of Agents](/deployment/Environment-Management/#detaching-and-attaching-environment)| This document will help you with the detaching and attaching events for your Agents in the Environments page.|
|[Settings in Agent](/deployment/settings/)|This document helps you with the settings page of the On-Premise Agent.|
|[Transactional Stores](/deployment/Overview-of-Plugin/)|This document will help you with the Plugins of APPSeCONNECT.|
|[Updating & Migrating an Agent](/deployment/upgradation-and-migration/)| This document will help you with the Upgradation and Migration of the On-Premise Agents.  |


##  System Requirement for Agent Installation   

APPSeCONNECT Agent is a tool that is installed on-premise and does the actual sync, 
so to get the highest performance on your sync operation, you should have a good hardware, best connectivity 
and network speed. Prefer using `local IP to connect to your application` if the app is accessible using LAN to 
improve performance, but with a high-speed network, APPSeCONNECT also performs great with remotely. 

Here is a list of minimum requirement for APPSeCONNECT to run : 

* 2 GHz Processor or faster 32-bit (x86) or 64-bit (x64)
* 4 GB RAM 
* At least 1 GB of Hard disk space in system drive.
* Windows Vista SP 2 and above or Windows Server 2008 SP 2 and above.
* Updated graphics drivers (Always best for performance)
* .NET Framework 4.6.1 or above
* Internet connectivity to get configurations and activation of the agent.
* Administrative user.
* Internet browser to access our cloud portal (https://portal.appseconnect.com/Account/Login?ReturnUrl=%2f#!)
* Dedicated bandwidth of 1 Mbps.

- For best performance, our Agent will require admin rights so that it can install our agent and can have universal access 
to all the required folders. 

- APPSeCONNECT also installs a background agent which will be installed in Local System account 
and would access the local application data folder to store cache and log files. 

Please ensure local system account have proper privilege to access "Installation directory".

To run APPSeCONNECT, you need to make sure of few things :
You should whitelist the following URLs from Network Firewall settings :

- https://admin.appseconnect.com
- https://cloud.appseconnect.com
- https://appsdrive.blob.core.windows.net/
- https://services.appseconnet.com/


`APPSeCONNECT Components` for deployment includes the following items :

* AGENT
* ADAPTER
* PLUGINS
* ADDONS
* EXTENSIONS

1) **AGENT** - APPSeCONNECT Agent is a special tool that can be downloaded on your own server and does the actual data 
synchronization with on-premise application with the help of Adapters.The Agent is a background service which runs 
as per your configuration running on schedule, either automatically or manually, and syncing data between applications. 
The Agent is capable of responding to any configurational changes and can retain that application configuration until 
the next change. 

2) **ADAPTER** - Adapter represents an interface between an APPLICATION and APPSeCONNECT. 
An adapter is one of the intregal component which connects your app with APPSeCONNECT. 
There are few responsibilities of an adapter which are defined as under : 

 * Create a credential view which allows connecting to the respective APP where you want to connect.
 * Create Push and Pull method inside the adapter which can send and receive data to and from the application.
 * Add additional business behavior with respect to the corresponding app.

The Adapter is loaded dynamically by the Agent and calls some specific methods using a fixed contract defined as an interface. 

3) **PLUGINS** - Plugin for AEC Database of Agent to support any DBMS at client side/client-server such that AEC can support 
databases like MYSQL,HANA,OLE-DB, Oracle, etc. for keeping a log and other transaction details. 

4) **ADD ONS** - AEC Add-on extends the functionality of a certain program but they are usually meant to function on a certain program. 

5) **EXTENSIONS** - APPSeCONNECT extension is something that is specific to the browser, and they are a bit different on 
each browser but tend to be able to learn more about the overall state of the browser, they may be automatically 
added to pages accessible separately from a page, etc.


