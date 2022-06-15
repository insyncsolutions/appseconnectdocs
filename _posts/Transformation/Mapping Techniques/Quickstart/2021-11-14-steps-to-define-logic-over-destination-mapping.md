---
title: "Steps to Define logic over Destination Mapping"
toc: true
description: "Get to know, how you can if- else mapping during transformation."
keywords: "Mapping Levels, Mapping at Attribute Level, Mapping at Loop Level, Mapping at Complex Object Level, Mapping at Complex Object Collection  Level, Respect Hierarchical Rendering on Mapping state"
tag: developers
category: "Transformation"
menus: 
    transformationbasic:
        title: "Steps to Define logic over Destination Mapping"
        weight: 4
        icon: fa fa-file-word-o
        identifier: definelogicdestinationmapping
---

Mapping in `APPSeCONNECT` is done so that a Source Application can communicate with the Destination Application efficiently and effectively. 
Since business applications differ from one another in terms of their strcutures and `APIs`, mapping provides you a logical interface 
to synchronize data in a smooth and free-flowing way. This document will talk about `if-else` logic, mapping process and its implementation in different levels. 

## Pre-requisites

* Login to the APPSeCONNECT Portal with valid credentials.  
* Navigate to the [Process Flow Section](/processflow/overview-of-processflow/). Here You can view the [Process Flow Listing Page](/processflow/processflow-listing-page/).  
* [Create a New Process Flow](/getting%20started/create-your-first-processflow/) or Edit an existing Process Flow for defining logic over 
detination mapping. 

## Mapping Levels

Mapping is done at various levels depending on the input data packet. [Refer here](/transformation/basic-of-source-destination-mapping/#source-destination-mapping) to grab the basic knowledge of mapping. 

### Mapping at Attribute Level

Click on the mapper node to define mapping at various level.The mapper node expands and the transformation window appear. 
The user/implementer can use `If-Else Mapping` in the attribute level by providing the conditions as mentioned below. 

You can add condition and attributes from the drop-down option for which the If-Else mapping will work.

![Attributelevel-AddCondition](/staticfiles/Transformation/media/Attributelevel-AddCondition.png)

**Note : The user can add conditions (Else-If & Else) inside an IF Node, except for the FOR-EACH LOOP LEVEL.**

*The above mapping scenario is explained below*

The Condition `default-address/country-code='US'` in the IF Node describes that if the Country Code in the default address is US, the clause Country_Region_Code=HU is carried out.

The Condition `default-address/country-code='IN'` in the Else-If node describes that if the Country code in the Default Address is IN, the clause Country_Region_Code = GB is carried out.

Refer the screen given below :
![Logicover Destinationmapping3](../../staticfiles/processflow/media/mapper/logicover-destinationmapping3.PNG)

The User can also add Else-If and Else(Otherwise) and its clauses in the attribute Level. The following screen shows the Condition add for If-Else.  
![Logicover Destinationmapping4](../../staticfiles/processflow/media/mapper/logicover-destinationmapping4.PNG)

### Mapping at Loop Level

You can only provide `IF Mapping` at For-Each Loop level. Below is an example which shows the **If Mapping** at Loop Level.  

![Logicover Destinationmapping5](../../staticfiles/processflow/media/mapper/logicover-destinationmapping5.PNG)

>In the For-Each Loop Level, only IF is used as this level for removing duplicate check and also removes junk data, for integration process. 

### Mapping at Complex Object Level

The user/implementer can work on the If-Else Mapping in the complex object level. 
You can perform `If-Else Mapping` at the complex object level following the below mentioned images.  

![ComplexObject-Mapping](/staticfiles/Transformation/media/ComplexObject-Mapping.png)

Like other levels, the user can add Else-If and Otherwise and its conditions from the drop down. 

### Mapping at Complex Object Collection  Level

The `If-Else Mapping` can be done at the ComplexObjectCollection Level. You can use if-else mapping level at this level by following the given example. 

![ComplexObjectCollection-If-Mapping](/staticfiles/Transformation/media/ComplexObjectCollection-If-Mapping.png)  
![ComplexObjectCollection-else-Mapping](/staticfiles/Transformation/media/ComplexObjectCollection-else-Mapping.png)

## Respect Hierarchical Rendering on Mapping state

On disabling the mapping of the parent node, it disables all the child node such that when the XML is rendered, 
only the enabled node will be rendered in the XML. This feature will help the user to implement
the hierarchical rendering feature in the APPSeCONNECT Portal.

**Pre-requisites**

Mapping should be done in the parent node for accessing the Enable/Disable feature. 

**Steps to implement hierarchical rendering on mapping** 

1.	Login to APPSeCONNECT Portal. 
2.	Navigate to the processflow listing page to create or edit an existing processflow. 
3.	Click on the Mappernode and the transform section opens up.
4.  On `expanding the schema object`, all the `complex objects and the complex objects collection` are displayed.
   ![Hierarchial Rendering Processflow](../../staticfiles/processflow/media/mapper/hierarchial-rendering-processflow.PNG)

5.	Hover the icon over the mapped complex object/complex object collection. The Disable option will appear. 
    ![hierarchial-rendering2](/staticfiles/Transformation/media/hierarchial-rendering2.png)    

8.	Click the Disable option, the complex object/complex object collection and its child, sub-child, 
    all the nodes get disabled, present under it.
    ![hierarchial-rendering3](/staticfiles/Transformation/media/hierarchial-rendering3.png) 
    ![hierarchial-rendering4](/staticfiles/Transformation/media/hierarchial-rendering4.png)
**Note : The ROW Node remains white even on disabling. Its colour will only change if the row node is also mapped.**
![hierarchial-rendering5](/staticfiles/Transformation/media/hierarchial-rendering5.png) 

9. Now, if a child node is enabled from the list of disabled nodes, the child gets enabled, also its immediate parent gets enabled.
    ![hierarchial-rendering5](/staticfiles/Transformation/media/hierarchial-rendering6.png) 
Now if the immediate parent is also associated with a parent (a complex object/complex object collection), it also gets 
enabled, rest all other child nodes on that tree, remains disabled. 

**Protip:** The Disabled node turns grey on disabling.
{: .notice--info} 
