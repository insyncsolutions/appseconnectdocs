---
title: "ZohoRecruit"
toc: true
description: "Get to know how you can configure ZohoRecruit credential in OP and Cloud agent, APIs, Actions and its filter."
keywords: "Pre-requisites for ZohoRecruit Configuration, Configure the ZohoRecruit Application in OP Agent, Configure the ZohoRecruit Application in Cloud Agent"
tag: developers
category: "Connectors"
menus: 
    zohosolution : 
        icon: fa fa-gg
        weight: 3
        title: "ZohoRecruit"
        identifier: zohorecruitconnector
---

## What is ZohoRecruit?

`Zoho Recruit` is a talent acquisition system catering to multiple hurdles faced by recruiters. 
With complete solutions for both in-house recruiters and staffing agencies, Zoho Recruit 
helps you source, track, and hire the best candidates, without any juggling required across different media.  

### What are the Advantages of Using ZohoRecruit as a hiring platform?

- Job Requisition Management  
- Customized Application Form     
- Duplicate Candidate Prevention      
- Applicant Tracking   
- Candidate Search    
- Publish to Social Media     
- Reporting       

However, application configuration is an integral activity prior to the process of integration. If your chosen application 
is `Zoho Recruit`, credentials need to be provided for validating the agent. Here you will find the detailed 
description on how to configure the agents in both `OP` and `Cloud` for `Zoho Recruit`.  

## Pre-requisites for Zoho Recruit Configuration 

1) Create a [developer account](https://accounts.zoho.in/register?servicename=AaaServer&serviceurl=https%3A%2F%2Fapi-console.zoho.in%2Flogin) in `Zoho` with necessary credentials. 
You need to activate your account before using the same.      
2) [Click here](https://www.zoho.com/recruit/developer-guide/apiv2/oauth-overview.html) to know the authentication mechanism and APIs of the application along with their structures.       
3) Email ID and Password of `Zoho` application to login successfully.    
4) You need to provide the access permission to your created client in `Zoho` from `Zoho Recruit`.       

### How to create a Client in Zoho?

1) Login to `Zoho` with valid credentials. From the dashboard page, click on `GET STARTED`.      
2) Select `Server-based Applications` as `Client Type`. 
![zohorecruit1](/staticfiles/connectors/media/application-connector/zohorecruit1.png)  
3) Provide `Client Name`, `Homepage URL` and `Authorized Redirect URIs`. On clicking `Create`, 
your app will be created as well as the `Client ID` and `Client Secret` will be generated. 
From the dashboard, select a specific `Client` and navigate to `Client Secret` such that you will get 
`Client ID` and `Client Secret`.   
![zohorecruit2](/staticfiles/connectors/media/application-connector/zohorecruit2.png)

### How to access ZohoRecruit from Zoho?

1)Login to your `Zoho` account with valid credentials. From the dashboard, expand the `user icon` on top right corner 
and click on `My Accounts`.           
![zohorecruit5](/staticfiles/connectors/media/application-connector/zohorecruit5.png)
2) On clicking the `grid` at the top left corner of the `user profile` page, a menu bar will appear providing 
all the `APPS` that are available inside `Zoho`. Scroll down and select `Recruit` under `HUMAN RESOURCES`. On performing, 
the same you will land on the dashboard of `ZohoRecruit`.
![zohorecruit6](/staticfiles/connectors/media/application-connector/zohorecruit6.png)

## On-Premise Agent Configuration 

### Installation of On-Premise Agent 

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration).    

### How to configure Zoho Recruit Application in OP Agent 

1) Create a [triggered processflow](https://docs.appseconnect.com/processflow/trigger-processflow/) with Zoho Recruit as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.     
2) Open the agent and click the checkbox in Settings Panel.        
3) Move into the App Configurational Panel of the agent and configure the details of the respective application.         

### Steps to configure the credentials in the OP agent 

1) Open the OP Agent by providing valid credentials. 
2) In the App Configurations panel of the agent, click on the + button, beside the application Zoho Recruit. 
The credential panel opens for the application Zoho Recruit.  
![zohorecruit3](/staticfiles/connectors/media/application-connector/zohorecruit3.png)
3)Provide the credentials for your applications. The following fields are required for validating the credentials. 
The Authentication fields for OAUTH 2.0 are :

- Base URL - Provide the base url of `Zoho`application.   
- OAuth URL - This URL is generated along with the Client ID and Client Secret in the REST application itself.   
- Token URL - A client-authorized key that lets the client access protected resources from Zoho. Enter the Access Token URL. 
- Client ID - This is generated when the client logs into the Application.
- Client Secret - This field is also generated by the REST supported Application.
- Call Back URL - This is the secondary URL required for data restoration.
- Scope - Scopes defines the specific actions applications can be allowed to do on a user behalf.   
![zohorecruit4](/staticfiles/connectors/media/application-connector/zohorecruit4.png)

4) Click on the `Authorization` button, to validate the connection. 
After clicking `Authorization`, a pop-up browser will open re-directing you to `ZohoRecruit` login page. 
Provide valid login credentials and click on `Login`. The validation starts immediately, and `Authorization Successful` will be displayed, if valid login credentials have been provided. 
Following the above processes, you can configure the ZohoRecruit application in the OP agent. 

## Cloud Agent Configuration 

### Configure the DocuSign Application in Cloud Agent

1) Login to `APPSeCONNECT` portal with valid credentials.   

2) Navigate to **Manage > App**. Expand the `ZohoRecruit` application and click on `Credential`. 

3) Expand the `REST` node, click on `Add New Credential`.  

4) Provide the credentials for your applications. The following fields are required for validating the credentials. 
The Authentication fields for OAUTH 2.0 are :

- Base URL - Provide the base url of `Zoho`application.   
- OAuth URL - This URL is generated along with the Client ID and Client Secret in the REST application itself.   
- Token URL - A client-authorized key that lets the client access protected resources from Zoho. Enter the Access Token URL. 
- Client ID - This is generated when the client logs into the Application.
- Client Secret - This field is also generated by the REST supported Application.
- Call Back URL - This is the secondary URL required for data restoration.
- Scope - Scopes defines the specific actions applications can be allowed to do on a user behalf.  
![zohorecruitcloud](/staticfiles/connectors/media/application-connector/zohorecruitcloud.png)    

5) Click on `Grant`, to validate the connection. 
After clicking on `Grant`, a pop-up browser will open re-directing you to `ZohoRecruit` login page. 
Provide valid login credentials and click on `Login`. The validation starts immediately, and `Authorization Successful` will be displayed, if valid login credentials have been provided. 
Following the above processes, you can configure the ZohoRecruit application in the `Cloud` agent. 

## Troubleshooting

**ISSUE 1** 

Some of the basic troubleshooting issue happens due to improper validations or even if it is accurately validated but the 
processflows do not sync the data successfully. This basic issue resolves after removing the Temp and Cache files from the 
portal and from your system. Therefore, after clearing the Temp and Cache files, again deploy and execute your processflow.  

**ISSUE 2**

User validation may fail due to invaild `Base URL`, `OAuth URL`, `Token URL`, `Client ID`, `Client Secret`, `Call Back URL` and `Scope`. Check the credentials once again and re-Validate the credentials. 

## Attributes and Actions

While defining a connection to an API in `ZohoRecruit`, you require clear understanding about the data requirements and endpoint configurations. 
You can refer to this document to find all the endpoint details of `ZohoRecruit`. To define the endpoint in APPSeCONNECT, you need 
to define Schemas and Actions. Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. Here is the 
list of some of the pre-packaged API actions defined for you which you can easily plug and play while doing your integration.

>Click here [ZohoRecruit](https://www.zoho.com/recruit/developer-guide/apiv2/get-roles.html) to know the authuorization and APIs details. 

|Endpoint|Action|Action Type|Schema|UI Help|API Path|
|---|---|---|---|------|-----|
|Candidates|Get Candidates|GET|Candidates|Retrieves details of each candidates.|-| 
|users|Users|GET|users|Retrieves details of each users.|[users](https://www.zoho.com/recruit/developer-guide/apiv2/get-users.html)|

>Since, we are using a triggered processflow, no need to use any action filter.   

