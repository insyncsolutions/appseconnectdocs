---
title: "Deleting Processflow"
toc: true
tag: developers
category: "Processflow"
menus: 
    quickstartprocessflow:
        title: "Delete Processflow"
        weight: 8
        icon: fa fa-file-word-o
        identifier: deleteprocessflow
---

APPSeCONNECT processflows suite features an extensive interface that provide the ability to easily create digital maps to make out robust processflows. 
The drag-and-drop interface is easy to use by any citizen integrator. With the aid of processflow feature, users can now graphically organize, create and view the data flow of a process thereby enabling customers to design integration anytime and anywhere with the help of our cloud portal.
In addition to the above functionalities, APPSeCONNECT provides deleting option which will allow you to delete a processflow once you have designed it,
[deployed](/processflow/deploying-and-executing-processfloww/) it or executed it. Deletion is an easy process for the user and this 
button is available in the [designer section](/processflow/processflow-listing-page/) of the portal.

## Prerequisites

1.	Should have valid credentials for logging in to the APPSeCONNECT portal.
2.	A processflow needs to be designed prior to using this functionality .

## Steps to Delete processflow

1. Login to the Portal and navigate to processflow module. The [processflow home](/processflow/processflow-listing-page/) page appears. Click the **New** button in the home page and the [designer](/processflow/components-of-processflow/) section appears.    
2. [Create](/processflow/creating-processflow/) a processflow. Once you have created the processflow, click `SAVE` button available on the header panel. The created processflows will be available in the processflow home page also. 
![pfdelete2](\staticfiles\processflow\media\pfdelete2.png) 

**Note : When a user is creating a new processflow for the first time, only `SAVE` button will be available.** 

2.1. You can delete a processflow just after saving by clicking on the `Delete` button available beside the **Save** button. A pop up will appear to run the process of deletion as shown below. Click `Yes` to proceed and `No` to Cancel the deletion process.    
![pfdelete3](\staticfiles\processflow\media\pfdelete3.png)  

3. If you wish to [deploy](/processflow/deploying-and-executing-processfloww/) the processflow in any environment you can proceed with the 
deployment option. Once the processflow is deployed, if you try deleting the processflow without undeploying it, you get the 
following message.   
![pfdelete4](\staticfiles\processflow\media\pfdelete4.png)  
4. To finally `Delete` a deployed processflow, go to the[Environment](/deployment/Environment-Management/) section to [Undeploy](/processflow/deploying-and-executing-processfloww/#undeploy-process-flow-from-environment) 
the processflow from the environment.      
![pfdelete5](\staticfiles\processflow\media\pfdelete5.png)    
5. Now come back in the designer section, to carry on the process of deletion of processflow. On clicking on the `DELETE` option, a confirmation message will be displayed. Click `Yes` to proceed and `No` to Cancel the deletion process.                  

The above steps will aid the deletion of processflow and user will be redirected to the processflow [Home page](/processflow/processflow-listing-page/) after successful deletion.   

- Users also get the option to delete a process from **ProcessFlow Home** page. If the processflow is deployed in an environment, you will be unable to perform the 
delete operation as shown below.  
![pfdelete9](\staticfiles\processflow\media\pfdelete9.png)    

- Undeployed Processflows can be deleted from **ProcessFlow Home** page by clicking on the delete button as shown below.  
![pfdelete10](\staticfiles\processflow\media\pfdelete10.png)    

**Note : The deleted processflows moves to the trash folder**.

