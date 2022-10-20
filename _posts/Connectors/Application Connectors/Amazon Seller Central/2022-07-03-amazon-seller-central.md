---
title: "Amazon Seller Central"
description: "Get to know how you can configure the agent for Amazon Seller Central, action and its filters."
keywords: "Amazon Seller Central Configuration, Amazon Seller Central  Application in OP Agent, Amazon Seller Central Application in Cloud Agent"
toc: true
tag: developers
category: "Connectors"
menus: 
    applicationconnector:
        title: "Amazon Seller Central"
        weight: 5
        icon: fa fa-file-word-o
        identifier: amazonsellercentralconnector
---

`Amazon Seller Central` is a platform offered by the world’s leading marketplace. Through this platform, a business 
can sell products online and have access to the millions of shoppers that use Amazon’s online marketplace. 
Seller Central allows business owners to become online retailers by using the platform’s 
e-commerce infrastructure and existing client base. 

## Benefits of Amazon Seller Central

- Open to anyone
- Control of the seller account
- Sell directly to Amazon’s customers
- Flexible logistical options
- Quick payment terms
- Platform’s large customer base

As `APPSeCONNECT` is a Business Process Automation tool, this will allow you to develop and configure seamless integration between business applications. 
Therefore, application configuration is a fundamental activity prior to the process of integration. If your chosen application is 
`Amazon Seller Central`, credentials need to be provided for validating the agent both in case of `OP` and `Cloud`. Here you will find the detailed description on 
how to configure the agents for the application `Amazon Seller Central`, Troubleshooting issues, action and its filters. 

![](https://www.youtube.com/watch?v=qpwNfUa-TMo)

## Pre-requisites for Amazon Seller Central Configuration 

1) Create an account in Amazon with necessary credentials. `Email Id` and `Password` are the manadatory details for logging in to the application.    
2) **Marketplace Website Url**, **Auth Url**, **Access Token Url**, **Aws Region** and **Aws MerchantId** to configure the application in the agent.    
3) [Click here](https://developer-docs.amazon.com/sp-api/docs/what-is-the-selling-partner-api) to know the Aws Region and APIs of the application. 

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Amazon Seller Central  Application in OP Agent

1) [Create a processflow](/getting%20started/create-your-first-processflow/) with Amazon Seller Central as source or destination application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2) Open the agent and click the checkbox in Settings Panel.  
3) Move into the App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure the credentials in OP Agent

1) Open the OP Agent by providing correct credentials.   
2) In the App Configurations panel of the agent, click on the `+` button, beside the application amazon seller central. 
The credential panel opens for the application amazon seller central. 
![amazonsellercentral_agentconfig](/staticfiles/connectors/media/application-connector/amazonsellercentral_agentconfig.png) 

3) Enter `Marketplace Website Url`, `Auth Url`, `Access Token Url`, `Aws Region` and `Aws MerchantId` at the required place. 
Here we are going to use    
**Marketplace Website Url** - https://sellingpartnerapi-na.amazon.com/   
**Auth Url** - https://sellercentral.amazon.com/apps/authorize/consent   
**Access Token Url** - https://api.amazon.com/auth/o2/token    
**Aws Region** - In this situation, `us-east-1` has been used as aws region. [Click here](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html) to get the details regarding the codes of other regions.   
**Aws MerchantId** - You need to mention the amazon Selling Partner Id. 
![amazonsellercentral_agentconfig1](/staticfiles/connectors/media/application-connector/amazonsellercentral_agentconfig1.png)

4) After providing the required details in all the fields, you need to click on `Authorize`, 
a web popup will open and you need to login with your Amazon Seller Central credentials. 
After successfully logging in, do not close the window. If all the process is successfully completed, 
the credentials will be saved automatically. However, if any error occurrs then you need to check the credentials 
that you have used in the OP agent and you need to Authorize again. 

Following the above processes, you can configure the amazon seller central application in the OP agent. 

## Cloud Agent Configuration 

### Configure the Amazon Seller Central Application in Cloud Agent

1) Login to `APPSeCONNECT` portal with valid credentials.   

2) Navigate to **Manage > App**. Expand the amazon seller central application and click on `Credential`. 

3) Expand the `REST` node, click on `Add New Credential`.  

4) Provide the necessary information `Marketplace Website Url`, `Auth Url`, `Access Token Url`, `Aws Region` and `Aws MerchantId`.  
![amazonsellercentral_cloud](/staticfiles/connectors/media/application-connector/amazonsellercentral_cloud.png)    

5) After providing the required details in all the fields, you need to click on `Grant`, 
a web popup will open and you need to login with your Amazon Seller Central credentials. 
After successfully logging in, do not close the window. If all the processes is successfully completed, 
the credentials will be saved automatically. However, if any error occurrs then you need to check the credentials 
that you have used in the cloud agent and you need to `Grant` again. 

6) Click on Save and a toaster message will be displayed confirming the same. 

## Troubleshooting

**ISSUE 1 : Agent Validation failed due to improper credential provided in the agent**

While validating the credentials in the agent, sometimes the validation fails due to improper 
`Marketplace Website Url`, `Auth Url`, `Access Token Url`, `Aws Region` or `Aws MerchantId`. 
Check the credentials once again and re-Authorize the credentials. 

**ISSUE 2 : Agent Validation failed due to improper credential provided in the Sign-Up process in Amazon Seller Central**

After putting the correct credentials in the agent, it may happen that you have entered wrong email-id and/or password in the 
sign-up process in amazon seller central application. Check the email-id and password and carry the validation process again. 

## Attributes and Actions

While defining a connection to an API in amazon seller central, you require clear understanding about the data requirements and endpoint configurations. 
You can refer to this document to find all the endpoint details of your amazon seller central application. To define the endpoint in APPSeCONNECT, you need 
to define Schemas and Actions. Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. Here is the 
list of some of the pre-packaged API actions defined for you which you can easily plug and play while doing your integration.

You can refer to [Amazon Seller Central](https://developer-docs.amazon.com/sp-api/docs/authorization-api-v1-reference) to know the authuorization and [APIs](https://developer-docs.amazon.com/sp-api/docs/orders-api-v0-reference) in details.  

|Endpoint|Action|Action Type|Schema|UI Help|API Path|
|---|---|---|---|------|-----|
|Product|/products/pricing/v0/price|GET|/products/pricing/v0/price|This will fetch product details.|[This will retrieve products](https://developer-docs.amazon.com/sp-api/docs/product-pricing-api-v0-reference)|
|order|/orders/v0/orders|GET|/orders/v0/orders|This will retrieve order that are currently available in amazon seller central.|[Fetching sales orders from Amazon Seller Central](https://developer-docs.amazon.com/sp-api/docs/orders-api-v0-reference)|

## Action Filter Implementation 

Data is fetched from source application using `APIs`, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add any parameters in the `action filter` to define the search criteria. 
The parameters can be added in the body and/or in the header section of the action filter. We shall be 
looking in both the scenerios of action filters. 

Let us consider that any user creates several orders in amazon seller central application. If you look at the API of amazon seller central application, such as `order` 
```json
{
  "payload": {
    "BuyerInfo": {},
    "AmazonOrderId": "026-1520163-6049104",
    "EarliestShipDate": "2022-03-10T00:00:00Z",
    "SalesChannel": "Amazon.co.uk",
    "AutomatedShippingSettings": {
      "HasAutomatedShippingSettings": false
    },
    "OrderStatus": "Canceled",
    "NumberOfItemsShipped": 0,
    "OrderType": "StandardOrder",
    "IsPremiumOrder": false,
    "IsPrime": false,
    "FulfillmentChannel": "MFN",
    "NumberOfItemsUnshipped": 0,
    "HasRegulatedItems": true,
    "IsReplacementOrder": false,
    "IsSoldByAB": false,
    "LatestShipDate": "2022-03-10T23:59:59Z",
    "ShipServiceLevel": "Std UK Dom_1",
    "IsISPU": false,
    "MarketplaceId": "A1F83G8C2ARO7P",
    "PurchaseDate": "2022-03-09T22:03:02Z",
    "IsAccessPointOrder": false,kh
    "IsBusinessOrder": false,
    "OrderTotal": {
      "CurrencyCode": "GBP",
      "Amount": "20.00"
    },
    "PaymentMethodDetails": [
      "Standard"
    ],
    "IsGlobalExpressEnabled": false,
    "LastUpdateDate": "2022-03-14T22:05:14Z",
    "ShipmentServiceLevelCategory": "Standard"
  }
}
```

You can retrieve the orders from the corrosponding API using the following filters under action in the body and/or in the header section. In this scenerio, let us assume that you are going to fetch several orders from amazon seller central. In the body of action filter, 
we will be using `MarketplaceIds` as the key and the `ATVPDKIKXODER` in the value field to determine specific customers from the platform. Along with the previous filter, we will be using `CreatedAfter` as the key and 
`~{LastOrderDate}~` as the value. ~{LastOrderDate}~ enables you to fetch orders on or after the last executed date. 
![amazonsellercentral_actionfilter](/staticfiles/connectors/media/application-connector/amazonsellercentral_actionfilter.png)

However, apart from the above filters you can use `TokenBased` as the key and `NextToken` as the value in the header section of the action filter. Since amazon seller central 
returns 100 order at time, so whenever a order request is made to the API during its response it will send you a token which will be forwarded to the API during its next request such that 
the order are fetched after the last order.
