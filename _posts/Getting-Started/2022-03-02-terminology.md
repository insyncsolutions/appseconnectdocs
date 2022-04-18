---
title: "Terminology"
toc: false
tag: developers
category: "Getting Started"
menus: 
    gettingstarted:
        title: "Terminology"
        weight: 3
        icon: fa fa-wpexplorer
        identifier: terminology
---

Users of APPSeCONNECT requires the knowledge of common terminologies that the user can come across, while working with the 
integration process in APPSeCONNECT. Here are some of the common terminologies that user can frequently come across.

## Table of the Terminology of APPSeCONNECT

|Terms|Details|
|---|---|
|***ProcessFlow***|A ProcessFlow or more specifically a Business Process Flow is a complete business process mapping that include multiple data integration points to sync data together. In other words, a ProcessFlow is a set of different integration points which commonly run together to make a complete meaningful update to the business applications. A process flow is the main integration solution created for a particular problem statement. When we create an integration between applications, it is the Process flow designer which aids in developing what data to flow and how it should flow from one application to another.|
|***Agent***|APPSeCONNECT Agent is an application which execute and control the sync process by transferring data from one application to another with the help of adapters. The Agent is either locally installed in the premise of the user or can reside within APPSeCONNECT cloud platform depending on the deployment model chosen.|
|***Environment***|APPSeCONNECT platform enables end-users to create and manage multiple deployment environment. You can create different environments for Development, UAT and Production, ensuring the data present in one environment becomes completely isolated to another, thereby ensuring complete freedom on handling multiple infrastructures.|
|***Schema***|Schema is the skeleton structure of an API or a Data Structure. It allows you to define the structure of data which needs to be passed to the target application to make meaningful update to the application.|
|***Attributes***|Attributes are the unit of data in a schema. A schema is defined by its attributes. Each attribute holds an unit of data to be passed through an API.|
|***Action***|Actions are the operations on an API. It defines the actual endpoint where the data needs to be passed to perform the operation. Actions are tightly coupled with Schema, ensuring a specific data structure can only represent data for a specific Action.|
|***Adapter***|Adapter is a piece of software component of an application which resides within the agent and helps APPSeCONNECT to communicate with the respective application efficiently.|
|***Packages***|Packages are plug and play oriented that act like a bridge to create connection between applications that connects different data sources both on-premise or in cloud using standard protocol based communication channel.|
|***Custom Renderer***|Custom Renderer feature is targeted to build a complex XML structure according to business requirement without performing field to field mapping.|
|***License***|License is a key-based authentication approach which secures every execution of your on-premise and cloud integration. Proper licensing ensures data safety and security such that data could freely flow from one application to another easily and quickly. Failed or invalid license increases the risk of data corruption and compromization.|
|***Nodes***|Nodes are associated with a particular action which uses specific action filters and credentials mentioned to the application to get a response back to APPSeCONNECT. Each node in APPSeCONNECT is tied to a particular connection, such that when the node is executed the data from that particular Application is generated and responded back to the application workspace.|
|***Links***|Links are termed as connection to two or more nodes demarking the flow of data from one node to another. In certain scenario, a link can also point to itself, which is termed as self-loop, this kind of loops will indicate a continuous flow of execution of a single node and triggering the data back to the flow.|
|***Sync Info***|During the sync process, the errors that have occured will be displayed in the Sync Info window. The Sync info groups the data particularly based on data mapping, enabling the user to manually resync the data whenever needed.|
|***Resync***|The platform tracks each and every data processed through it. It lists the status of the tracked data enabling you to resync the failed data either automatically or manaully.|
|***Snapshot***|Snapshot gives a detailed overview of the data that is being transferred through workflow and processflow giving you a complete picture of the data transformed through the sync process. The snapshot provides tracing over the data transferred through integration and options to investigate the Data Log, Transaction files & the Activity Log for each process execution.|
|***Mapping***|The process by which end-users or implementor can transfer the data between source application and destination application to generate a data packet understandable to the destination application through mapping. Data mapping is a technique of producing one to one data mapping between two schemas such that a conversion rule is created to generate the target schema.|
|***Lookup Mapping***|Lookup Mapping is a puissant feature which enables the end-users or implementer to provide a specific value to the application environment, such that when the source and destination application is integrated, the value in source application are replaced by the value in destination field, which is understandable to the target application.|
|***ProcessFlow***|ProcessFlow is a one-stop solution of APPSeCONNCET that enables end-users to represent the bussiness flow graphically such that the data can be synced or integrated between various business applications in a free-flowing and flexible way.|
|***Variables***|These are storage unit that can be used in any expressions while designing the ProcessFlow. The variables can be scoped to local or global ensuring the data is available for reuse in multiple nodes.|
|***Rules***|When end-users of APPSeCONNECT wants to perform some ACTIONS based on the type of EVENTS encountered during execution of integration, then those ACTIONS related to corresponding EVENTS will be termed as Rule.|
|***Technology Applications***|APPSeCONNECT comes with a number of technology connectors which can connect any data source having standard protocol-based communication channel established.|
|***APPSeCONNECT Expression Language***|APPSeCONNECT provides an Expression language which helps in defining the data mapping. The Expression langauge can be used in various expression syntaxes to generate final output of data.|