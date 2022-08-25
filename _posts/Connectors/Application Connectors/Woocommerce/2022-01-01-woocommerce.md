---
title: "WooCommerce"
toc: true
description: "Get to know how you can configure the agent for woocommerce"
keywords: "WooCommerce Configuration, Configuring the WooCommerce Adapter, Action Filter implementation for Data fetch from WooCommerce Application"
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "WooCommerce"
        weight: 7
        icon: fa fa-file-word-o
        identifier: woocommerceconnector
---

Application configuration is an integral activity prior to the process of integration. If your chosen application is WooCommerce, 
credentials need to be provided for validating the agent. Here you will find the detailed description on 
how to configure the agents for the application of WooCommerce, Troubleshooting issues and the attributes and actions.

WooCommerce is a REST Application which supports both the BASIC & OAuth 1.0 authentication. The Adapter of the application WooCommerce
provides the leverage to communicate and adapt with the AEC Portal. This section provides you the detailed process of validating
the credential of the application WooCommerce.

# Pre-requisites for WooCommerce Configuration 

1. Create an account in `WooCommerce` and Login into it. 
2. As `WooCommerce` is a cloud-based application, therefore it can be accessed through URL. The Base URL is your - `http://templatebar.com/dev/wordpress1/wp-admin`. 
3. **Username** and **Password** to access the application.  

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration).   

### Configuring the WooCommerce Application in On-Premise Agent

1. Open the agent and click the checkbox in Settings Panel.
2. [Create](/getting%20started/create-your-first-processflow/) and [Deploy](/processflow/deploying-and-executing-processflow/#deploying-processflows-to-environment) ProcessFlows in the cloud portal.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application. 

### Steps to Configure WooCommerce Credential in OP Agent

1.  The Base URL Endpoint has 2 options in the drop-down. 
a.	/wp-json/wc/ - This is the newer version of the WooCommerce that support the WordPress platform for WooCommerce. 
The version for this WooCommerce version should be >=2.6  
b.	/wc-api/ - This endpoint is for the older version of the WooCommerce platform. If the user platform is based on the older version, this end point is needed to be selected for agent validation.
The version for this WooCommerce version should be <2.6   
2. The API Version is the WooCommerce API Version. The user can have its WooCommerce Version by navigating to WooCommerce > Status > WooCommerce Version.
![woocommerce-adapter3](/staticfiles/connectors/media/application-connector/woocommerce-adapter3.png)
**Note : For more details about WC API versions, [click here](https://woocommerce.github.io/woocommerce-rest-api-docs/?javascript#introduction)**
3.	The check-box fields are the HTTP Headers that needs to be enabled if the http headers are required.    
![woocommerce-adapter4](/staticfiles/connectors/media/application-connector/woocommerce-adapter4.png)
4.  The Base URL is the WooCommerce Base URL. For Ex:http://templatebar.com/Individual/abcd/woocommerce  
**Note : If the URL has HTTP, the authentication OAuth 1.0 is supported and if the URL has HTTPS, the BASIC Authentication is supported. 
For both authentication process, the User Interface remains the same.**
5.	The API Key and the API Secret is generated from the WooCommerce platform. Navigate to WooCommerce > Settings > Advanced > REST API > ADD Key 
![woocommerce-adapter5](/staticfiles/connectors/media/application-connector/woocommerce-adapter5.png)
6.	Provide the details in the field provided in the WooCommerce platform and click on the Generate API Key Button.
a.	Description : This is the field for API Description.  
b.	User : This field is for specifying the User Type. The user should be as ADMIN   
c.	Permissions : This is a drop-down field; the permission should be selected as Read/Write for providing the permission for GET and CREATE operations.    
![woocommerce-adapter6](/staticfiles/connectors/media/application-connector/woocommerce-adapter6.png)  
7.	Input the generated API Key and the API Secret in the Agent.    
![woocommerce-adapter7](/staticfiles/connectors/media/application-connector/woocommerce-adapter7.png)  
**Note : The Consumer Key is the API Key and the Consumer Secret is the API Secret.**  
8.	In the App Configuration panel of the agent, click on the + button, beside the app WooCommerce.    
![woocommerce-adapter1](/staticfiles/connectors/media/application-connector/woocommerce-adapter1.png)
9.  On clicking the + button, the credential panel opens for the application WooCommerce.    
![woocommerce-adapter2](/staticfiles/connectors/media/application-connector/woocommerce-adapter2.png)
10.	Input the WooCommerce Username and Password in the Agent and click on the Validate and SAVE button.      
![woocommerce-adapter8](/staticfiles/connectors/media/application-connector/woocommerce-adapter8.png)

Following these steps, ends the process for validating agent for the application WooCommerce. 

## Cloud Agent Configuration 

### Configuring the WooCommerce Application in Cloud Agent

1. Login to `APPSeCONNECT` portal with valid credentials.   

2. Navigate to **Manage > App**. Expand the `WooCommerce` application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the necessary information `Credential Name`, `Base Url Endpoint`, `API Version`, `Base Url`, `API Key`, `API Secret`, `Username `and `Password`.  
![woocommercecloud](/staticfiles/connectors/media/application-connector/woocommercecloud.png)    

5. Click on Save and a toaster message will be displayed confirming the same. 

## Troubleshooting

**ISSUE 1 :  If the Source Application Not Found**

Some of the basic issue in processflow happens due to improper validations or even if it is accurately validated, this basic issue 
resolves after removing the Temp and Cache files from the portal and from your system. Therefore, after clearing all this re-deploy and execute the processflow on the agent. 
For E.g. If the Source Application Not Found in the log file appears, the probable cause is due to the presence of the Temp and Cache Files. 

**ISSUE 2 : Plugin Installation Issue**

On executing Customer Add processflow from WooCommerce to any destination application, it is noted that only 
first 10 customers created, successfully synced, but it fails or shows no result for rest of the customers. 
This is due to the plugin that might not have been installed. 

**Note : It is the feature in WooCommerce that without the AEC plugin, more than 10 customers will not sync**.

## Attributes and Actions

While defining a connection to an API endpoint in WooCommerce, you require clear understanding about the data requirements 
and endpoint configurations. You can refer to this document to find all the endpoint details of your WooCommerce installation.
 
To define the endpoint in APPSeCONNECT, you need Actions and Entities. Actions are specifically targeted for an endpoint 
while schema is the data needed to execute the API. Here, is the list of some of the pre-packaged API actions defined 
for you which you can easily plug and play while doing your integrations.

|Endpoint|Action|Action Type|Schema|UI Path|API Path|
|---|---|---|---|------|----|
|customers|Customers|GET|[Customers](https://portal.appseconnect.com/AppEntityAction?AppVersionId=cbc4737b-e610-4beb-835c-da5f59e6a5e2&entityId=61f33b9c-5087-4481-8e86-a8155be71c51&entityActionId=dde24ee9-0872-48f6-8593-8ca9ee6034f7&orgId=d21688a4-8967-48de-ae82-31dda565ec51)|[Fetch customers from WooCommerce and post it to the destination Application](https://learnwoo.com/woocommerce-create-new-user-account/)|[customers](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-customer)|
|orders|Orders|GET|[Orders](https://portal.appseconnect.com/AppEntityAction?AppVersionId=cbc4737b-e610-4beb-835c-da5f59e6a5e2&entityId=eecd4a6e-257e-4561-8f6d-c9ae13334ee4&entityActionId=b50f33bd-7843-4e5d-a7e2-07ec2f696d46&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False )|[Fetch the order from WooCommerce and post it to the destination Application](https://docs.woocommerce.com/document/managing-orders/)|[orders](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-an-order)|
|orders|ORDERS|POST|[Orders](https://portal.appseconnect.com/AppEntityAction?AppVersionId=cbc4737b-e610-4beb-835c-da5f59e6a5e2&entityId=eecd4a6e-257e-4561-8f6d-c9ae13334ee4&entityActionId=214fbbcb-91ab-417d-b576-f454517aee41&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False )|Post Invoices to WooCommerce from any Source Application|[orders](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-an-order)|
|products/productid|[Products](https://portal.appseconnect.com/AppEntityAction?AppVersionId=cbc4737b-e610-4beb-835c-da5f59e6a5e2&entityId=fcb096e1-4372-4aaf-a24a-29a4a174d4a4&entityActionId=9991a38f-2b00-4c4c-8ede-41febe22aac1&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False )|PUT|Products|Update Inventory in WooCommerce from Source Application|[products/productid](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-product)|
|products|Products|POST|[Products](https://portal.appseconnect.com/AppEntityAction?AppVersionId=cbc4737b-e610-4beb-835c-da5f59e6a5e2&entityId=fcb096e1-4372-4aaf-a24a-29a4a174d4a4&entityActionId=3ccaef9e-d9f0-41d0-ac2b-3f71ea9ede27&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False)|Post products in WooCommerce from any Source Application|[products](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-product)|

**Protip:** Customers and Orders can be created and placed from the Front-End also. For Placing orders from front end, visit the E-Commerce store and follow the generic steps for placing orders and creating customers.
this one.
{: .notice--info}

## Action Filter Implementation 

Data is fetched from source application using APIs, and as you are aware of, API provides filters which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action is generally defined as the endpoint of the application which is being fetched, while the filters define 
the search criteria of the data. 

1) In case of retrieving `Business Partner` from `Woocommerce` use the filters as provided below with `&&` operator.
![woocommerce_2](/staticfiles/connectors/media/application-connector/woocommerce_2.png) 

|Field Name|Filter|
|---|---|
|created_after|~{CreatedDate('yyyy-MM-dd'T'HH:mm:ss')}~|
|orderby|registered_date|
|per_page|50|
|page|1|
|role|all|

2) Use `last_update_after` as the key and `~{CreatedDate('yyyy-MM-dd'T'HH:mm:ss')}~` as its value, to fetch those business partners that have been updated as well as to fetch `Sales Order`from the source application.
![woocommerce_1](/staticfiles/connectors/media/application-connector/woocommerce_1.png)

3) Use `after` as the key and `~{ReadDateTime('yyyy-MM-dd'T'HH:mm:ss')}~` as its value, to fetch `Products` from Woocommerce. 
![woocommerce_3](/staticfiles/connectors/media/application-connector/woocommerce_3.png)




