---
title: "Basics of Source-Destination Mapping"
toc: true
description: "Get to know about the different mapping techniques and its functionalities "
keywords: "Source-Destination Mapping"
tag: developers
category: "Transformation"
menus: 
    transformation:
        title: "Quickstart"
        weight: 2
        icon: fa fa-file-word-o
        identifier: transformationbasic
---

Mapping triggers the transformation process between the Source and the Destination Applications. 
Source and Destination schemas are mapped in the Transformation section of the processflow. 
This document will help you to know about the Source-Destination Mapping in APPSeCONNECT portal.

## Pre-requisites for Source and Destination Mapping

1.	Valid credentials for logging into the APPSeCONNECT Portal.
2.	[Choose APP](/getting%20started/configurations/#process-of-choosing-app) or [Create APP](/getting%20started/configurations/#create-application)
3.	[Create Connection template](/getting%20started/configurations-for-integration/#configuring-connector-while-creating-connection) 
The pathway for source-destination mapping section is provided [here](/transformation/overview/).

## Source-Destination Mapping

Mapping of the attributes of destination application with source application attributes is implemented by the process known as 
Source-Destination mapping.  
![sourcedestination-mapping](/staticfiles/Transformation/media/sourcedestination_mapping.png)
Mapping Processes are initiated at various level of Input Packets
1.	**For-Each loop** - This is used for execution on a block of code on each element in a collection of items. 
It is useful to display each item in a collection of items till when the loop is defined.
Under For-Each loop, Entities have been used and Variables are set under Entities.
2.	**Complex Object Collection** - This specify the mapping list within a complex object. This mainly includes the collection of complex object and attributes. 
3.	**Complex Object** - Complex Objects are the objects which are highly structured and large in size (can also be small) of Variable Representation Length (VLR).
4.	**Attributes** - Each target system configuration constructs an "attribute map" which contains all the attributes known by the system. 

Variables are defined by two types of scopes. 

1. **Root Variable** - Global variable which can used in any entity.
2. **Root Entity Variable** - This is a local variable which is generally used under the scope of an entity.

## Steps to Perform the Source-Destination (Attribute) Mapping

1. Log in with valid credentials in the AEC portal.
2. Navigate to **Designer -> ProcessFlow**. [Create](/getting%20started/create-your-first-processflow/) or open a pre-built processsflow by clicking on edit.  
![transformation_1](/staticfiles/Transformation/media/transformation_1.png)
3. Click on the Node Configuration icon of Mapper node. The transformation page opens up. Here you can perform your necessary mappings.  
![transformation_2](/staticfiles/Transformation/media/transformation_2.png)
4. Expand the For-Each Loop node for mapping the attributes. Click on the **Do Mapping** button provided beside every attribute.  
![transformation_3](/staticfiles/Transformation/media/transformation_3.png)
5. The Mapping window opens up. You need to provide the fields for mapping is this window. 
   The User can also click on the entities/attributes to get it on the box.  
![transformation_4](/staticfiles/Transformation/media/transformation_4.png)

6. Click on the Save button after the mapping is done in that attribute. Similarly other attributes can also be mapped. 

**Points to Remember**

- You can also perform [Variable mapping](/transformation/defining-variables-in-processflow-mapping/) and [Lookup mapping](/deployment/implementing-lookup-in-mapping/#prerequisites-for-mapping-lookups).

- The user can enable and disable the attribute mappings. The `Disabling Mapping` feature is not available for the 
attributes with the primary key.**

For more details on Attribute Mapping [click here](/transformation/getting-started-with-mapping/).