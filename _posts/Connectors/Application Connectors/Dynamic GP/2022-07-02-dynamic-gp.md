---
title: "Dynamic GP"
description: "Get to know how you can configure the agent for Dynamic GP"
keywords: "Sage 300  Configuration, Configure the Sage 300 Application"
toc: true
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "Dynamic GP"
        weight: 22
        icon: fa fa-file-word-o
        identifier: sage300connector
---

Application configuration is an integral activity prior to the process of integration. If your chosen application is 
Dynamic GP, credentials need to be provided for validating the agent. Here you will find the detailed description on 
how to configure the agents for the application Dynamic GP, Troubleshooting issues, action and its filters. 

Dynamics GP is a business management solution for small and mid-sized organizations that automates and streamlines 
business processes and helps you manage your business. Microsoft Dynamics GP has applications for financial management, 
human resources management, manufacturing planning, supply chain management, field service, business intelligence, 
collaboration, compliance, and IT management. This section provides you the detailed process of validating the 
credential of the application Dynamic GP. 

## Pre-requisites for Dynamic GP Configuration 

1. Dynamic GP should be installed in your server with all admin previlages. 
2. The server should be available where Dynamic GP is installed along with the User ID and Password to access the same.  
3. You need to know the Authentication and APIs of the application.  

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Dynamic GP Application in the Agent

1. [Create a processflow](/getting%20started/create-your-first-processflow/) with Dynamic GP as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure the credentials in the Agent

1) Open APPSeCONNECT Agent by providing correct credentials. 

2) In the **Apps Configurational panel** of the agent, you will be able to view the Dynamic GP application. Click on the `+` icon to add the credential.    
![sapb1_agent](/staticfiles/connectors/media/application-connector/sapb1_agent.png)

3) Provide the credentials of Dynamic GP application.
![sapb2_agent](/staticfiles/connectors/media/application-connector/sapb2_agent.png)

