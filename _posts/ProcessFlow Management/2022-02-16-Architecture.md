---
title: "Architecture"
toc: true
tag: developers
category: "Processflow"
menus: 
    processflow:
        title: "Architecture"
        weight: 2
        icon: fa fa-gg
        identifier: architectureprocessflow
---

**ProcessFlow** is the main workspace of the product which lets you build an advanced and smart integration solution. 
ProcessFlow gives you an IDE that lets you build an integration that is best suited for your customers while giving you the option to deploy and execute from the same. 
A processflow, under the hood creates a micro-service architecture 
that can run in **Cloud servers** or **On Premise** getting or pushing data directly to the applications 
in execution and generate both transactional and data logs. In this article, we will see how the 
architecture of APPSeCONNECT processflow is laid out such that we can understand the under the hood big 
picture of the processflow. 

## Architecture

![processflow Architecture 01](/staticfiles/processflow/media/processflow_architecture_01.png)  

You can achieve your business specific needs by creating a processflow and deploying them. Your execution 
can happen on cloud directly on an hosted environment maintained by APPSeCONNECT, or it can generate a call 
to your own on-premise environment and execute the business flow using our APPSeCONNECT integration tool. 

When the user triggers a processflow manually (or APPSeCONNECT Scheduler triggers it for you), the first thing 
it tries to do, is to identify the environment(s) on which the processflow needs to be executed on. It can either 
execute itself on APPSeCONNECT cloud premise on an hosted agent, or on-premise environment where the agent 
is installed. The processflow starts with `Start` node and execute each links to find the next node. 
The nodes plays a vital role in a processflow determining what action it needs to execute, and passing or delegating 
activities to different workloads. 

The processflow engine takes care of each and every task or activity that needs to be executed on the platform. The 
engine takes help of Adapter to call individual Applications to invoke Get or Post actions. The engine calls the 
adapters, execute storage plugins, triggers notification, generate logs etc. 

If there is any cloud involvement from an on-premise execution or an on-premise dependency for a 
cloud solution, it triggers the call automatically using Service Bus and executes the process. 

The repository services takes care of storage and snapshot of the processflow executions which one can investigate later.


