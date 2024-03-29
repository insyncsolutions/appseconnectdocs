---
title: "Runtime Filter"
description: "Get the flavour of fetching and posting data to your business applications for specific scenarios using our runtime filter."
keywords: "Runtime filter, dynamic runtime filter"
toc: true
tag: developers
category: "Processflow"
redirect_from: 
     - /processflow/User-Defined-Dynamic-Filter/
menus: 
    deployment:
        title: "Runtime Filter"
        weight: 4
        icon: fa fa-file-word-o
        identifier: customfilterprocessflow
---

Using ProcessFlows, you can now implement Runtime filters on processflows that will allow you to fetch and post data to and fro applications 
that are required only for specific scenarios. With this feature, you can not only implement the generic filter but also a custom filter. On execution, you get the option to execute either with the generic filter or with the custom filter depending on your choice. 
Below are the process that would help you implement Dynamic Runtime Filter on your organisation.

## Prerequisites

- You should have a valid APPSeCONNECT Account.
- You should have a processflow designed with proper configurations on the [APP Nodes](/processflow/processflow-app/).
- Your designed processflow should be deployed successfully.

## Implementing Dynamic Runtime Filter

1) Navigate to the [Designer Page](/processflow/components-of-processflow/) of ProcessFlow.

2) Once you have [designed your Processflow](/getting%20started/create-your-first-processflow/), deploy the processflow. You'll get the Deployment steps on the Tracker Window.

3) Clicking on the Play button, you'll get the following two options in the drop-down.

- **Execute** - This option allows you to execute with the filter (generic filter) provided in the App Node.
- **Execute with Runtime filter** - This option will allow you to perform execution with a Runtime filter apart from the generic filter.

Select the option **Execute with Runtime Filter**.

![customfilter2](/staticfiles/processflow/media/runtimefilter2.png)

4) The Runtime filter Window opens that will allow you to provide the filter as per your need.

![customfilter3](/staticfiles/processflow/media/runtimefilter3.png)


**Note:**

- By Default, the Runtime filter will display the Action Filter used normally in the GET node. However, once edited and saved, you will not have to work on the same from the 2nd instances.  
- Changes made in the normal Action Filter will not impact that in the Runtime filter.

## Creating Dynamic Runtime Filter

This part of the document will allow you to create Runtime Filter on GET node for specific scenario execution. You can create these filters from TWO different areas.

- Create from **Execute with Runtime filter**
- Create from **Node Configuration - Configure Filter**

### Create From : Execute with Runtime Filter

1) Landing on the **Runtime filter Window**, you will be listed with all the GET nodes of that ProcessFlow. To **ADD** the filter click on the Ellipses -> Context Menu -> Create.

2) You can also add conditions and conjuctions over the filters by clicking on the Ellipses over the HEADER and the BODY section.

![customfilter4](/staticfiles/processflow/media/customfilter4.PNG)

3) You can either click on the **Cancel** button or directly execute the process by clicking on the **Execute**  button. You can track the Execution details on the Tracker Window.

4) You will be generated with [snapshots](/processflow/snapshot-processflow/) for every execution with the Runtime Filter. For every executions with Runtime Filter, snapshots be specifically indicated with a **`TAG`** icon.

![Customfiltersnapshottag](/staticfiles/processflow/media/customfilter5.png)


**Note:**

- You will not get the option of `Execute with Runtime Filter`, if your processflow is not deployed.
- Clicking on the Execute button in Runtime Filter window, will not SAVE the filter.

### Create From : Node Configuration - Configure Filter

1) Click on the Node Configuration button for the GET Node. You get the Node Configuration window. Click on the **Configure Filter** button to get the Action Filter window.

![customfilter10](/staticfiles/processflow/media/customfilter10.PNG)

2) Expand the nodes to view the **Runtime Filter** option. Click on the Ellipses to view the **CREATE** option.

![customfilter11](/staticfiles/processflow/media/customfilter11.PNG)

3) Clicking on the CREATE button, you get the window for providing the filter. Input the filter as required and click on the **Save** button.

4) The **Saved** filters will also be available in the **Execute with Runtime filter**. The process to add and create the filter is same as that performed in Execute with Custom Action filter.

For more details on this section, [ClicK Here](/connectors/configurations/#understanding-actions).


**Note :**

- By Default, the Runtime filter will display the [Action Filter](/processflow/manage-actions-actionfilters-errorfilters/) used normally in the GET node. However, once edited and saved, you will not have to work on the same from the 2nd instances.  
- Changes made in the normal Action Filter will not impact that in the Runtime filter.



## Deleting Runtime Action Filter

1) To Delete a Runtime Filter, Navigate to the **Runtime filter Window** by clicking on the **Execute with Runtime filter**, the window opens.

2) Click on the ellipses of the GET node, whose filter you would like to delete.

![customfilter8](/staticfiles/processflow/media/customfilter8.PNG)

3) You will get a confirmation message for proceeding with the delete process. Click on the `YES` button to proceed with the deletion process, otherwise click on `NO`.

![customfilter9](/staticfiles/processflow/media/customfilter9.PNG)

4) You can also delete the filter from the normal action filter UI. [Click Here](/connectors/configurations/) for more details.


**Note :**

- You may delete filters anytime from both the interfaces of Runtime Filter.
- For every operation you perform with Runtime Filter - Create, Edit, Delete & Execute, you will be updated with its operation on your [FEEDS](/accessing%20portal/accessing-portal/#feeds) section.
- You need to keep your Processflow deployed, to Execute with Runtime filter.
- While the Runtime Filter is on its Execution process, the Autosync remains PAUSED until it is completed. Any operation scheduled during that time will be paused and will be resumes immediately, once its over.