---
title: "RealTime ProcessFlow Execution"
description: "The Sequential Node Ordering enables you to manage the execution sequence of multiple flows within a processflow such that you do not have to unlink the nodes everytime to sequence the flows."
keywords: "Link order sequencing, ordering of nodes, sequential execution,  sequential node ordering"
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

This section of the documentation will guide you with the process of Creating & Saving **trigger processflows**. The steps for implementing the same is provided below :

## Prerequisites for Creating Trigger ProcessFlows

1. Should have valid credentials for logging in to the APPSeCONNECT portal.   
2. Applications should be chosen from the apps section, for proceeding with the design of processflows.  
3. Before designing a trigger processflow, you should get familiar with [different trigger types](/processflow/working-with-Start-Node/#working-principle).
4. Should have the basic knowledge of [creating and saving](/getting%20started/create-your-first-processflow/) processflows.   

## Steps to create a ProcessFlow

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

7.
