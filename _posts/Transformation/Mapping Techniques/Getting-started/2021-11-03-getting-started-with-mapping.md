---
title: "Introduction"
toc: true
description: "Mapping provides a visual interface where one can map data coming from an API to another using our platform."
keywords: "Structure of Mapping, Attribute Mapping"
tag: developers
category: "Transformation"
menus: 
    transformation:        
        title: "Getting Started"
        weight: 1
        icon: fa fa-wpexplorer
        identifier: mappinggettingstarted
---

Getting started section of mapping will help you to understand the main areas, you should be familiar with 
before start doing the transformation process. `Mapping` triggers the transformation process between the Source and the Destination Applications. 
Source and Destination schemas are mapped in the transformation section of the processflow. 

It is important to note that a processflow caters to a particular schema or an entity. A processflow maps the source schema 
for a particular action with the destination schema, thus facilitating the transfer of information between the schemas. The 
attributes of the schema may vary for different applications. Also, the data arriving from the source application may have a 
different format than the destination application. To resolve the issues that may arise, you can use Mapping. 

Mapping in a processflow is required to define which attributes of the target schema correspond to those of the source schema. 
In this effort, you write the logic that facilitates this transformation. Attribute mapping thus forms the main part of 
transforming data from one format to another. 

This document will help you to know about the `different types of Mapping` done in APPSeCONNECT portal for easy 
data transformation and smooth data integration between the applications.

## Structure of Mapping

The basic structure of mapping contains three main fields :

* Transformation
* Root Variable
* Tracking

![structure-of-mapping](/staticfiles/Transformation/media/structure_of_mapping.png)

### Transformation

This is the field where the attributes corresponding to the schema are mapped. This is 
also the place where the logic behind the transformation is implemented such that the 
integration proceeds uninterrupted. The various attributes that may be linked to the 
integration are declared here along with their child fields.

### Root Variable

To facilitate mapping in a processflow, you require root variables that store the data temporarily, to be 
used later in the transformation process. Root variables can be used for different 
purposes. They are used for storing data returned from an AppResource function, 
to store values returned from complex XPath expression or to store a chunk of XML 
data which you can use later in the mapping. A root variable may be used several 
times for data while setting up the transformation and is not entity item specific.

Once a root variable has been declared it can be used for the transformation of 
each and every item. The different root variables that may be required in the transformation process are defined 
in this section.

### Tracking

As the name suggests, `tracking` may be used to study the data synchronization from the source application to the destination application. 
Tracking provides an opportunity to include more details with the source schema items when they are being 
transferred to the destination schema.

When you execute a processflow, you can see the various data being transferred in the sync info 
along with the status of the sync. The data belongs to a schema and thus, 
has a schema id. The sync info only enlists each entity item by their primary id. 


## Basics of Attribute Mapping

You need to understand the XML and XPath types along with Attribute Mapping
process. This section will also elaborate on the APPSeCONNECT Mapping types. 

* [Undertanding XML & XPATH](/transformation/understanding-xml-and-xpath/)

* [Working with Schema Attribute & Action](/processflow/processflow-app/)

* [APPSeCONNECT Expression Syntax](/transformation/appseconnect_expresssion_syntax/)



