---
title: "Real-Time Sync Strategy"
toc: true
description: "Get to know about real-time data synchronization to successfully perform your business integration."
keywords: "real-time sync, real-time, realtime, realtime sync"
tag: developers
category: "best-practices"
menus: 
    bp:
        title: "Real-Time Sync Strategy"
        weight: 3
        icon: fa fa-wpexplorer
        identifier: bprealtimeway
---

In the case of `Real-time` sync, the data is never pulled from the application end, but rather it is pushed automatically 
using a Webhook component from the application. The request is made directly to the integration platform to do 
actual integration. For the security of data failure, many integration providers give a proxy component that stores the messages into a 
persistent store before pushing it to the integration platform. 

Here the requester is the application that pushes data to the integration platform using the request channel. The message 
is transformed and a reply is created to indicate whether the process is successfully executed or not. 

There are two patterns that one can follow while developing real-time sync : 

- Synchronous Pattern 
- Asynchronous Pattern

{::comment}
```plantuml!
"Source App" -> APPSeCONNECT: Pushes data
activate APPSeCONNECT
APPSeCONNECT-> "Source App" : Waits for the processing to complete and then Return response
deactivate APPSeCONNECT
==Asynchronous==
"Source App" -> APPSeCONNECT: Pushes data
activate APPSeCONNECT
APPSeCONNECT--> "Source App": Returns acknoledgement before executing.
APPSeCONNECT-> "Source App": Finishes execution
deactivate APPSeCONNECT
```
{:/comment}
![realtime_sync](/staticfiles/umldiagram/media/realtime_sync.png)

## Synchronous Pattern 

This pattern is based on the `Request/Reply` model. When an end-user creates or modifies any records on the source application, the data is pushed to a URL immediately. 
Source application then sends a message containing the record data to the integration, and suspends further processing while it waits for a response. 
The integration after receiving the message, performs any transformations, and sends to the destination application. 
The integration handles the response from destination application and returns a confirmation message to the source application. 
Once the source application receives the response, it continues with any post-processing tasks. 


**Pros and Cons**

- The synchronous pattern is safe and the source application can identify whether the process has completed successfully or not. 
- Synchronous pattern responds at a slow rate and hence the source application might need to wait longer. 

## Asynchronous Pattern

In the case of an asynchronous pattern for real-time processing, the response is immediately sent back by creating a 
Co-Relation Id. The fire and forget pattern requests the integration provider when there is an update in the source application. 
The integration receives the request, validates whether the data is perfect and then responds back as Accepted with a 
generated Co-relation id. After that, the data is being processed and the actual output or response for that particular 
integration point is written for that particular referenced co-relation id. The source needs to call a special API again 
to retrieve the actual response for that particular request. 

**Pros and Cons**

- Fire and forget pattern is ideal when there is a large amount of load in the source application and it does not bother whether the data is actually processed or not. 
- Fire and forget pattern will have overhead of calling another API after actual execution to identify whether the data is successfully processed or not. 
- Fire and forget needs a Queue to back up in the integration platform, to ensure the messages are processed in correct order. 

