---
title: "RealTime ProcessFlow Execution"
description: "Get the flavour of realtime processflow execution."
keywords: "trigger, trigger processflow, realtime processflow execution, triggerd integration"
toc: true
tag: developers
category: "Processflow"
menus: 
   quickstartprocessflow:
        title: "Trigger ProcessFlow"
        weight: 6
        icon: fa fa-file-word-o
        identifier: triggerprocessflow
---

Integration depends on the way the application exposes data, which is generally done through APIs, 
where one can communicate with the APIs, to create the list of data in the platform. Hence as an integration platform, 
it occasionally needs to pull data from the application and sync only the data which is modified overtime. 
We have a number of sync strategies to integrate data using `Polling` technique, which as an users/implementors 
you need to follow to identify the latest data to be synced.    

On the other hand, `Webhook` allows the application to generate a call back to the external application 
whenever a new data is updated to the application. Such an integration which is initiated by the application 
itself is called Triggered Integration. To perform the aforesaid integration, you need to need design a trigger 
processflow, which receives the data from outside world and executes various steps in the pipeline.   

This section of the documentation will guide you with the process of Creating & Saving **trigger processflows**. The steps for implementing the same is provided below :

## Prerequisites for Creating Trigger ProcessFlows

1. Should have valid credentials for logging in to the APPSeCONNECT portal.   
2. Applications should be chosen from the apps section, for proceeding with the design of processflows.  
3. Before designing a trigger processflow, you should get familiar with [different trigger types](/processflow/working-with-Start-Node/#working-principle).
4. Should have the basic knowledge of [creating and saving](/getting%20started/create-your-first-processflow/) processflows.   

## Steps to create a Trigger ProcessFlow

1)	Login to the Portal and navigate to the **Designer > ProcessFlow** module. The Process Flow listing page appears.
![Create Basicprocessflow13](/staticfiles/processflow/media/create-basicprocessflow13.png)

2)	By default, **Process Flow** folder is selected, where you can create new processflows as well as you can also view and edit existing processflows.

3)	Click on the new button for creating a new processflow.      
![Create Basicprocessflow2](/staticfiles/processflow/media/create-basicprocessflow2.png)   
**Note : If the Folder is empty, you can view the button Create a Process Flow, that navigates 
you to the processflow Designer Page.** 

4) A pop-up will appear where you need to put the **ProcessFlow name**. Select **Ok**, you will be navigated to the [processflow Designer Page](/processflow/components-of-processflow/) else you can abort the processflow creation by clicking on **Cancel**.        
![Create BasicProcessflow14](/staticfiles/processflow/media/create-basicprocessflow14.png)

5)	Provide a Description for the processflow in the processflow header panel.        
![Create Basicprocessflow15](/staticfiles/processflow/media/create-basicprocessflow15.png)

6) Drag the start node into the canvas. Select the **Trigger Type** as **Event**. 
On selecting the Trigger Type as Event, the following field would appear : Enter Register URL. Provide the details for the field.

Enter Register URL : You will have to provide your Organisation name as the sub-domain that would be merged with the APPseCONNECT Domain.   
![triggerpf1](/staticfiles/processflow/media/triggerpf1.png)

7) Navigate to our [Getting Started](/getting%20started/create-your-first-processflow/) section, to complete the remaining steps of creating a processflow.     
![triggerpf2](/staticfiles/processflow/media/triggerpf2.png)

**Note : In this scenerio, trigger processflow is designed using shopify and SAP Business One as source and destination application respectively.** 

8) Deploy the designed processflow in [OP or Cloud environment](/processflow/deploying-and-executing-processflow/#deploying-processflows-to-environment). 

9) Navigate to **Deploy > Environments**. Click on the ellipsis for the [respective triggger processflow](/deployment/Environment-Management/#on-premise-environment-details-page). Click on ProcessFlow URL and copy the url.  

10) Create a webhook for your choosen source application and assign the ProcessFlow URL to the webhook that 
you have created. As soon as, you create a new data in your source application corrosponding to your choosen endpoint, 
the syncing process will be triggered and the data will be mapped into the destination application. 

**Note :**

- No need to provide any Action Filter in case of Trigger ProcessFlow.  
- You can deploy **Trigger ProcessFlow** both in OP as well as in Cloud Agent.
- The **Execution button** in the processflow designer page will be in disabled mode.  
- If your ProcessFlow triggered is of EVENT Type, the ACTIONS column will have the option of ProcessFlow URL that will display you the Triggered URL of your Organisation.
