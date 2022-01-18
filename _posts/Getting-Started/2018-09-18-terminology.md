---
title: "Terminology"
toc: true
tag: developers
category: "Getting Started"
menus: 
    gettingstarted:
        title: "Terminology"
        weight: 3
        icon: fa fa-wpexplorer
        identifier: terminology
---

Users of APPSeCONNECT requires the knowledge of common terminologies that the user can come across,while working with the 
integration process in APPSeCONNECT.Some of the common terminologies that user can frequently come across while handling the integration process are mentioned below.

##Terminology related to APPSeCONNECT

|Phrases|Details|
|---|---|

|***Action***|Action are certain tasks like getting data from an application or sending data to an application based on specific API filter conditions known as Action Filters.|
|***Adapter***|Adapter is a piece of software component of an application which resides with the agent locally,that helps APPSeCONNECT communicate to the respective application efficiently and seamlessly for a complete sync process.|
|***Agent***|APPSeCONNECT Agent is an application which execute and control the sync process by transferring data from one application to another with the help of adapters,after performing required data conversion or manipulation.The Agent is either locally installed in the target organization’s server or can reside withn the APPSeCONNECT cloud platform depending on the deployment model chosen,to handle the sync processes for an organization exclusively.|
|Attributes|In APPSeCONNECT,an attribute is a property or characteristic of a schema.|
|***Connectors***|Connectors are plug and play oriented that act like a bridge to create connection between applications that connects different data sources both on-premise or in cloud using standard protocol based communication channel.|
|***Custom Renderer***|Custom Renderer feature is targeted to build a complex XML structure according to business requirement without performing field to field mapping.|
|***Environment***|APPSeCONNECT platform enables end-users to create and manage multiple deployment environment for free-flowing and smooth integration between various applications.|




|Log Bucket |For every transaction, log is generated that is shown in the OP Agent and in Snapshot. These generated logs are shown in the Log bucket of the agent and Snapshot.|
|Resync Bucket|The errors that have occurred during the sync process are displayed in the Resync bucket of the OP Agent and Cloud Agent.At an instance Resync bucket shows 1000 data.|
|Resync|The errors generated during the sync process are available for another attempts. Any changes and rectification to the errors are made, user can either resync the data manually or can schedule the resync accordingly.|


|***License Management***|License key-based authentication approach is security enhancement for your on-premise and cloud integrations. This mechanism authenticates users who tries to login to the integration client of APPSeCONNECT agent using a revocable, secure and unique license or a security token that is provided by the server.|
|***Lookup Mapping***|Lookup Mapping is a puissant feature in APPSeCONNECT which enables the end-users or implementer to provide a specific value to the application environment,such that when the source and destination application is integrated,the value in source application can easily be integrated with its value in destination application,corresponding to their respective fields.|
|***Mapping***|The process by which end-users or implementor can transfer the data between schemas of source and destination application to perform a smooth and efficient sync is called mapping.|
|***ProcessFlow***|ProcessFlow is a one-stop solution of APPSeCONNCET that enables end-users to represent the bussiness flow graphically such that the data can be synced or integrated between various business applications in a free-flowing and flexible way.|
|***Root Variable***|These are global variables that can be used in any attributes of any Complex objects & Complex Objects Collections.|
|***Rules***|When end-users of APPSeCONNECT wants to perform some ACTIONS based on the type of EVENTS encountered during execution of integration,then those ACTIONS related to corresponding EVENTS will be termed as Rule.|
|***Schema***|Schema is the skeleton structure that repersents the logical view of the application,showing all the attributes,actions and contraints that are currently available to perform smooth business operation.|
|***View Snapshot***|Snapshot gives a detailed overview of the data that is being transferred through workflow and processflow giving you a complete picture of the data transformed through the sync process.The snapshot provides tracing over the data transferred through integration and options to investigate the Data Log,Transaction files & the Activity Log for each process execution.|
|***Workflow***|Workflow is a powerful feature in APPSeCONNECT which enables orchestration of business processes with desired efficiency and optimality by allowing end-users to diagrammatically organize,create and view the data flow of a process for integration.|
