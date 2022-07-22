---
title: "SAP Business One"
description: "Get to know how you can configure the agent for SAP Business One"
keywords: "SAP Business One  Configuration, Custom Database Type Selection"
toc: true
tag: developers
category: "Connectors"
menus:
    applicationconnector :
        title: "SAP Business One"
        weight: 12
        icon: fa fa-file-word-o
        identifier: sapb1connector
---

Application configuration is an integral activity prior to the process of integration. 
If your chosen application is SAP Business One, credentials need to be provided for 
validating the agent. Here you will find the detailed description on how to configure the agents for the 
application of SAP Business One, attributes, action and the Troubleshooting issues.

SAP Business One is an ERP software platform specifically intended for small and medium-size businesses. 
SAP Business One (also known as SAP B1) was designed with the idea that smaller companies need ERP software 
to help manage their business, but not the kind of ERP that large and complex organizations need. 
It has functional modules for finance, customer relationship management, warehousing and production management, 
purchasing and procurement, and reporting and analytics. 

**Note : This document is for the SAP Business One version >=8.8**

## Pre-requisites for SAP Business One  Configuration 

1. Create an account in SAP Business One and Login into it. 
2. **Username** and **Password** to access the application.  
3. You need to know the Authentication and APIs of the application.

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the SAP Business One Application in the Agent

1. [Create a processflow](/getting%20started/create-your-first-processflow/) with SAP Business One as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure the credentials in the Agent

1) Open APPSeCONNECT Agent by providing correct credentials.

2) In the **Apps Configurational panel** of the agent, you will be able to view the SAP Business One application. Click on the `+` icon to add the credential.   
![sapb1_agent](/staticfiles/connectors/media/application-connector/sapb1_agent.png)

3) Provide the credentials of SAP Business One application.
![sapb2_agent](/staticfiles/connectors/media/application-connector/sapb2_agent.png)

Under SAP Event XML file path & SAP Image file path, you need to create two folders respectively and link the path to it. 
This path later needs to be provided in SAP B1 as well.

**Follow the steps mentioned below, to provide SAP Event XML file path & SAP Image file path in SAP B1**

-  Open SAP B1 after providing valid credentials.
-  Navigate through Administrator > System Initialization > General Settings.
-  A form will open. Select "Path" menu under it. Browse for SAP Event XML file path and Image path.

![sapb1-agent4](/staticfiles/connectors/media/application-connector/sapb1-agent4.png)

4) After providing all the credentials. Click "Save" button.

![sapb1_agent5](/staticfiles/connectors/media/application-connector/sapb5_agent.png)

A message "Connection Data Saved" will appear if all the credentials provided by you for SAP B1 is valid.

5) Click on the "Validate" button, to validate the connection.

![sapb1_agent6](/staticfiles/connectors/media/application-connector/sapb6_agent.png)

A message "Test Connection Successful" will appear if all the credentials provided by you for SAP B1 is valid. 
In this way, you can configure the credentials of SAP B1.

### Custom Database Type Selection

By default, the field for `Database Type` list the following types in its drop-down and they are :
- Hana Database
- Microsoft SQL Server 2000
- Microsoft SQL Server 2005
- Microsoft SQL Server 2008
- Microsoft SQL Server 2014
- Microsoft SQL Server 2016
- Microsoft SQL Server 2017
- Microsoft SQL Server 2019

SAP DIS adapter gives you the flexibility to create and support Custom database on its drop-down as per your requirement. Follow the below procedure to create custom database type.

1) Navigate to the APPSeCONNECT Folder, where your APPSeCONNECT OP Agent is downloaded.

2) Navigate to APPSeCONNECT > Adapter > BoDataServerTypes. 

3) Open the file **BoDataServerTypes** with NOTEPAD, available inside the **Adapter** folder. You can view the XML structure that defines all the default database types.

![sapdbtype1](/staticfiles/connectors/media/application-connector/sapdbtype1.PNG)

4) At the bottom of the file, add the syntax for adding a new database type.

![sapdbtype2](/staticfiles/connectors/media/application-connector/sapdbtype2.PNG)

While Adding make sure, the On-Premise Agent is closed & and Enable Environment is off.

5) The file would look as given below.

![sapdbtype3](/staticfiles/connectors/media/application-connector/sapdbtype3.PNG)

7) Restart your On-Premise Agent and check for the database type drop-down list. You should have the the added database type in the list.

![sapdbtype4](/staticfiles/connectors/media/application-connector\sapdbtype4.PNG)

Following the above process, you can successfully add your custom database type for your application SAP DIS.

**Note :** Adding custom database type requires ADMINISTRATOR permission. Incase, your system user profile does not have the admin permission, you need to manually provide the admin permission both in the **ADAPTER** folder and the **BoDataServerTypes** file.

## Troubleshooting

**Issue 1 : Source Application Data Not Found even if Data is present is the Source Application**

Some of the basic troubleshooting issue happens due to improper validations or even if it is 
accurately validated, the processflows do not sync. This basic issue resolves after removing 
the `Temp and Cache files` from the `portal` and from your `system`. Therefore after clearing all
this, you need to re-deploy and execute the processflow again.

For Example, if the "Source Application Data Not Found" in the log file appears, the probable cause is due 
to the presence of the Temp and Cache Files.

**Issue 2 : Syncing issues**

While working with SAP B1 Integrations, SAP Business One DI Server ON/OFF is needed to be done for proper 
syncing else data will not sync to SAP. 

## Attributes and Actions

While defining a connection to an API in SAP Business One, you require clear understanding about the 
data requirements and endpoint configurations. You can refer to this document to find all the endpoint 
details of your SAP Business One installation. To define the endpoint in APPSeCONNECT, you need Schemas and Actions. 
Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. 
Here, is the list of some of the pre-packaged API actions defined for you which you can easily plug and play 
while doing your integrations.

SAP Business One being a SOAP based application, it has objects that are used for pushing and pulling the data. 
[Click here](https://blogs.sap.com/2017/04/27/list-of-object-types/) to know about the `Object Code ID, its Primary Key and the related Table in SAP` that would be required for the Integration. 

|Endpoint|Action|Action Type|Schema|UI Path|API Path|
|---|---|---|---|------|---|
|ExecuteSQL|ExecuteSQL|GET|oBusinessPartners|[Fetch business partners from SAP Business One](https://help.sap.com/docs/SAP_BUSINESS_ONE/68a2e87fb29941b5bf959a184d9c6727/44f3e8afc4b80486e10000000a155369.html)|-|
|ExecuteSQL|ExecuteSQL|GET|oItems|[Fetch Products from SAP Business One to destination Application](https://help.sap.com/saphelp_sbo900/helpdata/en/45/2365ca9e152b31e10000000a1553f7/content.htm?no_cache=true)|-|
|AddObject|AddObject|POST|oBusinessPartners|Post employees from Source Application to SAP Business One|-|
|AddObject|AddObject|POST|oorders|Post order from any other application to destination application|-|

### Action Filter Implementation 


Data is fetched from source application using APIs, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add these parameters in the `action filter` to define the search criteria. 

In SAP Business One, a database is maintained containing various tables. Each such table contains information regarding Business Partners, Products, Orders, 
Quotations and many more. To know the details regarding the database tables, [click here](https://blogs.sap.com/2017/04/27/list-of-object-types/).

- General filters : It represents the overall filter criteria of the API. To define such filters, you do not need to 
specify anything special, just putting `DoQuery` in the key field and the query to fetch the data in the value field is fine. 

- In SAP Business One, Product created from the `UI` of the application are stored in the `OITM` table in the database. Suppose you need to retrieve 
50 products from SAP Business One. `OITM` table in SAP Business One contains various columns such as ItemCode, ItemName etc. You need to provide `DoQuery` in the key field and 
`Select Top 50 ItemCode,ItemName,UserText,U_WebID,OnHand from OITM where ISNULL(U_WitmFlag,'')='F' and isnull(U_WebID,'')=''` in the key field. In the select query,
    - ItemCode, ItemName, UserText, U_WebID and OnHand are the fields that you need to fetch from the application. 
    - 50 is the quantity that you need to fetch.
    - `where` is mentioned as filtering condition. Products having `U_WebID` as empty and if `U_WitmFlag` has some value, those products will be fetched.
                    

![sap_actionfilter](/staticfiles/connectors/media/application-connector/sap_actionfilter.png)


 