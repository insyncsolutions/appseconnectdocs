---
title: "Defining Variables in Mapping"
toc: false
description: "Get to know about mapping variables and its implementation."
keywords: "mapping variable"
tag: developers
category: "Processflow"
menus: 
    mapperprocessflow:
        title: "Defining Variables in Mapping"
        weight: 6
        icon: fa fa-file-word-o
        identifier: xpathnmappingprocessflow
---

Just like [ProcessFlow variables](/processflow/working-with-variable/), mapper also uses variables extensively. 
The Variables in mapper gives you temporary storage such that you can define and use it in various areas of your script as per your requirement. 
In case of Mapper, the Variable is accessed using a `$` sign, which replaces the variable name with the current value of it.
Here you will understand the process of defining [Variables](/transformation/types-of-variable/) (any variables that stores the data that can be used later within 
the process of transformation) and then mapping of variables during transformation phase. 

Here The flow is explained using `Root Variable` for a processflow.   
**NOTE- The process of defining the variables remain same for any type of variable.**

## Prerequisites for using Variables in Processflow Mapping

* You need to have valid credentials of the portal to login to your organization.
* You need to navigate to the [Process Flow listing page](/processflow/processflow-listing-page/) for creating or editing a ProcessFlow. 
* You need to have the basic ideas of defining the logics in [mapper node](/processflow/working-with-mapper/).
 
#### Adding Variables

1. Open a processflow from [Process Flow listing page](/processflow/processflow-listing-page/). 
Click on the Node Configuration button of the Mapper node. The Mapping Configuration window opens up where you can provide the necessary mapping for your business integration. 

2. Click on the ellipsis beside the `Root Variable`. Select the `Add Variable` option present. 
![mapping_variable1](../../staticfiles/processflow/media/mapper/mappingvariable_1.png)

3. Input the following details Variable Name, Data Type, Scope, Default Value, Is Persistant and Is Encrypted.                
![mapping_variable2](../../staticfiles/processflow/media/mapper/mappingvariable_2.png) 

(a) In this case, Variable Name is `CardCode` whose Data Type provided as `String`. The flow remains same for the 
Data type -  Bool, Datetime, Number and Double.  
(b) While using Complex Object or Complex Object Collection as Data Type for any variable providing the XPATH is mandatory.  

Once the details are filled, click Save. 

#### Mapping for Variables

1. For Mapping the variable, expand the ellipsis corrosponding to the variable that you have created. Click on **Do Mapping** and the mapping window appears. 
2. In the mapping window, implement the mapping for corrosponding variable. Select the function from the `Functions List` and click on the function as required.   
3. Click on the Save button. The mapping will be saved for the respective variable and a toaster message will be displayed confirming the same.
>The mapping can be executed with the functions as well as, with the source attributes. Implementing mapping only with the functions is not mandatory.

![mapping_variable3](../../staticfiles/processflow/media/mapper/mappingvariable_3.png)

The user can view the successful sync of the processflow for which the Variables was created.

#### Deleting variable

The user can delete the Variables whenever required, any-time after its creation. 
Expand the ellipsis of a variable and click on `Delete Variable` button. A pop-up will appear, on clicking `Yes` the variable will be deleted. A toaster message will be displayed at the botton right corner confirming the deletion of the selected variable. Else, click `No` to abort the deletion process. 
![mapping_variable4](../../staticfiles/processflow/media/mapper/mappingvariable_4.png)

>You need to remove the mapping corrosponding to the variable, in order to delete the varaible.

#### Editing Varibale

The user can edit the variables defined any-time after its creation by clicking on `Edit Variable` button. 

Expand the ellipsis of a variable and click on `Edit Variable` button. 
![mapping_variable5](../../staticfiles/processflow/media/mapper/mappingvariable_5.png)

Make the necessary changes in **Variable Name**, **Data Type**, **Scope**, **Default Value**, **Is Persistant** and **Is Encrypted**. Click on **Save** and the changes will be reflected.
![mapping_variable6](../../staticfiles/processflow/media/mapper/mappingvariable_6.png)

#### Attribute Mapping with Mapping Variable

Since mapping variables is used to store the value temporarily in a transformation process, so you can use 
the mapping variables in attribute mapping by following the below mentioned steps.

1. Click on the ellipsis of the attribute where you want to use the mapping variable. Select `Do Mapping`. 
2. The transformation window for the selected attribute opens up.
![mapping_variable7](../../staticfiles/processflow/media/mapper/mappingvariable_7.png)

3. Click `+` to expand Mapping Variables. Select any variable under `Mapping Variables` and click on **Save**. 
You will observe the mapping variable in the transformation window corrosponding to the selected attribute.
![mapping_variable8](../../staticfiles/processflow/media/mapper/mappingvariable_8.png)


