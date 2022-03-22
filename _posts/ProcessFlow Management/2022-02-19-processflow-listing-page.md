---
title: "Organizing ProcessFlow"
toc: true
tag: developers
category: "Processflow"
menus: 
    processflow:
        title: "Organizing ProcessFlow"
        weight: 5
        icon: fa fa-file-word-o
        identifier: organizing processflow
---

This section provides the option of creating folders for organizing the ProcessFlows with respect to the business 
requirements for any organizations. ProcessFlow Home section helps users to organize & manage all the processflows 
in folder structure such that user can maintain an easy usability as per their requirement. 

**To know more about the modules that would help creating ProcessFlows from the ProcessFlow Home Page, Navigate to the [Quickstart](/processflow/Quickstart-guide-to-processflow/) section.**

## ProcessFlow Home

1. Click on the **ProcessFlow** folder or any other folder. The Home page for the selected folder is displayed on the right side of the page. The Processflow Home page will list all the processflows that are created in the selected folder.  
2. For each processflows, the following details will be displayed.  
* **Name** : Displays the name of the ProcessFlows.  
* **Description** : Displays the description of the ProcessFlows.   
* **Action** : Clicking the three horizontal dots against each processflow, user gets the options to **Edit**,**Copy**,**Delete** & **Generate mapping document** for existing ProcessFlows.     

3. a. Click Edit Button, the **[Designer page](/processflow/designer-processflow/)** opens for the selected ProcessFlow for editing.  
   b. Click Copy Button, you'll be able to select the desired folder and sub-folder to duplicate your processflow and save them. Click [here](/processflow/copy-processflow/) to get details steps to perform duplication. 
   c. You can download the mapping document directly from the Portal to get information about the transformation logic. 
   d. Click Delete button, the selected ProcessFlow is moved to the Trash folder.
![processflowlisting-page2](/staticfiles/processflow/media/processflowlisting-page2.png) 

4. The ProcessFlow Home page will have a **NEW** button on the top right corner  
   of the page for [creating a new processflow](/processflow/creating-processflow/). Clicking on the **NEW** button, 
   you will be navigated to the [ProcessFlow Designer](/processflow/designer-processflow/).
![processflowlisting-page4](/staticfiles/processflow/media/processflowlisting-page3.png) 

5. The **FILTER** button is available beside the **NEW** button. Click on the button, you can filter processflows using search functionality, from the list.   


## ProcessFlow Folder

On visiting the **ProcessFlow Home** page, you can view the **Home** folder which is already selected. This 
is a default folder and every organisation within APPSeCONNECT would contain the 
Home folder for the **ProcessFlow Home** page.

1. Click on the three horizontal dots of **Home** folder, you can view a **NEW** button 
in the drop down that would enable the user to create a child folder of the selected folder.
![Processflow Home2](/staticfiles/processflow/media/processflow-home2.png)

2. You can create multiple child folders under the Home Folder. Users can create maximum
of 50 folders for processflow for an organization.
3. Click on the Home folder, the processflow listing page appears on the 
Right side of  the page. Empty folder will have the view as given below.
![Processflow Home3](/staticfiles/processflow/media/processflow-home1.png)
4. Now Click on [Create a ProcessFlow](/processflow/designer-processflow/) button, the ProcessFlow Designer page opens.

### Usability for the SUB/CHILD Folder

* Only **Process Flow** folder will have three horizontal dots (...) that will enable the you to create new child folders.
* Every created folder will have the option - `create a New Child Folder, Rename & delete`. 
* Name of a folder cannot be same if created on same level. However, folder name can remain same if created on different level.

### Steps to create Child Folders inside Process Flow Folder

a.	Click on the ellipsis (...)of the home folder, you can view a **NEW** button.  
![Process Createchild Folder1](/staticfiles/processflow/media/processflow-createchild-folder1.png) 

b.	Click the new button, you will get the window for adding a new child folder. Enter the name of the folder and click on the **Save** button. You get a success message.  
![Process Createchild Folder3](/staticfiles/processflow/media/processflow-createchild-folder3.png)

c. You can view the created folder in the processflow listing page upon expanding the **Home** folder.  
![Process Createchild Folder4](/staticfiles/processflow/media/processflow-createchild-folder4.png) 

d.	Click on the created folder (example - Production), you will get a message for creating new processflows if the folder is empty. 
Otherwise,click on the new button, you'll be navigated to the ProcessFlow Designing Page.  

e.	You can further create child folders for a selected folder by selecting the new option that can be viewed by clicking on the Ellipsis.(...)  
f.	All the created folder will get the options to create a **new** folder, **rename** the folder & **delete** the folder.      
![Process Createchild Folder6](/staticfiles/processflow/media/processflow-createchild-folder6.png)    

g.	Folders on deleting would be moved to Trash with a toaster message for successful completion of the delete process.   


**Note - 
1) Folder name will consist of 50 characters and can have alphanumeric characters. 
Name of a folder cannot be same if created on same level. However, folder name can 
remain same if created on different level.  
2) Full Folder Name is visible by hovering the tool tip over the folder name**

### Steps to Rename a Created Folder

1. You can rename a created folder by choosing the option **Rename** available under
the drop-down of the selected folder.  
![Processflow Rename1](/staticfiles/processflow/media/processflow-rename1.png)  

2. Click on the **Rename**, the window for renaming, opens.     
![Processflow Rename2](/staticfiles/processflow/media/processflow-rename2.png)

3. You can rename using any alphanumeric characters. The renamed folder will 
be available in the ProcessFlow List.    
![Processflow Rename3](/staticfiles/processflow/media/processflow-rename3.png)  


### Steps to Delete a Created Folder

1) You can delete any created folders by choosing the option **Delete**, available in the 
drop-down of the selected folder.  
![processflow-listing9](/staticfiles/processflow/media/processflow-folder-delete1.png)      

2) On clicking the **Delete** button, user gets a confirmation message for the deletion process.  
Click Yes button, you will delete the selected folder.  
![processflow-listing10](/staticfiles/processflow/media/processflow-folder-delete2.png)        

3) Clicking `Yes` button, will delete all its child folders & the processflow present inside it.
The deleted folders will be shifted to the `Trash folder` once deleted from the group level.  
![processflow-listing11](/staticfiles/processflow/media/processflow-folder-delete3.png)

4) Folders can even be deleted permanently from the **Trash** folder, by clicking on the delete button 
for the selected folder under **Trash**. User gets a Confirmation message for deleting permanently.  
![processflow-listing12](/staticfiles/processflow/media/processflow-folder-delete4.png)  

5) Clicking on the Yes button will delete the folder, its processflows and Child folders permanently.    

**The functionality for renaming and deleting is available only for the folders that are created by the user.
The default folders cannot be renamed or deleted.**

## Installed Process Flow folder

This folder will contain the incoming installed packages shared to your organisation. Incoming Packages when installed will be available in the **Installed Process Flow** folder.
The folder will have sub folders created while installing packages, with the same name as that of the installed package. 

To know more on Installed Process Flows, [Click Here](/processflow/processflow-package-installation/)

![installedpffolder](\staticfiles\processflow\media\installedprocessflow.png)

## Package Library folder

This folder will list you with three Sub-Folders : **My Packages**,**Shared With Me** & **Marketplace**. Clicking on **Package Library** folder, you will be shown the summary of packages you have created and shared in both the Sub-Folders.

The Sub-Folders will enable you to perform the following functionalities :

1) **My Packages** : This folder will allow you to Create, Share and View packages created by you on your organisation.

2) **Shared With Me** : This folder will allow you to view and install all incoming packages that are shared with you.

3) **Marketplace** : This folder contains all public packages that you can view & install in your own organisation.

To know more on packaging of processflows, [Click Here](/processflow/processflow-packaging-overview/)

![sharedlistingpage1](\staticfiles\processflow\media\packagelibraryfolder.png)

## Trash Folder 

This folder will list you with all the processflows as well as various folders which you have deleted.

To completely remove processflows from your organisation,you need to perform the following steps :
    
1) Click on the Ellipsis (...) beside the Trash folder, you  can view the button Empty Trash Folder.     
![Trashfolder1](/staticfiles/processflow/media/trashfolder1.png)   

2)	Click on the button **Empty Trash Folder**, you will get a confirmation message. Click on the **Yes** button for deleting all the folder and processflows permanently.  
 ![Trashfolder2](/staticfiles/processflow/media/trashfolder2.png)

3) You can also delete each processflows and folders individually.
 
   a)Click on **Trash** folder,click on the ellipsis of any processflow and finally select **Delete** or **Restore** as required.

   b)In case of folder deletion,select the required folder,click on ellipsis against that folder and finally click on **Delete**.You will get a confirmation message,click on **Yes**.

**Note: You cannot create any child folders under Trash. Default Folders can neither be Renamed nor Deleted.** 


