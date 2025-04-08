---
title: "Shopify using GraphQL"
toc: true
description: "configure agent for shopify GraphQL"
keywords: "creation of private app, shopify OP agent configuration, shopify Cloud agent configuration"
tag: developers
category: "Connectors"
menus: 
    shopifyconnector :
        title: "Shopify GraphQL"
        weight: 38
        icon: fa fa-file-word-o
        identifier: shopifygraphqlconnector
---

`Shopify` is a complete `ecommerce platform` that lets you start, grow, and manage a business. The adapter of the application Shopify provides 
the leverage to communicate and adapt with the AEC portal. This section provides you the detailed process of validating the credential of the 
application Shopify.

Application configuration is an integral activity prior to the process of integration. If your chosen application is `Shopify`, credentials 
need to be provided for validating the agent.  Here you will find the detailed description on how to configure the agents for the application
Shopify, Troubleshooting issues, the attributes and its action.    

## Pre-requisites for Shopify  Configuration 

1. Create an account in Shopify and Login into it. 
2. **Username** and **Password** to access the application.  
3. [Click here](https://shopify.dev/api/admin-graphql) to know the authentication mechanisn and endpoints of the application. 

### How you can create a Custom APP 

1. Login to your Shopify Application. Naviagte to `Apps` -> `Apps and sales channels settings` from the application admin page.
![shopifygraphql_4](/staticfiles/connectors/media/application-connector/shopifygraphql_4.png)   
2. Click on `Develop apps for your store` to create custom apps for your store.
![shopifygraphql_5](/staticfiles/connectors/media/application-connector/shopifygraphql_5.png)   
3. The `App Development` page will open up. You need to click on `Create an app` to create a custom app from scratch.  
![shopifygraphql_6](/staticfiles/connectors/media/application-connector/shopifygraphql_6.png)   
4. Provide a suitable `name` to your App and the `email id` will automatically be availbale as provided during login to the application. 
Click on `Create app` button at the bottom right corner of the dialog box. 
![shopifygraphql_7](/staticfiles/connectors/media/application-connector/shopifygraphql_7.png)
5. On clicking the `Create app` button, the app details page will appear. On clicking `Configure Admin API scope`, 
the `Admin API access scopes` will be open up. Provide the necessary access by clicking on the check-box and click on `Save`. 
![shopifygraphql_8](/staticfiles/connectors/media/application-connector/shopifygraphql_8.png)  
![shopifygraphql_9](/staticfiles/connectors/media/application-connector/shopifygraphql_9.png)   
6. On providing necessary accesses to you app, the `Install app` will be activated and click on the same to install the custom app 
in your store.
![shopifygraphql_10](/staticfiles/connectors/media/application-connector/shopifygraphql_10.png)
7. After installing the app successfully, the access token will be generated automatically. You will get the access token inside `API Credentials`.    
![shopifygraphql_11](/staticfiles/connectors/media/application-connector/shopifygraphql_11.png)

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration). 

### Configure the Shopify Application in the Agent

1. [Create a processflow](/getting%20started/create-your-first-processflow/) with Shopify as `source` or `destination` application, and [deploy](/processflow/deploying-and-executing-processflow/) the processflow in On-Premise agent.  
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure Shopify Credential in OP Agent

1. In the App Configuration panel of the agent, click on the `+` button, beside the app Shopify.     
![shopifygraphql_1](/staticfiles/connectors/media/application-connector/shopifygraphql_1.png)     
2. On clicking the `+` button, the credential panel opens for the application Shopify.    
Provide the `Base Url` and `Access Token` in the agent.    
3. After providing the credentials, click on `Validate` button. On successful validation, a message `Successfully Validated, now you can save this details.!!!` will be displayed. Click on `SAVE` to save the credentials.  
![shopifygraphql_20](/staticfiles/connectors/media/application-connector/shopifygraphql_20.png)   

Following this process, the `Shopify's GraphQL` application can be configured in the OP agent.    

## Cloud Agent Configuration 

### Configuring the Shopify GraphQL Application in Cloud Agent

1. Login to `APPSeCONNECT portal` with valid credentials.   

2. Navigate to **Manage > App**. Expand the `Shopify GraphQL` application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the necessary information `Credential Name`, `Bae Url` and `Access Token`.   
![shopifygraphql_19](/staticfiles/connectors/media/application-connector/shopifygraphql_19.png)    

5. On clicking `Validate` button, a message `Credentials validated successfully` will be displayed, if all credentials provided 
by you is correct. Finally, click on `Save` to save the credentials permanently.   

## Troubleshooting

Some of the basic troubleshooting issues happens due to improper validations or even if it is accurately validated, the processflow do not sync data properly. 
This basic issue resolves after removing the Temp and Cache files from the portal and from your system. 
Therefore after clearing all this, you need to [deploy and excute](/processflow/deploying-and-executing-processflow/) the processflow again to perform the required business integration in a smooth and free-flowing way. 
For E.g. If the `Source Application not Found` , remove the Temp and Cache Files. Again re-deploy and execute the processflow. 

While validating the credentials in the agent, it might happen that the `store name` used is not correct. Check it once again, from 
the application dashboard page and validate the same again. Other than this, you need to remember to install the created `custom app` 
else, the `Access Token` will not be generated.   

## Attributes and Actions

While defining a connection to a particular API endpoint in `Shopify GraphQL`, you require clear understanding about the data requirements 
and endpoint configurations. You can refer to this document to find all the endpoint details of your shopify installation. 
To define the endpoint in APPSeCONNECT you need to define Actions and Entities. Actions are specifically targetted for a particular 
endpoint while schema is the data needed to execute the API. Here are the list of some of the prepackaged API actions defined 
for you which you can easily plug and play while doing your integrations.

|Endpoint|Action|Action Type|Schema|Description|API Help|
|---|---|---|---|------|-----|
|customer|customers|GET|customers|Fetches customers from Shopify|[customer](https://shopify.dev/api/admin-graphql/2022-10/queries/customer)|
|product|products|GET|products|Fetches products frrom Shopify|[product](https://shopify.dev/api/admin-graphql/2022-10/queries/product)|
|order|orders|GET|order|Returns a list of orders placed|[order](https://shopify.dev/api/admin-graphql/2022-10/queries/orders)|
|customerCreate|customerCreate|POST|customer|Creates a new customer|[customerCreate](https://shopify.dev/api/admin-graphql/2022-10/mutations/customerCreate)|
|inventory|inventoryItemUpdate|POST|inventory|Updates an inventory item|[inventoryItemUpdate](https://shopify.dev/api/admin-graphql/2022-10/mutations/inventoryItemUpdate)|    

### Action Filter Implementation 

Data is fetched from source application using APIs, and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add these parameters in the `action filter` to define the search criteria.   

### Filter while retrieving data from Shopify

While fetching data fom `Shopify GraphQL`, you need to mention the filters both in `Headers` and `Body` section. 
Let us consider any API of shopify such as `customer`, the request structure will look like :
```
query {
  customer(id: "gid://shopify/Customer/544365967") {
    id
    firstName
    lastName
    acceptsMarketing
    email
    phone
    ordersCount
    totalSpentV2 {
      amount
      currencyCode
    }
    averageOrderAmountV2 {
      amount
      currencyCode
    }
    createdAt
    updatedAt
    note
    verifiedEmail
    validEmailAddress
    tags
    lifetimeDuration
    defaultAddress {
      formattedArea
      address1
    }
    addresses {
      address1
    }
    addressesV2(first: 10) {
      edges {
        node {
          address1
        }
      }
    }
    image {
      src
    }
    canDelete
  }
}

```

Let us assume that, you need to retrieve `id`, `fiirstname`, `lastname` and `email` of first `5` customers from Shopify. 
To accomplish this scenerio, mention the following in the body section of action filter as the parent condition : 
- `first` as the `key` and any numerical value in the `value` field. 
- `select` as the `key` and mention the fields to be retrieved as values.
- `query` as the `Key` and the value field will be empty since this will have some more fields as child conditions. You need 
to mention a date time filter as well. Provide `updated_at` as the key and any specific value('2022-11-08T05:27:28Z') in the value 
field. Else, you can also use dynamic date time by `~{GetLastDate(-2)}~` appresource function. Instead of `2`, you can also 
use any integer value. This function will retrieve customer details from the database, but 2 days back from know. 
- Combine all the above conditions using `&&`. 
![shopifygraphql_13](/staticfiles/connectors/media/application-connector/shopifygraphql_13.png)   
![shopifygraphql_14](/staticfiles/connectors/media/application-connector/shopifygraphql_14.png)

You need to add one action filter in ‘Header’ section as well, for storing the latest date in the database 
from your input data along with that key must be there in the input data.   
![shopifygraphql_12](/staticfiles/connectors/media/application-connector/shopifygraphql_12.png)   

For Resync, you must configure the `Retry Filter`. In the `Retry Filter`, inside the body section, 
you need to pass with ‘select’ key and the values. Without retry filter, the Resync will not work. The values will be the fields 
that you want to retrieve from the API.
![shopifygraphql_15](/staticfiles/connectors/media/application-connector/shopifygraphql_15.PNG) 

You Custom Trace Conflict Bucket as mentioned above.   
![shopifygraphql_16](/staticfiles/connectors/media/application-connector/shopifygraphql_16.png)  

### Filters while posting data to Shopify 

You can also use `Shopify` as destination application to store data. While doing the same, you need to use some action filters in the 
body section of the destination application. Let us suppose that, you need to add some product information in `Shopify`, 
provide `$inputParams` as the key and the value fields corrosponding to `$inputParams` will remain blank. You need to use `$inputParams` 
as the key irrespective of the schema used as the destination. Refer to the [API](https://shopify.dev/api/admin-graphql/2022-10/mutations/productCreate) of 
`Shopify` to know the child condition that you need to mention `$inputParams`. 
To specify the fields that needs to be updated, mention `select` as the key and the 
field names as the value(you can provide title, id, createdAt and updatedAt fields and many more).

![shopifygraphql_18](/staticfiles/connectors/media/application-connector/shopifygraphql_18.png)  