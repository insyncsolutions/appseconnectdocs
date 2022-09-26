---
title: "Overview of Application Connectors"
toc: true
tag: developers
category: "Connectors"
redirect_from: 
     - /connectors/overview-of-application-connectors/
menus: 
    Connectors :
        title: "Application"
        weight: 6
        icon: fa fa-file-word-o
        identifier: applicationconnector
---

An Application connectors are Pre-built optimized solution developed by APPSeCONNECT backend developer team and tested 
in real-life scenarios. If you have an application which has an application connector present on APPSeCONNECT platform,
you as an end user require very small effort to configure the connector to work correctly with the application. These connectors are 
maintained by the InSync team which consists of a number of highly skilled developers who work with the platform
to provide Actions and Schemas specific to the Application.

![](https://www.youtube.com/watch?v=aYOhkVw9J2E)

For application connectors, we have pre-built templates as well which connects two or more application together
where all the business logic to transform data from one application to another is pre-baked and devleoped and tested. 
Hence as an user, you can readily use those connectors just by adding them to your project and execute them on the platform.
Sometimes, these connectors requires some trivial adjustments because may be your applications are highly customized, and these 
adjustments can be implemented easily in the portal with zero code requirements.

## Type of Applications

Applications are broadly categorized into multiple types. They define the functions that the application is going to perform. 
Here are some of the application categories which cater to certain business proceses. 

### ERP(Enterprise Resource Planning) 

`Enterprise Resource Planning` (ERP) refers to a type of software that organization uses to manage day-to-day business activities 
such as accounting, procurement, project management, risk management and compliance, and supply chain operations. 
A complete ERP suite also includes enterprise performance management, software that helps plan, budget, predict, and report on an 
organization’s financial results.   

#### What are the key business benefits of ERP software?

**Information Integration** 

The most important benefit is promotion of integration. It is because it has the ability to update data between related business 
functions and components. Also the people involved in a project are interlinked to each other, thus it helps in improvement of productivity. 

**Reduction of Lead-Time** 

By reducing `Lead-Time` organization should have an efficient inventory management system, which is integrated with the purchasing, 
production planning and production departments.  

**On Time Shipment** 

`ERP` system are designed to help your company to reduce data transfer time, reduce errors and increase design productivity. 

**Better Customer Satisfaction** 

`ERP` system is capable of producing goods in a flexible way with consideration of time and cost management. 
It means will get individual attention and get services without spending more money or waiting for long period.   

**Increased Flexibility**  

Product flexibility is type of ability of the operation to efficiently produce highly customized and unique products. 
`ERP` system not only improve flexibility of manufacturing operations, but also improves flexibility of organization.  

#### Examples of SAP 

- SAP Business One
- SAP Servie Layer
- SAP ECC

### eCommerce 

`Electronic commerce`(ecommerce) refers to companies and individuals that buy and sell goods and services over the web. 
Ecommerce operates in different types of market segments and can be conducted over computers, tablets, smartphones, and other smart devices.  

#### Examples of E-Commerce

- Magento
- Shopify
- Amazon Seller Central

### CRM(Customer Relationship Management)

`CRM` stands for `Customer Relationship Management` and refers to all strategies, software and technologies 
used by organizations for engaging, acquiring and retaining customers. `CRM` is a combination of business strategies, 
software and processes that enables companies to build long lasting relationships with their customers.  

CRM software allows companies to automate customer-related workflows and ensure that all interactions 
with customers and prospects happen smoothly and efficiently across the entire customer journey. 
CRM software enables organizations to increase close rates, boost loyalty, and drive profits. 
With CRM software, companies can easily collect and manage customer data from multiple channels 
to build more precise customer profiles, provide personalized customer engagements and ensure 
maximum productivity of customer-facing teams.  

#### How a CRM helps your business?

- **IDENTIFY AND CATEGORISE LEADS** - A `CRM` system can help you identify, add new leads easily 
and quickly, and categorise them accurately. By focusing on the right leads, sales can prioritise 
the opportunities that will close deals, and marketing can identify leads that need more nurturing 
and prime them to become quality leads. 

- **INCREASE REFERRALS FROM EXISTING CUSTOMERS** - By understanding your customers better, cross-selling 
and upselling opportunities become clear — giving you the chance to win new business from existing customers.  

- **OFFER BETTER CUSTOMER SUPPORT** - A `CRM` system can help you provide the high-quality service 
that customers are looking for. Your agents can quickly see what products customers have ordered, 
and they can get a record of every interaction so they can give customers the answers they need quickly. 

- **IMPROVE PRODUCTS AND SERVICES** - A good CRM system will gather information from a huge variety of 
sources across your business and beyond. This gives you unprecedented insights into how your customers feel 
and what they are saying about your organisation such that you can improve what you offer, spot problems early, 
and identify gaps.  

#### Examples of CRM 

- Salesforce
- Zoho CRM
- Dynamics CRM
- Hubspot

## List of Pre-packaged Application Connectors

APPSeCONNECT as a platform supports a wide range of [pre-packaged connectors](/getting%20started/configurations/#process-of-choosing-app), which can be easily plugged and played 
by the enduser. These connectors are mainly developed in generic manner taking in account on Vanilla system application. Some 
customizations might be needed for the organizations to support custom implementation or customizations made over the vanilla applications. 

|Application|Application Type|Description|Versions|
|---|--|------|-----|
|[Magento](/connectors/Magento2/)|eCommerce|Magento is an ecommerce solution in Community or Enterprise variant which is supported by APPSeCONNECT platform| v1.0, v2.0|
|[Shopify](/connectors/Shopify/)|eCommerce|Shopify is a cloud based eCommerce solution which provides two variant, Shopify and Shopify Plus, both supported as pre-packaged solution in APPSeCONNECT|v1.0|
|[Priority](/connectors/Priority/)|ERP|Priority is the first application in the ERP arena to support a single integrated solution for all your operational needs, supported as pre-packaged solution in APPSeCONNECT|v1.0|
|[Sage](/connectors/sage300/)|ERP|Sage 300 is a cloud based ERP system which has only one version which comes as a pre-packaged application with APPSeCONNECT|SAGE300 2018|
|[WooCommerce](/connectors/woocommerce/)|eCommerce|WooCommerce is an E-Commerce Platform which supports two versions of it, as it is one of the pre-packaged application of APPSeCONNECT. |v1.0|
|[Uniconta](/connectors/uniconta/)|ERP|Uniconta is a cloud based ERP System that comes a pre-packaged application with APPSeCONNECT|v1.0|
|[SAP Business One](/connectors/sap-business-one/)|ERP|SAP Business One is an ERP System which is supported by the APPSeCONNECT|>=v8.8 & SAP B1 S/L 9.0|
|[Bamboo HR](/connectors/bamboohr/)|ERP|BambooHR is a cloud based Human Resource Platform which is one of the pre-packaged application of APPSeCONNECT|v1.0|
|[ZohoCRM](/connectors/zohocrmv2/)|CRM|This is a cloud based CRM Application which is supported by APPSeCONNECT|v1.0 & v2.0|
|[MS Dynamics Business Central](/connectors/dynamicsnav-business-central/)|ERP|This is an ERP System which comes as a pre-packaged application with APPSeCONNECT|≥ v2009R2 Generic|

You can choose as many of the pre-packaged solution on the platform to connect between one another. 