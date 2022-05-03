---
title: "Dynamics 365 Business Central"
toc: true
tag: developers
category: "Connectors"
menus: 
    navbusinesscentralconnector:
        title: "Dynamics 365 Business Central"
        weight: 14
        icon: fa fa-file-word-o
        identifier: navbusinesscentralconnectorcloud
---
## Introduction
 
Business Central is a business management solution for managing your business for various sized organizations that automates and streamlines business processes. Companies can eventually add functionalities which is relevant to the domain of operations, and can customized to support even highly specialized industries. Business Central provides solutions to the companies to manage their business, including finance, manufacturing, sales, shipping, project management, services, and many more with its highly adaptable and rich features. 
 
Business Central is fast and easy to implement and configure, and its simplicity guides to innovate product design, development, implementation and usability. 
 
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
The list will guide you about the fileds of the web services like Object Name, Object Id, Service Name, Published Mode etc, while calling the web services from the different applications. Keep the format as mentioned in the list. 

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