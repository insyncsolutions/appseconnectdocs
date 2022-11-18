---
title: "CommerceTools"
toc: true
description: "Get to know about commercetools credential validation, APIs and Action filter."
keywords: "pre-requisites for commercetools configuration, configure the commercetools application in op agent, configure the application in cloud agent"
tag: developers
category: "Connectors"
menus: 
    applicationconnector : 
        icon: fa fa-gg
        weight: 36
        title: "CommerceTools"
        identifier: commercetoolsconnector
---

`commercetools` is a `e-commerce platform`, which describes separating the frontend and backend layers of any application 
and having them communicate with each other via an `API`. Its flexible API also enables businesses to engage with their 
consumers through `mobile apps`, `business websites`, `social network` and many more. Therefore, the implementation 
and hosting of your online store are under your control.    

## Why do retailers choose commercetools?

- **Personalisation** - With `commercetools`, you are independent of the program that prescribes how a frontend 
should be organized. You don’t have to stick to a specific templating system, train your staff to follow the exact 
rules laid by the software vendor. Users can then fully control what happens in the frontend and shape your brand 
recognition without adhering to a templated layout, which certainly doesn’t make your website and app stand out from the crowd.    

- **Scalability** - Usually, the `frontend` and `backend` are individually scaled. As they are loosely coupled, 
the backend will not be affected even if the frontend receives a huge amount of traffic. As a result, the software 
helps businesses change and grow in order to meet their upcoming demand.     

- **Promptness** - Having the freedom to experiment yourself, you can implement `new user interfaces` faster without having to 
install and maintain full-stack software. Development becomes much more efficient since teams can work in parallel. 
By using commercetools, you’ll be able to save more time and optimize the developing process.     

As `APPSeCONNECT` is a Business Process Automation tool, this will allow you to develop and configure seamless integration between business applications. 
Therefore, application configuration is a fundamental activity prior to the process of integration. If your chosen application is 
`commercetools`, credentials need to be provided for validating the agent both in case of `OP` agent. Here you will find the detailed description on 
how to configure the agent for `commercetools`, troubleshooting issues, action and its filters.  

## Pre-requisites for Commercetools Configuration 

1) Create an account in [commercetools](https://docs.commercetools.com/merchant-center/accounts) with necessary credentials according to the region of your business.   
2) `API URL`, `Client ID`, `Client Secret`, `Scope` and `Auth Token Url` should be availbale.        
3) You need to know the [authorization mechanism](https://docs.commercetools.com/api/authorization) and [different APIs](https://docs.commercetools.com/api/projects/products) of the application along with their structures.       

### How to create API Client?

1) Login to `commercetools` application with valid credentials. From the dashboard, navigate to `Settings` -> `Developer Settings`. 
Click on `create new API Client`. Provide the name of the `API Client` and select `Scope` as `Admin Client`. Finally, click on `create API Client`. 
The `API Client details` will be displayed to you and save the credentials for future use. You will get the `Client Id`, `secret` and `scope` from the `API Client details` page.     
![commercetools3](/staticfiles/connectors/media/application-connector/commercetools3.png)

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Commercetools Application in OP Agent

1) [Create a processflow](/getting%20started/create-your-first-processflow/) with `commercetools` as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2) Open the agent and click the checkbox in Settings Panel.  
3) Move into the App Configurational Panel of the agent and configure the details of the respective application. 

### Steps to Configure the credentials in OP Agent

1) Open the OP Agent by providing correct credentials.   
2) In the App Configurations panel of the agent, click on the `+` button, beside the application `commercetools`. 
The credential panel opens for the application. 
![commercetools1](/staticfiles/connectors/media/application-connector/commercetools1.png) 

3) Enter `API URL`, `Client ID`, `Client Secret`, `Scope` and `Auth Token Url`at the required place. When logged in 
to `commercetools` application, the `API URL` will be displayed at the status bar depending on the region you have selected 
for your business. Here, the `API URL` will be `https://api.us-central1.gcp.commercetools.com/shubhendu/` and use 
the `Auth Token Url` as `https://auth.us-central1.gcp.commercetools.com/oauth/token`.
![commercetools5](/staticfiles/connectors/media/application-connector/commercetools5.png)

4) Click on the “Validate” button, to validate the connection. A message `Validation passed, now you can save these details` will appear 
if all the credentials provided by you for `commercetools` is valid. After validating the credentials, click “Save” button to save the credetials. 
Following the above processes, you can configure the `commercetools` application in the OP agent.  

## Cloud Agent Configuration 

### Configuring the Commercetools Application in Cloud Agent

1. Login to APPSeCONNECT portal with valid credentials.   

2. Navigate to **Manage > App**. Expand the commercetools application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the necessary information `API URL`, `Client ID`, `Client Secret`, `Scope` and `Auth Token Url`.    
![commercetools6](/staticfiles/connectors/media/application-connector/commercetools6.png)    

5. On clicking the validate button, the credentials will be validated provided by you. You can save the credentials by clicking `Save` button.  

## Troubleshooting

**ISSUE 1 :** You should specify the `API URL` according to the region your business belongs. Find the [region](https://docs.commercetools.com/api/authorization#requesting-an-access-token-using-the-composable-commerce-oauth-20-service) and select the 
`API URL` accordingly. 

**ISSUE 2 : Agent Validation may fail due to Client ID, Client Secret and Scope provided in the agent**

While validating the credentials in the agent, sometimes the validation fails due to improper 
`Client ID`, `Client Secret` and `Scope`. Check the credentials once again and re-Validate the credentials.       

## Attributes and Actions

While defining a connection to an API in `commercetools`, you require clear understanding about the data requirements and endpoint configurations. 
You can refer to this document to find all the endpoint details of `commercetools` application. To define the endpoint in `APPSeCONNECT`, you need 
to define Schemas and Actions. Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. Here is the 
list of some of the `pre-packaged API` actions defined for you which you can easily plug and play while doing your integration.

You can refer to [commercetools](https://docs.commercetools.com/api/authorization) to know the authuorization and [APIs](https://docs.commercetools.com/api/projects/products) in details.    

|Endpoint|Action|Action Type|Schema|UI Help|API Path|
|---|---|---|---|------|-----|
|customers|customers|GET|customers|Customers represent data about a specific customer in your project.|[Customers](https://docs.commercetools.com/api/projects/customers)| 
|Order|Order|GET|Order|You can view all orders presented by particular customers.|[Order](https://docs.commercetools.com/api/projects/orders)|
|ProductTypes|ProductTypes|GET|ProductTypes|Product Types are used to describe common characteristics, most importantly common custom Attributes.|[ProductTypes](https://docs.commercetools.com/api/projects/productTypes)|
|TaxCategory|TaxCategory|GET|TaxCategory|Tax Categories define how Products are to be taxed in different countries.|[TaxCategory](https://docs.commercetools.com/api/projects/taxCategories)|

### Action Filter Implementation 

Data is fetched from source application using `APIs`, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add any parameters in the `action filter` to define the search criteria. 
The parameters are added in the body section of the action filter. We shall look into, how 
you can provide the action filter. 

Let us consider, you want to retrieve customers created from `commercetools`. While doing that, you may use `createdAt` as the key 
and `~{CreatedDate}~` as the value to retrieve them using date filter. To restrict the number of custumers at a particular retrival, 
you can use `limit` as the key and integer value in the field. Apart from these you may the following as `key-value pair`, 
`lastModifiedAt` and `2022-09-20T14:42:47.438Z'.
![commercetools4](/staticfiles/connectors/media/application-connector/commercetools4.png)
