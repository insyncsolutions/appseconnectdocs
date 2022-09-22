---
title: "Big Commerce"
description: "Get to know how you can configure the agent for Big Commerce"
keywords: "Big Commerce Configuration, Configure the Big Commerce Application"
toc: true
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "Big Commerce"
        weight: 29
        icon: fa fa-file-word-o
        identifier: bigcommerceconnector
---

`BigCommerce` is an e-commerce solution for small and medium businesses. With BigCommerce you can 
quickly and easily create an online store where you can sell products, process and ship orders, 
manage stock as well as customize the design of your store. 
`BigCommerce` offers a series of very attractive advantages for anyone who has an e-commerce store. 

## Benefits of using BigCommerce

- Customer Service
- Content Syndication
- Online Marketing Apps
- Stock and returns management
- Fully adapted to mobile devices

As `APPSeCONNECT` is a Business Process Automation tool, this will allow you to develop and configure seamless integration between business applications. 
Therefore, application configuration is a fundamental activity prior to the process of integration. If your chosen application is 
`Big Commerce`, credentials need to be provided for validating the agent both in case of `OP` agent. Here you will find the detailed description on 
how to configure the agents for the application `Big Commerce`, troubleshooting issues, action and its filters. 

## Pre-requisites for Big Commerce Configuration 

1) Create a developer account in [Big Commerce](https://www.bigcommerce.com/start-your-trial/?_gl=1*1cs9u29*_ga*NTkyNDI0NDY2LjE2NjM4MjI3OTg.*_ga_WS2VZYPC6G*MTY2MzgzMDIzNi4zLjEuMTY2MzgzMDI0NC41Mi4wLjA.&_ga=2.268002190.1445483873.1663822798-592424466.1663822798) with necessary credentials.   
2) [Click here](https://developer.bigcommerce.com/docs/ZG9jOjIyMDYwNw-authentication) to know the authentication and different APIs of the application along with their structures.       
3) `API Path`, `Username` and `API Token` are required to configure the agent.

### How to create API Account and retrieve API Path, Username and API Token

1) Log in to your `Big Commerce` application with valid credentials. From the dashboard, navigate to 
`Settings` -> `API` -> `API accounts`. From `API accounts` page, click on `Create API account` on the top right corner. 
![bigcommerce_createaccount](/staticfiles/connectors/media/application-connector/bigcommerce_createaccount.png)

2) Enter the `Name` and provide the necessary permissions by selecting `read-only` or `modify`. Click on `Save` and 
you will be provided with `Client ID`, `Client Secret` and `API Token`. 

>Keep a note of these credentials as these will be used in the agent configuration.

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Big Commerce Application in OP Agent

1) [Create a processflow](/getting%20started/create-your-first-processflow/) with big commerce as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2) Open the agent and click the checkbox in Settings Panel.  
3) Move into the App Configurational Panel of the agent and configure the details of the respective application. 

### Steps to Configure the credentials in OP Agent

1) Open the OP Agent by providing correct credentials.   
2) In the App Configurations panel of the agent, click on the `+` button, beside the application bigcommerce. 
The credential panel opens for the application bigcommerce. 
![bigcommerce_opagent1](/staticfiles/connectors/media/application-connector/bigcommerce_opagent1.png) 

3) Enter `API Path`, `Username` and `API Token` at the required place. The `API Path` will be obtained while creating 
the `API Account`.
![bigcommerce_opagent2](/staticfiles/connectors/media/application-connector/bigcommerce_opagent2.png)

4) Click on the “Validate” button, to validate the connection. A message “Test Connection Successful” will appear 
if all the credentials provided by you for bigcommerce is valid. After providing all the credentials, click “Save” button. A message “Connection Data Saved” will appear 
if the required credentials are provided by you for `big commerce`.

Following the above processes, you can configure the BigCommerce application in the OP agent. 

## Troubleshooting

**ISSUE 1** 

Some of the basic troubleshooting issue happens due to improper validations or even if it is accurately validated but the 
processflows do not sync the data successfully. This basic issue resolves after removing the Temp and Cache files from the 
portal and from your system. Therefore, after clearing the Temp and Cache files, again deploy and execute your processflow.

For E.g. : If the Source Application Not Found appears in the log file, the probable cause is due to the presence of the 
Temp and Cache Files.

**ISSUE 2**

User validation may fail due to invaild API Path, Username and API Token. While validating the credentials in the agent, sometimes the validation fails due to improper 
API Path, Username and API Token. Check the credentials once again and re-Validate the credentials. 

## Attributes and Actions

While defining a connection to an API endpoint in `BigCommerce`, you require clear understanding about the data requirements 
and endpoint configurations. You can refer to this document to find all the endpoint details of your `BigCommerce` application. 
To define the endpoint in APPSeCONNECT you need Actions and Entities. Actions are specifically targeted for an endpoint 
while schema is the data needed to execute the API. Here, is the list of some of the pre-packaged API actions defined 
for you which you can easily plug and play while doing your integrations.

|Endpoint|Action|Action Type|Schema|API Path|
|------|---|---|---|----------|---|
|customers|customers|GET|customers|[Customers](https://developer.bigcommerce.com/docs/ZG9jOjIyMDYwNA-customers-and-subscribers#requests)|
|product|product|PUT|product|Inventory Update|
|order|orders|GET|order|[Orders](https://developer.bigcommerce.com/docs/ZG9jOjIyMDYxNg-orders-overview)|

### Action Filter Implementation 

Data is fetched from source application using APIs, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add these parameters in the `action filter` to define the search criteria. 

Let us consider the customer API of `BigCommerce` where your are going to fetch seevral such customers. 
Considering the customer API, use `min_date_created` as the key and `~{CreatedDate}~` as the value. 
Similarly, for action filter of other endpoints you should refer to the corrosponding API structure. 

![bigcommerce_actionfilter](/staticfiles/connectors/media/application-connector/bigcommerce_actionfilter.png) 