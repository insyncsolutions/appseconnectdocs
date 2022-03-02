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
APPSeCONNECT is a iPaaS which enables developer or citizen integrator to build integration solution such that the data could be transferred from one application to another in a seamless and free-flowing manner.It acts as middleware between enterprise applications which transfers data from one application and updates the same to their respective applications.
It provides secured and powerful tooling capability which will let users create integrations between various bussiness applications.However,APPSeCONNECT consists of the following componenets to bring the power of automation into business operations,unleashing productivity and growth across teams in your organization.

## What is an APPSeCONNECT Components?

APPSeCONNECT provides a number of components and services which enables the developers use to create and maintain an integration solution for the customers. These are : 

* Portal 
* Agent
* App Profiles
* Packages
* SDK

Each of these components present in APPSeCONNECT works in tandem to generate integration solution between source and destination application. 
The components provides specific building block for the integration, each of them are capable of doing specific operation on the platform.
APPSeCONNECT as an iPaaS provides a way to deliver Business Process Automation by integrating data flow between all the applications present in 
a business enabling smooth update of data between applications. 

> Some of the components are also allowed to be built be community

## Portal

The portal is the web based application that allows the Citizen integrators create integration between one or more applications. The portal gives appropriate 
tools and services to help design, develop, and maintain integration solutions. The Portal is the main interface from where almost all the activities 
related to the application is performed over time. The [APPSeCONNECT portal](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2f#!) 
is protected behind a secure authentication to ensure the data is safe inside it. The Portal can be opened directly from the browser application giving 
the user a 360 degree view of all the services running on the environments and also allows to manage them from it. 

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
 
## Agent

Agent is a small tool that does the actual transformation of data between application. The Agent takes instructions from Portal through standard APIs
and follows it to generate seamless integration between applications. The ProcessFlows created on the portal is deployed and downloaded to the agent to execute. 
APPSeCONNECT allows to use two kinds of Agents : 

1. Hosted Agent 
2. On Premise Agent

The Hosted Agent is a micro-service based multi-tenant platform that executes your processflow into its fabric either automatically, or manually based 
on users action. Any notification or status of synchronization will be directly available over the Portal. 

## Application Profiles

iPaaS bridges the data synchronization between applications. Now If you think of applications, they are generally updated using API. Each of the APIs
are different in terms of structure, way of connectiviity, protocols, etc. Hence, there is always a need of creating Application Profiles, which 
individually can connect to a specific application to fetch or push data. 

In APPSeCONNECT,APPs provides you an area to define all the above mentioned particulars of an API for a business application such that they are separated from one another.In other words,APPs are the logical
grouping of schemas, actions, credentials, adapters etc. such that they can be easily separated from one another. The App section in APPSeCONNECT
provides a way of defining Schemas and Actions specific to an App, such that when the same is used again, these API informations can be reused again. 

**Note : In APPSeCONNECT, name of APP is used to define Application profiles for simplicity.**

### Need of Apps

* Easy to find Schemas and Actions specific to an App.
* Less chances of Bugs.
* Optimized for one API.
* Requires less customizations.
* Easily understandable through App Logos.
* Easily marketable for Citizen Integrators.

### Types of APPs

* Native App - These are pre-built and pre-packaged APPs that are natively supported by the platform. The APIs are already mapped for these applications and tested by the community. 
The native apps are configured by the product team to give you best experience and lesser or negligiable learning curve to use it. 
* Technology App - These apps are pre-build and provided by the platform for a specific protocol. A protocol defines the way of communication. Even though a technology app does not define
the various tenats of the apps like schemas, actions, etc to map the APIs of any application, but they provides a way to connect APIs without defining an Adapter or without going through the 
complexities of the data channels and connectivity. 
* Custom App - These apps are built from scratch, and is only used when someone requires high level of customization and the other type of apps does not support them.

## Packages

Even though there are a lot of pre-packaged apps supported in the platform which gives you access to a huge number of APIs, sometimes, as an end user 
you might want to avoid the complexity of understanding how the data should flow from your applications. The Packages are a set of ProcessFlows already developed
for the end users, which can be readily consumed whenever it deems fit for a customer. 

A package provides a way of sharing a full fledged business process, such that everything about the package reside within it. For example, let us suppose you want to integrate between 
magento and SAP. If you use the Pre-packaged Apps to create an integration between them, that means the developer needs to create mapping using APPSeCONNECT Expression language
such that the data could be transferred between applications correctly. But in case you opt for a package, installing a package will automatically create the necessary mappings and everything 
to connect between the two or more applications. After installing a Package, you can deploy to an Agent to execute and sync data. 

### Types of Package

1. Private Package: These are privately owned packages, which can be shared with other Organizations as a Partner. The Privately held packages can also be kept safe for furture use. 
2. Public Packages: These are the packages which are in global cache and available to the external world. The Public packages can be freely installed in any organization based on the permission. 


## SDK

An adapter is a software component or a plugin which builds the bridge between the line of business application with APPSeCONNECT. 
The responsibility of an adapter is to ensure the data created by APPSeCONNECT could be either requested to the target application through 
adapter or the data is pushed directly to the target application. There are two responsibiltity of any adapter, 
 - Pull Data
 - Push Data

 An adapter is built using an SDK, a software development kit provided by APPSeCONNECT, which can help in building the bridge between your application
 with APPSeCONNECT. As APPSeCONNECT works with XML, so from APPSeCONNECT any XML which is posted to an adapter needs to be processed and communicated to
 the application. 

APPSeCONNECT platform is built using Microsoft.NET,so you need to be acquainted with any of the high level languages present in .NET platform.This platform provides an SDK which will be used to develop and implement an adapter using any standard .NET language like C# or VB.NET.
Our SDK is hosted as Nuget Package or publicly available to developers.
