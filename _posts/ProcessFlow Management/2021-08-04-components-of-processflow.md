---
title: "Components of ProcessFlow"
toc: true
description: "Components of ProcessFlow Designer to create,design and develop your smart,interactive and free-flowing integration system."
keywords: "Constituent of ProcessFlow, Components of ProcessFlow, Header panel, Left panel, Right panel, Designer view"
tag: developers
category: "Processflow"
menus: 
    processflow:
        title: "Designer of ProcessFlow"
        weight: 4
        icon: fa fa-file-word-o
        identifier: componentsofprocessflow
---

**ProcessFlow** is a visual representation of a business process integration, which helps you as an user to orchestrate a business process in such a way so that you can modularize and control the complexity of business integration properly.

## Various Section of a ProcessFlow 

**ProcessFlow Designer** provides a number of components and services which enables the developers to create and maintain an integration solution for the customers. These are : 

* Applications
* Technology Applications
* Logic Nodes
* Node Suggestion
* Drag/Drop Node Canvas
* Link ordering
* Data Mapper
* Loops
* Variables
* Deployment
* Execution

Each of these components present in ProcessFlow Designer page works in tandem to generate integration solution between source and destination application. 
The components provides specific building block for the integration, each of them are capable of doing specific operation on the platform. *Let us look into a ProcessFlow to understand it better*.

![Components of processflow1](/staticfiles/processflow/media/componentsofprocessflow1.png)

As ProcessFlow gives you an IDE that lets you build an integration that is best suited for your customers while giving you the option to deploy and execute from the same,
here comes the canvas where you can design, deploy and execute all from the single place. The canvas consists of various segements that are marked on which the user needs to work on.

1. **Header panel** - This area provides you knowledge about the name and description of the ProcessFlow, various options to work with the ProcessFlow Designer and allows you to finally save/delete/deploy a ProcessFlow.
2. **Left panel** - This section provides you with a toolbar which is grouped into Application tools, Flow Connect which represents the connectors for technology like REST, SOAP, Database, File System, etc., and the Flow Logic where the nodes representing orchestration are listed.
3. **Designer View** - This is the actual canvas where you shall design your processflows.
4. **Right Panel** - This section lists the ProcessFlow node suggestions and real-time view of the ProcessFlow.


### Header Panel

![componentsofprocessflow header panel](/staticfiles/processflow/media/componentsofprocessflow_header.png)

Here you can provide ***name*** and ***description*** of the processflow which will enable you to identify your respective processflows uniquely. Below the processflow name, you get an option to add description to the ProcessFlow. The field for providing the Description to the processflow is an optional field. You can edit the description any number of times as required.  
**Note : The processflow name will be a mandatory field for designing and saving any processflows.**

Details of the list of executable buttons are given below :

* **Play button** : The Play button will allow you to execute any of your created processflow. Click on the Play button, select **Execute** or [Execute with Runtime filter](/processflow/Runtime-Filter/) to execute your processflows as per your requirement.   
* **Tracker button** : You can view the execution status and messages related to execution process in the Tracker Window. The deployment and execution logs will be displayed in the tracker window.
* **Delete button** : The delete button will allow to delete the selected Nodes and Links from the processflow. You'll get a confirmation pop-up for the delete operation of the processflow. 
* **Zoom in** : You can zoom in the processflows for better viewing purpose.
* **Zoom out** : You can zoom out the processflow for better user experience. Users can also resize the screen accordingly. 
* **Link Order** : You can sequence your execution order of your processflow. On clicking the [Link Order](/processflow/link-order-sequencing/) button, the order sequence window configuration window opens.
* **User Defined Functions** : Here, you can implement multiple User Defined Functions for implementing Definite Tasks within your ProcessFlow. For more details on User Defined Functions, [Click Here](/processflow/Working-with-functions/#user-defined-function).
*  To view the screen in full screen mode, click the Button for Full Screen.
*  You will have the option to adjust the screen resolution to 100%, 50% & 25% & Fit to Screen as per the need.
* **Environment List** : You can see the environments where the Processflow is deployed. You can open the Processflow using the link too.
*  **Save** : The save button allows you to save the following processflow for later use. You can edit the processflows anytime by clicking the edit button available in the [processflow listing page](/processflow/processflow-listing-page/).  
* **Delete** : You can view this button beside the **SAVE** button that will allow you to [delete](/processflow/delete-processflow/) the processflow completely.
* **Deploy** : You can select the type of environment where you want to deploy your processflow.


You can view the **Back to processflow** button that will navigate you to the [listing page](/processflow/processflow-listing-page/).


### Left panel

You can add processflows nodes to the processflow designer panel. The nodes can be dragged and dropped in the design panel for configuring & designing the ProcessFlow. Users can utilize any node based on the business requirement and can view the 
following tabs and menus in the left panel of the page.    

1)	**Search** : You will be able to search any Nodes & Apps related to processflow. You will be filtered with the results based on the alphabets you type.               
2)  **Start** : This node initiates the execution of the processflow.                   
3)	**End** : This node depicts the completion of the processflow.                       
4)	[Mapper](/processflow/working-with-mapper/) : This node allows you to map the fields of source and destination applications used in the processflow.       
5)	[Apps](/processflow/processflow-app/) : You can view two tabs on expanding **Apps** : `Pre-prackaged apps` & `My Apps`. 

 - **Pre-packaged Apps** : You will be able to view all the pre-packaged apps available for your organisation as per the plan. 
 - **My Apps** : You can view all the custom and the technology apps created in your organisation.

***On dragging the applications to the designer panel, the [node configuration window](/processflow/processflow-app/) would appear***.     

6)	**Flow Connect** : You can view **FTP**, **Database**, **REST** connector nodes upon expanding.   
7)	**Flow Logic** : You can view all the process property nodes namely halt, resume etc required to implement the customer business process.  
8)	**Notifications** : Expanding this menu, you can view all the nodes for implementing actions within a processflow.  


### Designer View 

![componentsofprocessflow designer panel](/staticfiles/processflow/media/componentsofprocessflow_designer.png)

You can design/create the processflow here. Drag and drop the required nodes to the 
designer panel for creating the processflow. Expanding the menu in the left panel, 
you can view all the node that can applied for designing the processflow.


### Right Panel

The right panel of the processflow Designer Page will have the following sections :  

![componentsofprocessflow right panel](/staticfiles/processflow/media/componentsofprocessflow_rightpanel.png)

* **Suggested Node** : Here you'll get suggestions of providing nodes that can be applied with the node dragged in the processflow designer panel.
* **Real Time View** : Here you would display the real-time view of the processflow.

