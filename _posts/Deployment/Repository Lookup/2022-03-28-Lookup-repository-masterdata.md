---
title: "Lookup Repositories"
toc: true
tag: developers
category: "Deployment"
menus: 
    deployment:
        title: "Creating Repository Collection & Reference Tables"
        weight: 1
        icon: fa fa-file-word-o
        identifier: lookuprepoprocessflow
---

Repositories in APPSeCONNECT provides the user to create and manage Lookups in form of reefrence tables 
for the organisation. Lookups enables the user to provide specific values to the application 
integration, such that when the source and destination application is integrated, the value in 
source application can easily be integrated with its value in destination application, corresponding
to its field. Having independent repositories for lookups will help the users to create Lookup collections 
and manage them in separate refernce tables as per their need. Each Repository Collection created will 
multiple have **reference tables** that will enable the users to store and manage the collection 
of Lookup References.

## Prerequisites

* Should have an organisation created in APPSeCONNECT.
* User should have valid credentials for login to the APPSeCONNECT Credentials.

### Steps to Create Repository Collections

1.	Login to the portal and navigate to **Manage > Repositories**. You can view Repository landing page, if creating for the first time.  
![Create Lookrepo1](/staticfiles/processflow/media/create-lookrepo1.png)   

2.	Click the button to Create a new Repository Collection. The window for providing the name for the Repository Collection opens.  Enter the name for the Repository Collection and click on the **SAVE** button.  
![Create Lookrepo3](/staticfiles/processflow/media/create-lookrepo3.png)  

3.	On clicking the **Save** button,you can view **Repository** page and the created Repository Collection will be present in the tree. You can also create another Repository Collection by clicking the `New` button.  
![Create Lookrepo4](/staticfiles/processflow/media/create-lookrepo4.png)  

4.	You will get the same view of the window as given in the previous steps to create multiple repositories.    

**Note : You cannot create multiple Repository Collection with same name. Following the above process, you can successfully create multiple Repository Collection.**

## Reference Tables

Reference tables are the collection of lookup references which can be created under each Repository Collection. The steps for creating **reference tables** are given below.

### Steps to create Reference Tables

1.	Login to the portal and navigate to **Manage > Repositories**. On clicking over the ellipsis icon (...) beside every Repository Collection, user gets the following options.  
a.	Edit : You can **rename** the collection by clicking Edit Button.  
b.	Delete : You can delete the whole Repository Collection including the tables inside it, by clicking on delete button.   
c.	**[Import](/deployment/export-and-import-lookup/#steps-to-import-lookups-from-repository-collection) : You can import an excel file for creating reference tables from your local system.**  
d.	**[Export](/deployment/export-and-import-lookup/#steps-to-export-lookups-from-repository-collection) : You can export the created lookups to your local system.**    
e.	New Table : You can create a new table under the selected Repository Collection by clicking on new table.  
f.  Clear All : You can clear all the data of the Repository Collection by clicking on this option. You will get a warning message,click `Yes` to proceed, else click `No` to cancel.    
![Reference Table2](../../staticfiles/processflow/media/reference-table2.png)

2.	Click `New Table` button and you will get the window for naming the table. Input the table name and click on **Save** button. 
![Reference Table4](../../staticfiles/processflow/media/reference-table4.png)  

3.	You can view the created table under the selected Repository Collection. Click over the table, you will view the following. 
![Reference Table5](../../staticfiles/processflow/media/reference-table5.png)  

4.	Click  `Add New` button, for creating new lookups under the selected Reference Table. The Add New Lookup wizard opens up with the following fields. Click  **Save** button once the details are provided.  
a.	Source : Need to provide the source value.   
b.	Destination : Need to provide the destination value.  
c.	Comments : You can provide short descriptions for identifying the lookups workaround.      
![Reference Table7](../../staticfiles/processflow/media/reference-table7.png) 
**The Source and the Destination is a mandatory field for saving the lookup.**
**Maximum length for entering the Values in Source & Destination field is of 100 Characters.** 

5.	You can view the lookup created under the selected Reference Table. 
The Reference Table page of the selected table will list all the lookups created in the form of Table Rows.
The page will display these columns.  
a.	Source  
b.	Destination   
c.	Description   
![Reference Table8](../../staticfiles/processflow/media/reference-table8.png)    

6.	Every lookup in table rows are editable. Clicking on each cells of the table rows will enable you to edit all the three fields. Clicking on the Tick icon will update the changes made for the lookup. You will get a confirmation message for updating successful. The Cross icon will cancel the operation. You will also get a Delete option, when clicked on the Ellipsis icon (...) beside each table rows. 
![Reference Table9](../../staticfiles/processflow/media/reference-table9.png)     
7.	a)User can create multiple lookup rows by clicking on the New button available on the top right of the page.
    Although User cannot create multiple Lookup Table Rows with same Source values under a single Reference Table.
    b)	You can filter rows by implementing search. The search function 
will filter options available with the selected Reference Table.  
**Note: User cannot create multiple Lookup Table Rows with same Source values under a 
single Reference Table.** 

![Reference Table12](../../staticfiles/processflow/media/reference-table10.png)    

Following the above steps, you can successfully `create multiple Repository Collections` and `Reference Tables` inside it.

