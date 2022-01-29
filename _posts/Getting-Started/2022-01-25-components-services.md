---
title: "Components and Services"
toc: true
tag: developers
category: "Getting Started"
menus: 
    gettingstarted:
        title: "Components and Services"
        weight: 4
        icon: fa fa-wpexplorer
        identifier: componentsandservices
---

## What is an APPSeCONNECT Components?

APPSeCONNECT is a iPaaS which enables developer or citizen integrator to build integration solution such that the data could be transferred from one application to another in a seamless and free-flowing manner.It acts as middleware between enterprise applications which transfers data from one application and updates the same to their respective applications.
It provides secured and powerful tooling capability which will let users create integrations between various bussiness applications.However,APPSeCONNECT consists of the following componenets to bring the power of automation into business operations,unleashing productivity and growth across teams in your organization.


* Portal

* Adapters. 

* Agent. 

* Apps and application profiles. 

These are reusable program blocks or components that are integrated with other blocks to form APPSeCONNECT.All these components communicate with each other for needed services,viz. control integration between APPs.APPSeCONNECT mostly uses the default APIs available with eCommerce,CRM,Marketplace and ERP systems.
Apart from that,APPSeCONNECT has a small software named ‘Agent’,installed within the ERP server,which is used to configure and control the integration.While its cloud part is used to configure the integration Touchpoints and interact with the Agent remotely.


## Portal

The APPSeCONNECT portal is the web based interface where you can access APPSeCONNECT application for efficient,smooth, free-flowing integration,with the set of Functional modules.The [APPSeCONNECT portal](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2f#!) is easily accessible by clicking on the aforesaid link.
Once you have logged in,you will be able to view the following scenerio enabling an end-user or citizen integrator to view basic information about users,functional module,bookmarks,subcription details,execution status,execution counts etc.

![DashboardView](/staticfiles/root/media/DashboardView.png)

In the above figure,some elements of the APPSeCONNECT portal are common to all apps,accessible via the left side panel of the page.Of note,these also includes accessing your account,where you can update your information as well as changing your password.

The set of functional modules are easy to navigate and ease the method of integration via our Portal.
The view of functional module(s) is given below:

![FunctionalMenus](/staticfiles/root/media/FunctionalMenus.png)

Let us walkthrough the Functional Modules for understanding the usage and need of each menu. 

|Modules|Details|
|---|---|
|Home|This page will show the details of the organisation,user logged in into,Project Basic Information,Configuration Completion Details etc.|
|Designer|This section will allow users to design the business flows using Workflows or Processflows|
|Deploy|This section will let users work with the Environment deployed.|
|Manage|This section will allow the users to manage their Apps,Connections,Rules,Repositories,APIs,Feeds etc.|
|Help|This section will allow the user to get help and learn about the usability of the features.User can easily connect to the Documentation and Community resource from HELP.|


## Adapters

Adapter in terms of APPSeCONNECT is a piece of software component external to the business application which is built as a plugin to the platform allowing developers or implementors to connect two external application in a seamless and free-flowing way.
The responsibility of an adapter is to ensure smooth and efficient communication between two application such that APPSeCONNECT can use adapter to fetch and push data to respective business applications whether it is On-Premise or Hosted.This also defines how an external application
is communicated through APPSeCONNECT,credential is defined and used for communication.Thus,it can be concluded that adapter acts as a actual communication layer between business application and APPSeCONNECT.

APPSeCONNECT platform is built using Microsoft.NET,so you need to be acquainted with any of the high level languages present in .NET platform.This platform provides an SDK which will be used to develop and implement an adapter using any standard .NET language like C# or VB.NET.
Our SDK is hosted as Nuget Package or publicly available to developers.


## Agent

APPSeCONNECT Agent is an application which execute and control the sync process by transferring information or data from one business application to another with the help of adapters.
More technically,APPSeCONNECT Agent is the light-weight,dynamic,run-time engine for the sync process which takes data from one adapter and hands it over to another for their respective business application,after performing the required data conversion or manipulation to ensure efficient,smooth and free-flowing integration.
The Agent is either locally installed in the target organization’ server or can reside withn the APPSeCONNECT cloud platform depending on the deployment model chosen,to handle the sync processes for an organization exclusively.

Thus,to wrap up in short it can be stated that APPSeCONNECT performs two major roles as below.

* Responsible to execute the instructions given in cloud application.
* Transfers the data from one APP to another with the help of its adapters.

## Apps and Application Profiles

APPSeCONNECT is a iPaaS which lets developer or citizen integrator to build integration solution such that the data could be seamlessly transferred through it such that it acts as middleware between enterprise applications which transfers data from one application and updates the same to their respective applications.
But,every application is different in terms of API,their structure,data format,endpoints etc.Thus,to perform a smooth and efficient integration with APPSeCONNECT the data format,layout,structure,
endpoints etc. of each and every business application needs to be correctly defined.Here comes the importance of APPSeCONNECT,where APPs gives you a way to logically seperate these profiles form one another.

In APPSeCONNECT,APPs provides you an area to define all the above mentioned particulars of an API for a business application such that they are separated from one another.In other words,APPs is a logical
grouping of end ponits such that functioning and working with API endpoints become easier.

**Note : In APPSeCONNECT,name of APPs are given with actual line of business application.**

### Need of APPs

* Enhance sales growth.
* Audience building.
* Business process optimization.
* Marketing and communication channels.
* Valuable analytics.
* Competitive advantage in the business market.

### Types of APPs

* Native App - These are pre-built and pre-packaged APPs that are available in Portal to perform integration in a smooth,seamless and free-flowing way.For example,if a situation arises where an end-user wants 
to integrate data between Magento and SAP Busuness One,then the APPs that are available in portal for Magento and SAP Business One can be used provided the schemas,protocols setup and adapters version matches with the business requirement.
* Technology App - Technology APPs are built by any developer or citizen integrator by using pre-defined schemas,protocol set-up,adapters that are currently available.
* Custom App - To build APPs from scratch Custom APPs are used by APPSeCONNECT users to suite them as the best solution.

## Schemas

A schema is defined as structure of an entity that requires multiple actions to perform multiple operations depending on the data that needs to be retrieved or consumed from an application as per the transaction happening.
This also provides a logical seperation between two or more APIs,such that each data structure can be individually identified by a canonical name.In APPSeConnect,to add schemas to your app node,`Add Schema` and `Import Schema` options are availbale.

## Action & Filters

**Actions** are certain tasks or commands like getting data from an application or sending data to an application based on specific API filter conditions known as **Action Filters**.APPSeCONNECT lets you define actions of each and every schemas whether it is manually added or imported one,by providing `Action Name` and `Action Description`.

**Action filter** for an integration represents the same as API filters.In APPSeCONNECT,**Action filter** lets you define a filter criteria for an action which filters out the data from the API.You can think this as an Where clause of a Select statement or even a search criteria in Windows file system.You should always define an action filter by learning the API structure,such that you dont call the same data again and again.

The dynamic **Runtime Filter** feature is available for performing specific integration operations at any instance.This Filter's functionality will only allow you to **Create**,**View** and **Delete** filters.

The **Retry filter** allows end-user or citizen integrator to create a filter that downloads an item based on a particular id such that the erroneous data can be resynced.
