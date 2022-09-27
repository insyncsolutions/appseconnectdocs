---
title: "Dynamics 365 Business Central"
toc: true
tag: developers
category: "Connectors"
menus: 
    navbusinesscentralconnector:
        title: "Dynamics 365 Business Central"
        weight: 6
        icon: fa fa-file-word-o
        identifier: navbusinesscentralconnectorcloud
---
## Introduction
 
`Business Central` is a business management solution for managing your business for various sized organizations that automates and streamlines business processes. Companies can eventually add functionalities which is relevant to the domain of operations, and can customized to support even highly specialized industries. Business Central provides solutions to the companies to manage their business, including finance, manufacturing, sales, shipping, project management, services, and many more with its highly adaptable and rich features. 
 
`Business Central` is fast and easy to implement and configure, and its simplicity guides to innovate product design, development, implementation and usability. 
 
## Pre-requisite of Business Central
 
* Valid credential of Business Central account.
* You should have extension installation permission


## Installing the extension

Navigate to https://dynamics.microsoft.com/en-us/business-central/signin/  for Sign in to Dynamics 365 Business Central with a valid credential. New users may apply for new account. 

Navigate to Setup & Extensions > Extensions > Manage > Upload Extension. 

 ![BusinessCentralUploadExtension](/staticfiles/connectors/media/application-connector/BusinessCentralUploadExtension.png)

Browse and upload the .app file from the folder location. You may choose the current version and language to for the deployment. Activate Accept to enable the deployment of the extension. 

During deployment of the extension, you may check the status of the deployment. For that choose Deployment Status and then view the status of the extension deployment. Navigate to the row to view additional details. 
In the deployment status details you can reach out to Refresh button in the actions from where you may retrieve the most recent status and details. 

After successfully deployment of the .app extension, choose the Refresh button to see the new extensions in the list of installed extensions. 

## Web services exposed

To reach the Web Services List, enter “Web Services” in the search section of the top menu bar and select the Web services option. 
![MenuWebServices](/staticfiles/connectors/media/application-connector/MenuWebServices.png)
The list will guide you about the fields of the web services like Object Name, Object Id, Service Name, Published Mode etc, while calling the web services from the different applications. Keep the format as mentioned in the list. 

|Object ID|Object Name|Sevice Name|Published|Details|
|---|---|---|---|------|
|55000|AEC Application|aecapp|Yes|used to create different type of Application Details|
|55001|AEC Application Item|aecappitems|Yes|used to create Web related application specific Item Details data during Item creation|
|55002|AEC ShipInv Sync|aecshipinvsync|Yes|used to create Web related application specific Customer Shipping Invoice Details data while generating Shipping Invoice|
|55003|AEC Application Customer|aecappcustomer|Yes|used to create Web related application specific Customer Details data during Customer creation|
|55004|AEC Order Header|aecorderheader|Yes|used to create Web related application specific Order Details data during Oder creation|
|55004|AEC Order Header|aecsalesorderheader |Yes|used to create Web related application specific Sales Order Details data during Sales Order creation|
|55005|AEC Order Header Cart|Aecsalesorderheadercarts|Yes|used to create Web related application specific Sales Order Cart Details data during Order Cart creation|
|55007|AEC SalesOrder Header|Aecsalesorderheaders |Yes|used to create Web related application specific Sales Order Details data during Sales Order creation|
|550012|AEC Order Lines|aecorderlines|Yes|used to create Web related application specific Order Item Lines Details data during Order creation|
|550013|AEC Shipment Lines|aecshipmentlines|Yes|used to create Web related application specific Order Shipment Lines Details data during Order Shipping|
|550016|AEC Item LocationInventory|aecitemlocationinventory|Yes|used to store Web related application specific Item Location Inventory Details data while generating Item Inventory|
|550021|AEC Child Details|aecchilddetails|Yes|used to store Web related application specific Child Details data|

## Troubleshooting

We haven't identified any troubleshooting steps till date. But if you face any issues with the APIs, feel free to comment here or else add a Support Ticket. 

## How you can configure Basic Authentication in Dynamics 365 Business Central for On-Premise Agent?

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration).   

### Configuring Dynamics 365 Business Central

1. [Create](/getting%20started/create-your-first-processflow/) and [Deploy](/processflow/deploying-and-executing-processflow/#deploying-processflows-to-environment) ProcessFlows in the cloud portal. 
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Dynamics 365 Business Central Application

1. In the App Configurations panel of the agent, click on the + button, beside the app `Dynamics 365 Business Central`. The credentials panel opens for the application `Dynamics 365 Business Central`. 
![dynamics365basicopagent1](/staticfiles/connectors/media/application-connector/dynamics365basicopagent1.png)    
2. Select the `Authentication` type from the drop-down as `Basic` and enter the value for `API Path`, `User Name` and `Web Service Access Key`. 
Click on Validate Button. A success message will be displayed if the credentials are validated properly. Finally, click on `SAVE`.    
![dynamics365basicopagent2](/staticfiles/connectors/media/application-connector/dynamics365basicopagent2.png)   
Following this process, the Dynamics 365 Business Central can be configured in the OP agent. 

### Cloud Agent Configuration 

### Configure the Dynamics 365 Business Central Application in Cloud Agent

1. Login to `APPSeCONNECT` portal with valid credentials.   

2. Navigate to **Manage > App**. Expand the Dynamics 365 Business Central application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the necessary information `Credential Name`, `AuthType`, `API Path`, `User Name` and `Web Service Access Key`.   
![dynamics365basicloud](/staticfiles/connectors/media/application-connector/dynamics365basiccloud.png)    

5. On clicking `Validate`, a success mesaage will be displayed, if all the credentials provided 
are correct. Finally, click on `Save`, a toaster message will be displayed confirming the same.  

## How you can configure Outh2.0 Authentication in Dynamics 365 Business Central for On-Premise Agent?

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration).   

### Configuring Dynamics 365 Business Central

1. [Create](/getting%20started/create-your-first-processflow/) and [Deploy](/processflow/deploying-and-executing-processflow/#deploying-processflows-to-environment) ProcessFlows in the cloud portal. 
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Dynamics 365 Business Central Application

1. In the App Configurations panel of the agent, click on the + button, beside the app `Dynamics 365 Business Central`. The credentials panel opens for the application `Dynamics 365 Business Central`. 
![dynamics365basicopagent1](/staticfiles/connectors/media/application-connector/dynamics365basicopagent1.png)    
2. Select the `Auth` type from the drop-down as `OAuth2.0`and enter the value for `API Path`. 
Click on Authorize Button. A custom browser opens for validating your chosen application. You need to provide 
any user login credential of `Dynamics 365 Business Central`. Immediately, `portal.appseconnect.com` appears and 
the credentials in the `OP` agent gets validated and saved. 
![dynamics365outh2opagent2](/staticfiles/connectors/media/application-connector/dynamics365outh2opagent2.png)   
Following this process, you can configure Dynamics 365 Business Central using `Outh2.0` authentication in the OP agent. 

### Cloud Agent Configuration 

### Configure the Dynamics 365 Business Central Application in Cloud Agent

1. Login to `APPSeCONNECT` portal with valid credentials.   

2. Navigate to **Manage > App**. Expand the Dynamics 365 Business Central application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the `Credential Name`, select `AuthType` as `Outh 2.0` and `API Path`. In case of `Outh 2.0`, no need to specify any value for 
`UserName` and `Web Service Acess Key`. However, `UserName` and `Web Service Acess Key` will contain some default values. 
![dynamics365outh2cloud](/staticfiles/connectors/media/application-connector/dynamics365outh2cloud.png)    

5. On clicking `Grant`, a custom browser opens for validating your chosen application. You need to provide 
any user login credential of `Dynamics 365 Business Central`. Immediately, `portal.appseconnect.com` appears and 
your credentials gets validated. Follow the above procedures to validate your credtials for `Outh 2.0` in cloud. 

## How to get the API Path?

You need to login to `Dynamics 365 Business Central` account with valid credentials. From the `Home` page, 
navigate to `Web Services List` page. Consider any `Web Services` from the list, the data present under the column 
`OData V4 URL`, will be your `API Path` except the service name.  

## How to get User Name and Web Service Access Key?

Login to `Dynamics 365 Business Central` account with valid credentials. From the `Home` page, click on the three 
ellipses. You will be navigated to `Business Manager Evaluation` page, click on `Explore more roles`.
![dynamics365_un1](/staticfiles/connectors/media/application-connector/dynamics365_un1.png) 
![dynamics365_un2](/staticfiles/connectors/media/application-connector/dynamics365_un2.png) 

Under `System Administration`, expand `Users`. Several users that have already been created will be visible, 
expand any one of them. While expanding any user, the `User Name` and `Web Service Access Key` will be visible, 
copy them and use these credentials in the agent.
![dynamics365_un3](/staticfiles/connectors/media/application-connector/dynamics365_un3.png) 

> Login user should have execute permission for table, page and API.  