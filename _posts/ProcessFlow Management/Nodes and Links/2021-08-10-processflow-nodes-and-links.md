---
title: "Nodes and Links overview"
description: "Nodes are individual units of execution which you can drag and drop in the ProcessFlow Designer to generate a data integration pipeline. A node performs a set of operations to the data to ensure the execution goes through various modules of execution unit to give you the result you desire."
keywords: "Nodes and links, start node, get node, mapper node, post node, splitter node, merger node, self node, delay node, decision node"
toc: false
tag: developers
category: "Processflow"
menus: 
    processflow:
        icon: fa fa-link
        weight: 7
        title: "Nodes and Links" 
        identifier: processnodeandlinks 
---

Given below is the list of elements you will be able to use in APPSeCONNECT processflow. You can use the following nodes for designing and executing processflows for sync purpose :

|Processflow Nodes|Description|
|------------------|----------------|
|[Start Node](/processflow/working-with-Start-Node/)| This node initiates the start process of the processflow execution. You cannot SAVE or execute a processflow without a Start Node.|
|[GET Node](/processflow/processflow-app/)|This node fetches the data from the source application for the sync purpose. You need to enable the APP dragged for operating GET node by selecting the Node Type as GET in the Node Configuration window of the dragged application.|
|[Mapper Node](/processflow/working-with-mapper/)| This node transforms the data to the destination application by applying field mappings of source and destination application.|
|[POST Node](/processflow/processflow-app/)| This node dumps the transformed data to the destination application after the transformation process is completed. You need to enable the destination application as POST node by selecting the Node Type as POST in the Node Configuration window of the dragged destination application.|
|[Splitter Node](/processflow/working-with-processflow-splitter/)|Splitter Node in processflow will split the incoming data into small packets such that the execution load of bulk data can be minimized during the execution process.|
|[Merger Node](/processflow/working-with-revamped-merger/)|Merger Node in processflow will merge multiple data into batches as per the input provided by the user.|
|[Self loop](/processflow/working-with-processflow-selfloop/)|This enables the user to apply self-loop on a node such that on execution, the self-loop will iterate until all data is available from its predecessor node.|
|[Delay Node](/processflow/working-with-processflow-delay/)| This node will enable you to hold the execution flow for a specific period, so as to fetch more incoming requests from the Predecessor Node. Delay node can be implemented anywhere within a processflow, and the configuration for implementing delay can be provided using Static Time or by using a Dynamic Time.|
|[Decision Node](/processflow/working-with-decision/)|This node enables you to apply condition checks for filtering redundant data.|
|End Node| This node signifies the completion of the sync process. You may or may not use the End node to design processflows.|
