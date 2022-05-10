---
title: "Steps to create a Package"
description: "Experience the flavour of creating, editing and viewing packages."
keywords: "create packages, listing packages, viewing packages, editing packages"
toc: true
tag: developers
category: "Processflow"
menus: 
   packagesoverview:
        title: "Creating a Package"
        weight: 1
        icon: fa fa-file-word-o
        identifier: packageprocessflow
---

Processflow Packaging is a concept of zipping multiple ProcessFlows or Processflow folders from one organisation to another. 
Processflow being the advanced version of workflows, now enables you to select ProcessFlows and develop a package out of it, which can be shared and have the option to install
in a different organisation. This document will help you to create a new package.

## Prerequisites

- You need to have valid credential to the portal.
- You need to have the Processflow created. Steps to create new Processflow is given [here](/getting%20started/create-your-first-processflow/).
- You cannot create package out of a [Shared package](/processflow/processflow-package-sharing/), for the ProcessFlows that are [installed](/processflow/processflow-package-installation/) on your organisation.
- You can select your ProcessFlows only from the [Processflow folder](/processflow/processflow-listing-page/#process-flow-folder) and its sub-folder.
- You can add as many ProcessFlows for creating a package. There is no specified limit when adding ProcessFlows, while creating package.

## Creating Package

This section will enable you to create new package from created processflows. Follow the below steps to create a new package.

1. Login to Portal and navigate to the **Designer** > **ProcessFlow** module. This loads the ProcessFlow tree which gives access to your **Package Library**. 
2. Expanding **Package Library** node, you'll be able to view **My Packages** folder. Click on **My Packages** folder, to create new packages. 
![Packagelibrary](/staticfiles/processflow/media/packagelibrary.png)

3. In this screen, you'll see all the packages that you have already created as well as if you want to create new package click on **Create** button.
![PackageCreate](/staticfiles/processflow/media/package-create.png)

4. Clicking on **Create** button, the package creation wizard appears. The package creation wizard comprises of three sections.

i. **Choose ProcessFlows** - This section will allow you to choose various processflows from ProcessFlow folder as well as its sub-folder. The selected Processflows will be displayed in the upper table as you select them. 

a) In the Choose ProcessFlows section, you’ll be able to view the folder path, that will enable you to find Processflows from your Processflow folders. By default, the Home Folder will be selected in the **Folder Path** and all the Processflows under **HOME**  folder will be listed in the below table for the selection process. 

b) The Processflow table below, will enable you to select the ProcessFlows for packaging. The following details will be displayed in the table. 

   **Name** - Name of the ProcessFlows.                   
   **Description** - This will display you the Processflow description.             
   **Image** - This will let you view all the logos of the application implemented inside the Processflow. Processflows exceeding four Applications inside will have a carousel slider in the image column to let you view all the applications in use. 
    Select the ProcessFlows by enabling the checkboxes beside the Processflow names. You’ll be able to view the Selected ProcessFlows in the table above, along with the same details. 

![Packagechooseprocessflow](/staticfiles/processflow/media/package-chooseprocessflow.png)

c) Click on the **Continue** button. The Configuration section appears on the package creation wizard.


ii. **Configuration** - This section will allow you to configure the details of the packages required.

a) You can now view the **Configuration** section. You need to provide the following details. The following details will be available in this section. 

![Packageconfiguration](/staticfiles/processflow/media/package-configuration.png)

**Package Name** - You need to enter the name of the package. The name should be less than 100 characters.                
**Package Description** – You’ll be provided with a platform to enter a description to the package. There is no limitation to the description based on the number of characters.                        
**Version** - You can provide a version to the package. The version should be equal to 3 decimal places. You'll be provided with an example, beneath the field.                          
**Package Documentation** - This is a markdown editor and you need to add the related documentation or links for reference. You can also preview the provided document or link by clicking on its preview button.                              

b) Click on the **Continue** button after providing all the mandatory details of the package.


iii. **Preview**- This section will display all the configurations provided in the earlier steps as a final preview. 

a) You’ll be navigated to the Preview section. You’ll be able to view all the related details you provided in the previous steps. 

![Packagepreview](/staticfiles/processflow/media/package-preview.png)

b) Click on the **Save** button to the create the package. Following the above process, you can successfully create a Processflow package. 

**Note : Any changes made to the original Processflow, the modifications will not reflect in the packaged versions. You need to create a new package for packaging the modified ProcessFlows.** 


## Listing Packages

Once you have created your Processflow Package, you can successfully view the package lists in the Processflow Home page of your organisation. As a prerequisite, you need to have your packages created on your organisation.

1) Navigate to the Processflow module. The [Processflow Home](/processflow/processflow-listing-page/) page appears.

2) Expand the package library node. You will be able to view the folder **My Packages**. 

3) Click on the My packages folder. You will be able to view the "My Packages" listing page. The following information will be displayed in the listing page.

- **Package Name** - You will be able to view the names of the packages listed in the "Package Name" column.
- **Status** - You will be able to view the status of the package.
- **Apps** - You can view all the applications used in the ProcessFlows containing in the package in a corousel slider.
- **Sharing** - You can view an icon indicating that the package is shared to any other organisation.
- **Actions** - Clicking on the Ellipses (Three horizontal dots) on the action column, you can view the following three options : **Edit**, **View** & **Publish to Marketplace**.

![package7](/staticfiles/processflow/media/package7.PNG)

Following the above process you can successfully view the list of the packages.

## Viewing Packages

Now you have done creating your packages, and you can view the packages listed under `My Packages` Section. 
To View a specific Package,  click **View** option available on the Contextual menu of the Package.
![package-edit-view](/staticfiles/processflow/media/package-edit-view.png)

The following pop up appears where you can view the package details along with 
three specific tabs namely - Description, Documentation, Processflow.
![packageview_package_final](/staticfiles/processflow/media/packageview.png)

The `View Package` window offers you with the following package information.  

**Package Name** - Package name information was provided during Package creation.     
**Version** -  Version information was provided during Package creation.    
**Created by** - This indicates the Organization name of the user who created the Package.     
**Install** - This button enables to install the package. You can install the package from `My Package -> View Package-> Install` option & also 
from `Shared with Me -> Package-> Install` section. [View here](/processflow/processflow-package-installation/) 
for installation details.  

The tab details are mentioned below :

**Description Tab** - This section provides you the package description along with the view of application
used in the packages. Here you can also view the last modified package date and time along with the icons of the apps used.       
**Documentation Tab** - This section provides you the documentation of the ProcessFlows.        
**Processflow Tab** - This section enlist the list of Processflow included in the package.      

In the Processflow Tab  `Search` option is provided where you can search the required 
processflows by providing the processflow names.  

## Editing Packages

This section enables you to edit package information as per your business requirement which you have 
created. You can edit any Package available in Package Library section.

1. For editing packages go to ProcessFlow Menu -> Package Library section-> My Packages.
2. Now to edit a  Package, click **Edit** option of the Contextual menu of that Package.
![package-edit-view](/staticfiles/processflow/media/packageedit.png)  

3. This will open the `Edit Package` window.  
![package-edit](/staticfiles/processflow/media/packageedit1.png)

4. In the `Edit Package Details` window, here you will be able to edit the following fields :

(a) You can also add new processflows to your package as per your requirement.     
(b) Package Name - Here you can edit the package name.                   
(c) Package Description - Here you can edit the Package Description.                    
(d) Package Documentation - Here you can edit the package documentation and all the associated functionality of the documentation.                         
(e) Package Version - Here you need to provide a new version of the edited package.                        
After doing the changes, the User will be able to save the changes by clicking on the Save button. 
If the user clicks on the Cancel button, the changes will not be saved.  

**Note : (a) You will be able to view the Package Documentation within the Editor, during Edit mode.  
(b) Preview option is available in the editor to view the changes.  
(c) In Edit mode, you will not be able to view or edit the Processflow(s) present in a Package**.  





