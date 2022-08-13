---
title: "Dynamics AX"
description: "Get to know how you can configure the agent for Dynamics AX, action and its filters."
keywords: "Dynamics AX Configuration, Dynamics AX Application Configuration in OP Agent, Dynamics AX Application Configuration in Cloud Agent."
toc: true
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "Dynamics AX"
        weight: 26
        icon: fa fa-file-word-o
        identifier: dynamicsaxconnector
---

Dynamics AX is a powerful enterprise resource planning(ERP) software package for finance and operations. 
It helps global enterprises organise, automate, and optimise their processes on-premises, in the cloud, 
or through hybrid deployment. It’s part of the Microsoft Dynamics suite of intelligent business applications. 

As `APPSeCONNECT` is a Business Process Automation tool, this will allow you to develop and configure seamless integration between business applications. 
Therefore, application configuration is a fundamental activity prior to the process of integration. If your chosen application is 
`Dynamics AX`, credentials need to be provided for validating the agent both in case of `OP` and `Cloud`. Here you will find the detailed description on 
how to configure the agents for the application `Dynamics AX`, Troubleshooting issues, action and its filters. 

## Pre-requisites for Dynamic AX Configuration 

1. The server where `Dynamics AX` and `APPSeCONNECT` agent is installed should be available along with `Company Name` and `User Account` already created in the application. 
2. You need to create `Inbound Port` for every service you need to access from the application. 
Navigate to `Dynamics AX` -> Select any company -> `System Administration` -> `Inbound ports`. Click on `New`, a window will 
appear where you need to provide `Port Name` and `Description`. Select `HTTP` as Adapter and click on `Configure`. 
From `Service Contract Customizations`, select the services that you need to add in the current port. 
3. `Server Name` along with its `username` and `password` should be available. 
4. `Company Name`, `AX InstanceName` and `Network Domain` should be provided to you while handing you the server.  
5. You need to provide a customer id obtained from the application in `Account No for Validation`. 
Open dynamics AX in your local server. Select the company that has been provided to you, 
click on `Account Receivable` -> `All Customers`. A list of customers will appear along with their customer id. Choose a 
customer id and put it in the `OP` agent.
7. In `Service Name`, you need to provide the port name that you have used will creating the `inbound port`. 

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Dynamic AX Application in the Agent

1. [Create a processflow](/getting%20started/create-your-first-processflow/) with Dynamic AX as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure the credentials in the Agent

1) Open APPSeCONNECT Agent by providing correct credentials. 

2) In the **Apps Configurational panel** of the agent, you will be able to view the Dynamic AX application. Click on the `+` icon to add the credential. 
![dynamicsop1](/staticfiles/connectors/media/application-connector/dynamicop1.png) 

3) Provide the `Server Name`, `Network User`, `AX Instance Name`, `Network Password`, `Service Name`, `Network Domain`, `Company Name` and `Account No for Validation`.
![dynamicsop2](/staticfiles/connectors/media/application-connector/dynamicop2.png) 

4) Click on the "Validate" button, to validate the connection. 
A message "Test Connection Successful" will appear if all the credentials provided by you for Dynamic AX is valid. 
In this way, you can configure the credentials of Dynamic AX.  

5) After providing and validating all the credentials. Click "Save" button. 
A message "Connection Data Saved" will appear if all the credentials provided by you for Dynamic AX is valid.

## Troubleshooting

**Issue 1** 

Agent validation fails due to improper `Server Name` and `Database Name`. You need to check that the 
`Server Name` where `Dynamics GP` is installed is provided correctly in the OP agent. In order to check 
the `Database Name`, open `SQL Server` with correct login credentials. While `SQL Server` opens up, 
you will be able to see the database name in the left panel, check it whether it is matching exactly with 
the database name provided in the OP agent. 

