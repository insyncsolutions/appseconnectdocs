---
title: "Understanding Components of Mapping"
toc: true
description: "Mapping provides a visual interface where one can map data coming from an API to another using our platform."
keywords: "Structure of Mapping, Attribute Mapping"
tag: developers
category: "Transformation"
menus: 
    transformationbasic:
        title: "Understanding Components of Mapping"
        weight: 1
        icon: fa fa-file-word-o
        identifier: tmappingcomponents
---

Mapping triggers the transformation process between the Source and the Destination Applications. 
Source and Destination schemas are mapped in the Transform section of the processflow. 
This document will help you to know about the components required for executing `Source-Destination` Mapping 
in APPSeCONNECT portal.

![Scenario1-GroupingCondition](/staticfiles/Transformation/media/mapping_defaultscreen.png)

## Components of Mapping

Mapping of the attributes of destination application with source application attributes is implemented by the process known as `Source-Destination` mapping. 
The components present for implementing the Mapping process are as follows :

### For-Each loop 

This is used for execution on a block of code on each element in a collection of items. 
It is useful to display each item in a collection of items until the loop finishes its execution. 
Under `For-Each loop` entities have been used and variables are set under entities. Every time the processflow is executed 
the loop undergoes the execution for the transformation instead of writing the logic multiple times. 

>The path provided beside the For-Each-Loop is the [XPath of the XML](/transformation/understanding-xml-and-xpath/) for that processflow. 

### Schema 

This is the skeleton structure of an `API` or a Data Structure. It allows you to define the structure of data which needs to be passed to the target application to make meaningful update to the application. 

### Complex Object Collection 

This specify the mapping list within a complex object. This mainly includes the collection of complex object and attributes. 

### Complex Object 

Complex Objects are the objects which are highly structured and large in size (can also be small) of Variable Representation Length (VLR). 

### Attributes 

Attributes are the unit of data in a schema. A schema is defined by its attributes. Each attribute holds an unit of data to be passed through an API. 

### Root Variable 

These are the Global variable which can be used inside any entity.  

### Root Entity Variable 

Root Entity Variable can be used several times in different parts of the transformation process underlying in the processflow. 

### Namespaces 

This feature is used to differentiate two `XML files` for avoiding the duplication and redundancy. 

### Renderer 

APPSeCONNECT provides a feature to define and format XML rules as needed while implementing Attribute Mapping. 
XML has a default expression which can be viewed in the XSL after the Mapping. This default expression can be overridden by the Renderer. 



