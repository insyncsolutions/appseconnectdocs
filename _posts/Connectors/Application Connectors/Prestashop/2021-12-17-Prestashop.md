---
title: "Prestashop"
toc: true
description: "Get to know how you can configure the agent for Prestashop"
keywords: "Prestashop Configuration, Configuring the Prestashop application, Action Filter implementation for Prestashop Application, Configure the Prestashop Application, Configuring the Prestashop Application in Cloud Agent"
tag: developers
category: "Connectors"
menus: 
    applicationconnector : 
        icon: fa fa-gg
        weight: 11
        title: "Prestashop"
        identifier: prestashopconnector
---

Application configuration is an integral activity prior to the process of integration. If your chosen application is Prestashop, credentials 
need to be provided for validating the agent.  Here you will find the detailed description on how to configure the agents for the application
Prestashop, Troubleshooting issues, the attributes and its action.

Prestashop is a REST (CRUD type) application which supports the Webservices authentication. The adapter of the application Prestashop provides 
the leverage to communicate and adapt with the AEC Portal. This section provides you the detailed process of validating the credential of the 
application Prestashop.

# Pre-requisites for Prestashop Configuration 

1. Create an account in Prestashop and Login into it. 
2. **Username** and **Password** to access the application.  
3. [Click here](https://devdocs.prestashop.com/1.7/webservice/getting-started/) to know the APIs of the application.

## On-Premise Agent Configuration 

### Installation of On-Premise Agent

You need to install the agent on your local server. To Know about On-Premise Agent Configuration, [Click here](/deployment/Deployment-Configuration/#on-premise-agent-configuration).   

### Configure the Prestashop Application in the Agent

1. [Create](/getting%20started/create-your-first-processflow/) and [Deploy](/processflow/deploying-and-executing-processflow/#deploying-processflows-to-environment) ProcessFlows in the cloud portal. 
2. Open the agent and click the checkbox in Settings Panel.  
3. Move into the  App Configurational Panel of the agent and configure the details of the respective application.  

### Steps to Configure Prestashop Credential in OP Agent

1. In the App Configuration panel of the agent, click on the + button, beside the app Prestashop.  
![prestashop1](/staticfiles/connectors/media/application-connector/prestashop1.png)     
2. On clicking the + button, the credential panel opens for the application Prestashop.   
![prestashop2](/staticfiles/connectors/media/application-connector/prestashop2.png)    
3. Prestashop users can fetch the webservice key from Prestashop portal only.   
   Navigate to Advanced Parameters > Webservice > Key. For more details related to webservice, [click here](https://devdocs.prestashop.com/1.7/development/webservice/).    
![prestashop3](/staticfiles/connectors/media/application-connector/prestashop3.png)    
**Note : `Web Id Prefix` is an optional field. However, user can provide the detail as per the requirements.**  
4. Web Id Prefix is generally used when the Prestashop is having multiple Store in the same installation. 
   The prefix of the respective store is provided in the Web Id Prefix to segregate the data coming from multiple stores.
5. After providing the credentials, click on `Validate` button followed by `SAVE`.  
![prestashop4](/staticfiles/connectors/media/application-connector/prestashop4.png)    

Following the above process, the Prestashop application can be configured in the OP agent.

## Cloud Agent Configuration 

### Configuring the Prestashop Application in Cloud Agent

1. Login to APPSeCONNECT portal with valid credentials.   

2. Navigate to **Manage > App**. Expand the Prestashop application and click on `Credential`. 

3. Expand the `REST` node, click on `Add New Credential`.  

4. Provide the necessary information `Credential Name`, `Base Url`, `Web Service User ID`, `WebService Account Key`, `Web Id Prefix` and `Inline Authentication`.  
![prestashop_cloud](/staticfiles/connectors/media/application-connector/prestashop_cloud.png)    

5. Click on Save and a toaster message will be displayed confirming the same.

## Troubleshooting

**ISSUE 1 : Cannot POST data, Source application returned False**

`Cannot POST data, Source application returned False` even if Data is present in the Source Application (Prestashop).

Some of the basic troubleshooting issue happens due to improper validations. In this case, check for the proper validations of the credential 
for the source application adapter. Also, try deleting the Temp and Cache files from the portal and the system, and try validating the adapter again. 
Once validated, re-deploy and execute the processflow for its successful execution.

## Attributes and Actions

While defining a connection to an API in Prestashop, you require clear understanding about the data requirements and endpoint configurations. 
You can refer to this document to find all the endpoint details of your Prestashop installation. To define the endpoint in APPSeCONNECT, you need 
to define Schemas and Actions. Actions are specifically targeted for an endpoint while schema is the data needed to execute the API. Here is the 
list of some of the pre-packaged API actions defined for you which you can easily plug and play while doing your integration.

Prestashop has a generic [API Document](https://devdocs.prestashop.com/1.7/development/webservice/) and [Authentication](https://www.postman.com/binshops/workspace/binshops-public-workspace/folder/1491681-d7d64c08-e5dc-4b93-8f01-61fa88d6096d?ctx=documentation) following the CRUD type REST API protocols. 

|Endpoint|Action|Action Type|Schema|UI Help|API Help|
|---|---|---|---|-----|-----|
|customers|customers|GET|[Customer](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3d71faa24b-4ecd-4fa9-b2dd-f42cd0a04de5%26entityActionId%3d18d50f59-0f74-4e0a-8a33-e9ab25090f4b%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=71faa24b-4ecd-4fa9-b2dd-f42cd0a04de5&entityActionId=18d50f59-0f74-4e0a-8a33-e9ab25090f4b&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|[Fetching customers from Prestashop and posting it into Destination Application](http://doc.prestashop.com/display/PS14/Managing+Customers#ManagingCustomers)|[customer](https://www.postman.com/binshops/workspace/binshops-public-workspace/request/1491681-9b5e146e-f106-428d-b190-3acaee59f3bc)|
|addresses|addresses|GET|[address](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3d62606e78-cff8-4b33-9498-5aef4df43f19%26entityActionId%3d87be2f2f-aedc-4e4d-a696-604d9e8d26b7%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=62606e78-cff8-4b33-9498-5aef4df43f19&entityActionId=87be2f2f-aedc-4e4d-a696-604d9e8d26b7&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|[Fetching customer address from Prestashop and posting it into Destination Application](http://doc.prestashop.com/display/PS17/Customer+addresses)|[alladdresses](https://www.postman.com/binshops/workspace/binshops-public-workspace/request/1491681-93cac36b-f7d6-42ac-b645-00d4fe3fc962)|
|orders|orders|GET|[Order](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3dd14831fb-419e-47bb-8ead-19eadcbfd73b%26entityActionId%3d655ad116-e8d5-4619-9f4c-58060855b512%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=d14831fb-419e-47bb-8ead-19eadcbfd73b&entityActionId=655ad116-e8d5-4619-9f4c-58060855b512&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|[Fetching orders from Prestashop and posting it into Destination Application](http://doc.prestashop.com/display/PS17/Orders)|[orderhistrory](https://www.postman.com/binshops/workspace/binshops-public-workspace/request/1491681-c84fd961-05b4-41c2-9ced-c544f86db4a3)|
|order_invoices|order_invoices|GET|[order_invoices](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3d16224c0b-f158-40d4-bd0d-456c6f173a0a%26entityActionId%3dc4ad11f4-1043-4896-b642-589968ddb7d8%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=16224c0b-f158-40d4-bd0d-456c6f173a0a&entityActionId=c4ad11f4-1043-4896-b642-589968ddb7d8&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|[Fetching invoices from Prestashop and posting it into destination application](http://doc.prestashop.com/display/PS17/Invoices)|[order_invoices](https://devdocs.prestashop.com/1.7/webservice/resources/order_invoices/)|
|POST customers|POST customers|POST|[customer](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3d71faa24b-4ecd-4fa9-b2dd-f42cd0a04de5%26entityActionId%3da0cd83f3-0b02-49e5-8560-770665a40722%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=71faa24b-4ecd-4fa9-b2dd-f42cd0a04de5&entityActionId=a0cd83f3-0b02-49e5-8560-770665a40722&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|Posting customers from Source Application to Prestashop|[customer](https://www.postman.com/binshops/workspace/binshops-public-workspace/request/1491681-36de078a-f819-4439-be02-0623f522fec1)|
|POST products|POST products|POST|[product](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2fAppEntityAction%3fAppVersionId%3d2280f742-83d4-4605-acbd-c4246086fab5%26entityId%3d28e2659a-b7e3-4012-8645-6f31d7f4bbe7%26entityActionId%3dbbb46ef1-00df-4145-892b-9ade7b1f6eb3%26orgId%3dd21688a4-8967-48de-ae82-31dda565ec51%26IsFromPopup%3dFalse&AppVersionId=2280f742-83d4-4605-acbd-c4246086fab5&entityId=28e2659a-b7e3-4012-8645-6f31d7f4bbe7&entityActionId=bbb46ef1-00df-4145-892b-9ade7b1f6eb3&orgId=d21688a4-8967-48de-ae82-31dda565ec51&IsFromPopup=False#!)|Posting products from Source Application to Prestashop|[products](https://devdocs.prestashop.com/1.7/webservice/resources/products/)|

### Action Filter implementation 

Data is fetched from source application using [APIs](https://devdocs.prestashop.com/1.7/webservice/resources/), and as you are aware of, API provides filters 
which will allow you to specify a subset of data from the whole bunch of data created in the server, 
the same can be specified through Actions and Action filters. The Action generally defines the 
endpoint of the application which is being fetched, while the filters define the search criteria 
of the data. You can add these parameters in the `action filter` to define the search criteria. 

- The `display` parameter can be used to return all fields when used with the `full` value. 
You need to put the `display` parameter in the key field and `full` in the value field of the action filter as `display=full`. 
This will return all the fields of an endpoint that have been requested by you.  

- `display` parameter enables you to specify selected fields as per your requirement. 
Mention a list of field names in brackets as : `display=[id,lastname,firstname,phone_mobile]`. 
You need to mention the `display` parameter in the key field and `id,lastname,firstname` or any other field name in the value field of the action filter. 

- The `filter` parameter controls which items to be returned. You need to specify the field name in `[]`. 

  - The `EQUAL` operator is used when you need to get specific items. For example, if you want the addresses for customer #1, you can filter your GET request 
  with the filter parameter as `filter[id_customer]=1` where id_customer is a field of the addresses endpoint. This will fetch the addresses of 
  those customers who have 1 as their id_customer. Similarly, you can use any other field and its corresponding value. 

  - The `LIKE` operator is used when you need to search for items. For example, if you want the addresses with 
  cities starting with **SAINT**, use the filter as `filter[city]=[saint]%` where city is a field of the addresses endpoint. This will return 
  the addresses of those customers who have their city starting with `saint`.

  - The `OR` operator is used when you need to get items matching several criteria. Use the filter as `filter[city]=[paris|lyon]` 
  where city is a field of the addresses endpoint. This filtering condition will provide you with those addresses where the city belongs to 
  `paris` or `lyon`.

  - You can also use `filter` in combination with the `display` parameter. Let say you want to get the mobile phone numbers 
  of customers #1, #7 and #42. You need to use the filtering condition as `filter[id_customer]=[1|7|42]` and `display=[phone_mobile]`. Write the 
  conditions seperately as key-vaule pair in the action filter and join them using `&&` operator.

  - If you need to filter the entries in the input packet according to their date, then you should always 
  specify `date=1` parameter to allow date filtering.  

Let us consider the API structure of `customer` schema in Prestashop application. If you need to fetch a group of customers from the application, 
you can specify the condition in the action filter by taking any field from the xml structure of the respective APIs. For instance, to fetch customer with id as 1 
use `filter[id_customer]` in the key field and `1` in the value field. To display specific fields from customer schema, such as firstname, 
lastname and email, use `display` in the key field and `firstname,lastname,email` in the value field.

```
<prestashop xmlns:xlink="http://www.w3.org/1999/xlink">
  <customer>
    <id><![CDATA[]]></id>
    <id_default_group><![CDATA[]]></id_default_group>
    <id_lang><![CDATA[]]></id_lang>
    <newsletter_date_add><![CDATA[]]></newsletter_date_add>
    <ip_registration_newsletter><![CDATA[]]></ip_registration_newsletter>
    <last_passwd_gen><![CDATA[]]></last_passwd_gen>
    <secure_key><![CDATA[]]></secure_key>
    <deleted><![CDATA[]]></deleted>
    <passwd><![CDATA[]]></passwd>
    <lastname><![CDATA[]]></lastname>
    <firstname><![CDATA[]]></firstname>
    <email><![CDATA[]]></email>
    <id_gender><![CDATA[]]></id_gender>
    <birthday><![CDATA[]]></birthday>
    <newsletter><![CDATA[]]></newsletter>
    <optin><![CDATA[]]></optin>
    <website><![CDATA[]]></website>
    <company><![CDATA[]]></company>
    <siret><![CDATA[]]></siret>
    <ape><![CDATA[]]></ape>
    <outstanding_allow_amount><![CDATA[]]></outstanding_allow_amount>
    <show_public_prices><![CDATA[]]></show_public_prices>
    <id_risk><![CDATA[]]></id_risk>
    <max_payment_days><![CDATA[]]></max_payment_days>
    <active><![CDATA[]]></active>
    <note><![CDATA[]]></note>
    <is_guest><![CDATA[]]></is_guest>
    <id_shop><![CDATA[]]></id_shop>
    <id_shop_group><![CDATA[]]></id_shop_group>
    <date_add><![CDATA[]]></date_add>
    <date_upd><![CDATA[]]></date_upd>
    <reset_password_token><![CDATA[]]></reset_password_token>
    <reset_password_validity><![CDATA[]]></reset_password_validity>
    <associations>
      <groups>
        <group>
          <id><![CDATA[]]></id>
        </group>
      </groups>
    </associations>
  </customer>
</prestashop>
```
- You can retrieve Customers from `Prestashop` by creating a variable at processflow level 
![prestashop_1](/staticfiles/connectors/media/application-connector/prestashop_1.png) 

and using it in the action filter.
![prestashop_2](/staticfiles/connectors/media/application-connector/prestashop_2.png)
  
- Fetch the updated customer information from `Prestashop` using a variable at processflow level
![prestashop_3](/staticfiles/connectors/media/application-connector/prestashop_3.png)

and using it in the action filter.
![prestashop_4](/staticfiles/connectors/media/application-connector/prestashop_4.png)

> [Click here](https://devdocs.prestashop.com/1.7/webservice/getting-started/#available-parameters) to know the usage of filters other than the mentioned above. 




