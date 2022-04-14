---
title: "Publishing to Marketplace"
toc: true
tag: developers
category: "Processflow"
menus: 
   packagesoverview:
        title: "Publishing to Marketplace"
        weight: 4
        icon: fa fa-file-word-o
        identifier: packageprocessflow
---

Processflow Packaging is a concept of zipping multiple ProcessFlows or Processflow folders from one organisation to another. 
Processflow being the advanced version of workflows, now enables you to select ProcessFlows and develop a package out of it, which can be shared and have the option to install 
in a different organisation. This document will help you to create and publish a package,re-versioning as well as re-publishing them.

## Creating Package

This section will enable you to create new package from created processflows. Follow the below steps to create a new package.

1. Login to Portal and navigate to the **Designer** > **ProcessFlow** module. This loads the ProcessFlow tree which gives access to your **Package Library**. 
2. Expanding **Package Library** node,you'll be able to view **My Packages** folder. Click on **My Packages** folder,to create new packages. 
![Packagelibrary](/staticfiles/processflow/media/packagelibrary.png)

3. In this screen,you'll see all the packages that you have already created as well as if you want to create new package click on **Create** button.

![PackageCreate](/staticfiles/processflow/media/package-create.png)

4.Clicking on **Create** button,the package creation wizard appears. The package creation wizard comprises of three sections.

i. **Choose ProcessFlows** - This section will allow you to choose various processflows from ProcessFlow folder as well as its sub-folder. The selected Processflows will be displayed in the upper table as you select them. 

a) In the Choose ProcessFlows section, you’ll be able to view the folder path, that will enable you to find Processflows from your Processflow folders. By default, the Home Folder will be selected in the **Folder Path** and all the Processflows under **HOME** folder will be listed in the below table for the selection process. 

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

**Note: Any changes made to the original Processflow, the modifications will not reflect in the packaged versions. You need to create a new package for packaging the modified ProcessFlows.** 


## Publishing Package

Once you have created your Processflow Packages, you can successfully view the packages in the **My Packages** listing page of your organisation. But if you want to make it available to the external users, you need to go through the publishing procedure which will validate your creation and list your package to APPSeCONNECT marketplace. 

1. Navigate to the **Designer** > **ProcessFlow** module. This loads the ProcessFlow tree which gives access to your **Package Library**. 
2. Expand the **Package Library** node in ProcessFlow listing page and click on **My Packages** folder. 
3. On **My Packages** folder,you can view the created packages on your organisation. 
![publishtomarketplace1](/staticfiles/processflow/media/publishtomarketplace1.png)

4. Select a package from **My Packages** folder that have its status displayed as **New**. Click on the contextual menu available in the Actions column which will display **Publish To Marketplace**. 
![publishtomarketplace2](/staticfiles/processflow/media/publishtomarketplace2.png)

5. Clicking **Publish To Marketplace** will sent the package to the approver for acceptance. The approvers are the subject matter experts on the platform who can install your package, test it in their environment before approving. The approving is a manual process, and we encourage you to visit your library to check the status. 
6. After you submit your request for publishing, you'll see your package Status is changed from **New** to **Waiting for Approval**, which means, the approver is looking into it. 

![publishtomarketplace3](/staticfiles/processflow/media/publishtomarketplace3.png)


## Accessing Comments,Re-Versioning and Re-Publishing

Publishing a package to a marketplace is not an easy job. There are a number of steps required to be done before you can finally publish it to marketplace. The approver will ensure all the processes you mentioned on the package documentation is perfectly implemented in the package or otherwise they will send a change request. Once the change request is received, you'll be able to regenerate a new package with a new version and resubmit the changes. 
Let us look at the steps to publish the package after re-versioning. 

1. Publish a package to Marketplace by clicking **Publish To Marketplace**. The status of this package will be changed to **Waiting for Approval** from **New**. 
2. An Approver after reviewing the package can approve, reject or respond to a package. 
3. Clicking on **Package Library** node in ProcessFlow listing page,you’ll be able to view **My Packages** folder. 
4. On **My Packages** folder, you can view the created packages on your organisation. The status of those packages bear **Responded** will have comments given by the approver. 
5. Click on the context menu and you can view **Re-Publish to Marketplace**. You can view the comments provided by the approver. 
![packagecomments](/staticfiles/processflow/media/packagecomments.png)

6. Perform the necessary changes as suggested by the approver and send the package for approval.
**NOTE – Package with same version cannot be re-published. Upgrade the package version before sending for approval.** 

7. If you donot change the version,then the message **Package Version already exist. Please Provide a new version** will be displayed.Henceforth,you should change the version of the package and **Re-Publish** the same. 
![packagereversioning](/staticfiles/processflow/media/packagereversioning.png)