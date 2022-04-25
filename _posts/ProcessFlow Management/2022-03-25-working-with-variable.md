---
title: "Working with Variables"
toc: true
tag: developers
category: "Processflow"
menus: 
    processflow:
        title: "Working with Variables"
        weight: 8
        icon: fa fa-file-word-o
        identifier: variablesprocessflow
---

APPSeCONNECT processflow allows you to create variables that stores certain values that can be reused in any part of the processflow or in any other processflows designed within your organisation.
Variables are used to store data so that it can be used within a node or processflows. With variables you will not have to provide expressions and generic function multiple times, 
instead you can define the variable with the required expression and deploy it anywhere within the processflow or any other processflow.

For Example : You have created a variable having the name `XYZ` with data type `String` and have associated an XPATH expression `//items/item/customer_id`. 
Once defined, upon calling the variable, it will execute the expression associated with the variable.

### Prerequisites

- You need to have valid credentials to your organisation.
- You need to design a new processflow or you need to have an existing processflow created.
- The variable name should be unique irrespective of the scope used.
- You need to provide the values for the mandatory fields in the **GENERAL** Tab of the Node Configuration Window before creating a Variable.

### Creating Variable

Creating variables in Processflow is easier and can be done directly by dragging the app node
in the [designer section](/processflow/components-of-processflow/). You need to follow the below steps so that you can create variables and take the advantage of them.

1) Select an application node and drag the node to the designer panel where you want to define the variables, the node configuration window appears. You can view two tabs in the node configuration window.
* General  
* Properties  

2) Enter the required details in the [General Section](/getting%20started/create-your-first-processflow/) of the node configuration window. Click on **Properties section** and the screen for variable list appears, if you have created the variable previously. Or else, click on the `CREATE` button. 

![var1](\staticfiles\processflow\media\var1.png)

3) You need to provide the following details in the **Properties Tab** :

- **Variable Name :** This field enables you to provide the name of the variable.
- **Data Type :** Here, you need to select the type of variable that you require. You can select the data type from the drop down. You will be getting the following options in the drop down : `String`,`Bool`,`DateTime`,`Number`,`ComplexObject`,`ComplexObject`,`Double`.
- **Expression :** You can provide either an Xpath or a function expression for it to store against the variable.
- **Default Value :** You can also store a default value against the variable such that if the expression provided results invalid, the default value can be initiated during the execution process of the variable.
- **Scope :** The variable can be executed depending upon the scope defined. The Scope of the variable can be defined within the following type.
    - **Process Flow :** This is the Global variable that can be used in the processflows under any nodes.
    - **Node :** This is the Local Variable and can be used only in the node where it is defined within that processflow.


  You will also be able to view the following toggle button in the `Create Variable` page.
    - **Is Persistant :** On Enabling this toggle button, the value after the execution will be remembered across subsequent executions.
    - **Is Encrypted :** Enabling this toggle will encrypt the output of variable in the database.
  Once all the necessary details are provided. Click on the **SAVE** or **SAVE & CLOSE** button. 

![var3](\staticfiles\processflow\media\var3.PNG)

4) On clicking the `View List` button, you can view all the created variable for the node in a list view.

**Note :** 

- **Variables with datatype `ComplexObect` & `ComplexObjectCollection` cannot be implemented on Action Filter.**

- **The field `Default Value` remains disabled if the datatype is selected as `ComplexObject` or `ComplexObjectCollection`.**

- **When providing the default value for the data type DateTime, the value needs to be provided in ISO format.**

- **The default value for DateTime datatype should be in UTC time.**

- **By default, the toggle buttons will be set to `NO`.**

- **Variable Name should not have any blank spaces in between. You will restricted from saving the variable in such cases.**

Following the above process you can successfully define & Save a Variable.

### Listing of Variables 

Once you have defined and saved the Variable, you will be able to view the list of the variables created. Follow the steps to view the list of variables.

A. Click on the `VIEW LIST` button in the **Create Variable** window after defining and saving the variable.

B. You will be able to view the list of variables in Properties Tab. You can view all the variables that has been created on that node.

C. You will be able to view these following details in the Variable List.

- **Variable Name** - You can view the name provided while defining the variable.

- **Expressions** - You can view the expression used on the variable will be displayed.

- **Data Type** - You can view the datatype used while defining will be displayed.

- **Scope** - You can view the scope of the variable defined will be displayed.

- **Actions** - You can view and perform the following operations from actions : `Edit` & `Delete`.

D. Clicking on the filter icon, you can search a variable from the variable list by providing its name.


### Editing Variable

Editing Variable is equally easy as creating and saving a variable. The process to edit a variable is given below :

A. Open the Application Node Configuration Window where you have defined the variable.

B. Clicking on the Properties Tab, the Variable listing page opens.

![var5](\staticfiles\processflow\media\var5.png)

C. Click on the ellipses icon (Three horizontal Dots) on the **Actions** column beside the variable. You'll get two options from the drop down.
- Edit : Enables you to make any changes to the created variable.
- Delete : Deletes the created Variable.

D. Click on the EDIT button. You can view the `Create Variable` page. Modify the changes that are required and click on the SAVE button.

**Note :** You can modify only **Expression** and **Default Value** fields.

### Deleting Variable

Deleting a variable is an essential part of processflow development so that you make necessary changes.

A. Open the Application Node Configuration Window where you have defined the variable. Click on the ellipses button beside the Variable, in the variable listing page.

B. Click on the Delete button available on the drop down window. 

![var6](\staticfiles\processflow\media\var6.PNG)

C. You'll be getting a confirmation message for the deletion process.

![var7](\staticfiles\processflow\media\var7.PNG)

D. Your variable gets deleted from the list.

_**Note :** You cannot delete a Variable that is currently in use for execution and will be provided with an error while doing so._

### Execution Flow of Variable

1) [Design the processflow](/getting%20started/create-your-first-processflow/) and Open the **Node Configuration Window** for the application implementing [GET operation](/processflow/processflow-app/#working-principle-for-getpost-node). The node configuration window opens.

2) Enter the required fields in the **General Tab** of the Node Configuration Window of the application implementing GET operation. Click on the **Properties** Tab.

![var8](\staticfiles\processflow\media\var8.PNG)

3) Click on the [**Create**](/processflow/working-with-variable/#creating-variable) Button in the Properties Window. The Variable creation page opens, enter the required details and click on the save button.

![var9](\staticfiles\processflow\media\var9.png)

4) Navigate to the General tab and click on the **Configure Filter** button. Expand the Action filer node, enter `created_at` in the key field and `variable name` in the value field. To know more about Actions & Action Filters, [Click Here](/transformation/working-with-schemas-action-filter/). Finally, click on the save button.

![var11](\staticfiles\processflow\media\var11.png)

5) You can now successfully [deploy and execute](/processflow/deploying-and-executing-processflow/) the processflow. You can also view the [snapshot](/processflow/snapshot-processflow/) of the processflow after successfully deployment and execution.

![var12](\staticfiles\processflow\media\var12.png)

6) Click on the [`File Tab` of GET node](/processflow/snapshot-processflow/#1-scenario-get-node) to view all the files fetched after the date that is provided in the variable.

![var13](\staticfiles\processflow\media\var13.png)

7) You can also view the Activity Logs of GET Node in the snapshot for viewing the variable implementation logs.


**Note:**

- Generic Function for `Lastof` has been used for fetching all data after the LastOf value provided. After an instance, the generic function will store the `created_date` value of the last data such that on the next execution, all the data after the `LastOf date` will be fetched.
- You need to provide `~ (tilt icon)` when providing Generic function in the `Expression` field both at front and back.
- Using of the `$` symbol along with the Curly Braces `{}` is mandatory for identifying the variable usage.
- Variables with datatype `ComplexObect` & `ComplexObjectCollection` cannot be implemented on Action Filter.
- You will be provided with a Error Message in the **Activity Logs**, if the provided variable is syntactically wrong or has failed to execute.

### Utility of Variables

This part of the document will list few scenarios that will help you understand the usablity of Variables :

| Variable Name | Datatype | Expression | Default Value |Scope| Utility|
|--------|-------------|-------------|---------|-------|-----|
| custxp | string | `{//items//item/` <br/> `cust_id}` | - |  ProcessFlow or Node | Here, the variable is created with the name `$custxp` and is provided with an xpath expression. When ever the variable is called within the scope, the expression provided in the variable will be executed. |
| countryval | string | `{//items//item/` <br/> `country_id}` | ProcessFlow or Node |`"NY"` | Here, a variable is created `${countryval}` that stores a static value of sting type. On the applying the variable on Action Filter of GET node, the variable will execute the expression provided and fetch only those data, that matched the value provided in the variable.|
| Email | Bool | `{//items//item/ ` <br/> `email_id}` | True |ProcessFlow or Node|Here, the variable is created of the data type Boolean and is provided with both Expression and a default Value. On implementing the Variable on Action Filter for GET operation will fetch only those data that contains the email.|
| IsGuest | Bool | `{//items//item/ ` <br/> `country_id}`| True| ProcessFlow or Node|Here, the variable is created of the data type Boolean and is provided with both Expression and a default Value. On implementing the Variable on Action Filter for GET operation will fetch only those data that contains the value TRUE against the attribute country id.|
|TotalSpent| Double | `{//customers/customer` <br/> `/total-spent}`  | 55.55 | ProcessFlow or Node | Here, the variable is of the datatype `Double` is provided with default value. On implementing the variable in the action filter of Shopify operating GET, all the data whose `total-spent` value equals the variable default value will be fetched.|
|Frieght| Double | `{//items//item` <br/> `//addresses/frieght}` | 6.25 |processflow or Node| Here, the variable frieght is declared with an expression and a default Value. On implementing the Action filter Operating GET for Magento2, all the data with frieght value 6.25 will be fetched.|
|LastData| DateTime | `~{gen:LastOf(//items` <br/> `/item/created_at)}~`|2020-07-08 06:31:35|processflow or Node | Here, generic function is used as an expression and default value is provided as a Date Time  value which signifies that, the last record fetched will be upto the provided DateTime.|
|FirstData| DateTime | `{//items/item/` <br/> `created_at}`|2020-07-06 04:45:35 |processflow or Node|Here, the expression and value used will fetch a specific data that matches the given value, when the variable is used in the action filter.|
|ZipCode|Number|`~{gen:FirstOf(` <br/> `//customers/` <br/> `/customer//` <br/> `addresses/zip)}~`|10001|processflow or Node|Here, the variable is created with a generic function is provided  as an expression. The variable is implemented on the action filter of Shopify GET node that will fetch all the customers who zip code contains 10001.|
|GrpCode|Number|`~{gen:FirstOf(` <br/> `//items//item/` <br> `group_code)}~`| 1 |processflow or Node| Here, the variable is created with a generic function as an expression. The variable is implemented on the action filter of Magento2 GET node that will fetch all the data whose Group Code matches the value provided in the variable.|