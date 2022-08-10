---
title: "Dynamic GP"
description: "Get to know how you can configure the agent for Dynamic GP"
keywords: "Dynamic GP Configuration, Configure the Dynamic GP Application"
toc: true
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "Dynamic GP"
        weight: 22
        icon: fa fa-file-word-o
        identifier: dynamicgpconnector
---

Application configuration is an integral activity prior to the process of integration. If your chosen application is 
Dynamic GP, credentials need to be provided for validating the agent. Here you will find the detailed description on 
how to configure the agents for the application Dynamic GP, Troubleshooting issues, action and its filters. 

Dynamics GP is a business management solution for small and mid-sized organizations that automates and streamlines 
business processes and helps you manage your business. Microsoft Dynamics GP has applications for financial management, 
human resources management, manufacturing planning, supply chain management, field service, business intelligence, 
collaboration, compliance, and IT management. This section provides you the detailed process of validating the 
credential of the application Dynamic GP. 

**Note : This document is for configuring Dynamic GP in On-Premise Agent only.** 

## Pre-requisites for Dynamic GP Configuration 

1. Dynamic GP should be installed in your server with all admin previlages. Dynamic GP and SQL Server may or may not be hosted in the same server.  
2. The server should be available where Dynamic GP is installed along with the `Company Name`, `User ID` and `Password` to access the same.  
3. You need to know the Authentication and APIs of the application.
4. `Server Name`, `Database Name`, `CustomerNo`, `SQL Server UserId` and `SQL Server Password` should be available. 
5. `eConnect Service` should be available for the server and all user permission should be provided for the server where `Dynamics GP` is installed. 

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

3) Provide the credentials for `Server Name`, `Database Name` and `CustomerNo`. 
`SQL Server UserId` and `SQL Server Password` are optional ones, if available you can provide them. 
`Server Name` and `Database Name` will be provided to you by your client at the being of the configuration process. 
You can find a valid CustomerNo following either of the below procedures. 

- Open `SQL Server` with correct login credentials that have been provided to you. In the left panel under 
`Object Explorer`, expand `Databases` node and find out the database that you are looking for. Click on `New Query` in the toolbar. 
To find a valid CustomerNo you need to write the query `select * FROM RM00101` and  execute it. The query will return 
you a list of customers that are present in DynamiC GP. Select any `CustomerNo` from `CUSTNMBR` column and put it in the agent. 

- Open `Dynamics GP` with valid `Company Name`, `UserId` and `Password`. From the dashboard navigate to `Sales -> Cards -> Customer`. 
As the Customer Maintenance dialog box opens up, click on the lookup icon beside the Customer Id text box. 
The `Customers and Prospects` opens up, showing you all the customers that are currently available in the application along with the Customer Id. 
Click on any `Customer Id` and the details will be available. You can select any customer Id from here.

4) After providing all the credentials. Click "Save" button. 
A message "Connection Data Saved" will appear if all the credentials provided by you for Dynamic GP is valid.

5) Click on the "Validate" button, to validate the connection. 
A message "Test Connection Successful" will appear if all the credentials provided by you for Dynamic GP is valid. 
In this way, you can configure the credentials of Dynamic GP.  

## Troubleshooting

**Issue 1 : Agent Validation Failed due to improper `Server Name` and `Database Name`.** 

Agent validation fails due to improper `Server Name` and `Database Name`. You need to check that the 
`Server Name` where `Dynamics GP` is installed is provided correctly in the OP agent. In order to check 
the `Database Name`, open `SQL Server` with correct login credentials. While `SQL Server` opens up, 
you will be able to see the database name in the left panel, check it whether it is matching exactly with 
the database name provided in the OP agent.  

**Issue 2 : Agent Validation Failed due to improper CustomerNo.**

Sometimes agent validation fails due to improper CustomerNo provided in the agent. You should provide a 
valid CustomerNo which is already present in the database. Since `APPSeCONNECT` communicate with `Dynamics GP` 
using a `eConnect Service`, thus while validating the configuration provided in the OP agent, APPSeCONNECT 
sends a eConnect service request along with the CustomerNo to the application. If the specified CustomerNo is available, 
the application sends a response to the agent else the validation fails and you need to find a valid 
CustomerNo following either of the below procedures. 

- Open `SQL Server` with correct login credentials that have been provided to you. In the left panel under the 
`Object Explorer`, expand `Databases` node and find out if the database that you are looking for is availbale or not. If so, 
then click on `New Query` in the toolbar. Since `Dynamic GP` stores all customer related records in `RM00101` table, so to find a
valid CustomerNo you need to write the query `select * FROM RM00101` and  execute it. The query will return you a list of 
customers that are present in DynamiC GP. Select any `CustomerNo` from `CUSTNMBR` column and put it in the agent. 

- Open `Dynamics GP` with valid `Company Name`, `UserId` and `Password`. From the dashboard navigate to `Sales -> Cards -> Customer`. 
As the Customer Maintenance dialog box opens up, click on the lookup icon beside the Customer Id text box. 
The `Customers and Prospects` opens up, showing you all the customers that are currently available in the application along with the Customer Id. 
Click on any `Customer Id` and the details will be available. 

**Issue 3 :** Sometimes validation fails due to improper working of `eConnect service`. To check the same, you need a tool
`XmlDocumentSender`. Open `XmlDocumentSender`, a `eConnect Document Sending Utility` dialog box appears, configure the following.

- Click on `Connection String`, provide the server name and database name in the dialog dox that appears up.
- Click on `Select XML file`, from the dialog box that appears select the xml file that allows customers to read by id. 
The xml structure to fetch a specific customer will appear under `XML Document`. Inside the xml structure, the node `INDEX1TO` and 
`INDEX1FROM` will let you specify the customer id that you want to fetch. Click on `Send XML`. The response will be displayed 
in the `Return Information`. According to the respone, you can identify the issue and take necessary action against it.
 
## Actions and its Filter Implementation 

While defining a connection to an API in `Dynamics GP`, you require clear understanding about the 
data requirements and endpoint configurations. To define the endpoint in APPSeCONNECT, you need Schemas and Actions. 
Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. 
Here, you can use `RQeConnectOutType` as action if you are using `eConnect service ` to send 
the request to respective application or several others approaches are also there to perform the same. 
![dynamic_action1](/staticfiles/connectors/media/application-connector/dynamic_action1.png)

Data is fetched from source application using APIs, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action filters defines the search criteria 
of the data. You can add these parameters in the `action filter` to define the search criteria. 

Suppose you need to fetch 10 customers from dynamic GP at a time. In this situation, you need to create a schema named as
`Customer` and action as `RQeConnectOutType`. Under this action, you should mention the filtering conditions 
as key value pairs. 
![dynamic_action2](/staticfiles/connectors/media/application-connector/dynamic_action2.png)

You need to mention `eConnectProcessInfo` and `eConnectOut` in the body as the filter respectively. 
Under `eConnectProcessInfo`, use the following as child conditions 

|Key|Value|
|---|---|
|Outgoing|TRUE|
|MessageID|Customer|

Under `eConnectOut`, use the following as child conditions 

|Key|Value|
|---|---|
|DOCTYPE|Customer|
|OUTPUTTYPE|2|
|FORLOAD|0|
|FORLIST|1|
|ACTION|0|
|ROWCOUNT|10|
|REMOVE|0|
|WhereClause|CREATDDT BETWEEN '~{CreatedDate}~' and '~{MaxDateLimit}~'|

**Note :** Similarly, for other APIs `Product`, `Orders`, `Shipment` etc. you should follow 
the above mentioned action filters and procedures to design, deploy and execute processflow such
that the data could be synced properly. 








