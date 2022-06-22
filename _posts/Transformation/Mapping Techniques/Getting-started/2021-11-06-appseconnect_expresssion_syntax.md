---
title: "APPSeCONNECT Expression Language"
toc: true
description: "APPSeCONNECT enables you to perform various types of mapping during transformation."
keywords: "types of mapping,mapping types"
tag: developers
category: "Transformation"
menus: 
    mappinggettingstarted:        
        title: "APPSeCONNECT Expression Language"
        weight: 3
        icon: fa fa-wpexplorer
        identifier: typesofmapping
---

Transformation is one of the major step to any integration solution as different `APIs` consume different structures in terms of data 
and format. Every transformation you perform over data requires extensive implementation of business logic. 
The integration platform provides capabilities to map the data sources such that destination consumable schemas can be generated. 
`APPSeCONNECT` provides its own language and syntax which gives you as an integration specialist 
a way to define your business logic. The language which you write to transform the data from one data format to another is `APPSeCONNECT Expression langauge`.

Behind every application integration, there is a business logic. APPSeCONNECT stores this integration 
logic in the form of data. Attribute mapping forms the main part of transforming data from one format 
to another format. In the following sections, we will guide you through APPSeCONNECT Expression langauge, different types of mapping and how they 
are important in performing tasks such as customizations and alterations with the change in business requirement. 

## Prerequisites

Before going deep into different types of mapping, you need to know the following in details. 

* [Types of Variable](/transformation/types-of-variable/)

* [Understanding XML & XPATH](/transformation/understanding-xml-and-xpath/)

* [Working with Schema Attribute & Action](/transformation/working-with-schemas-action-filter/)

## Types of Syntax Used in APPSeCONNECT

APPSeCONNECT Expression Language provides three types of syntaxes to perform free and smooth transformation.

### Double Curly Braces 

Double Curly Braces is used to evaluate the data in an XML document. Any Xpath expression that you provide inside Double Curly Braces 
will be evaluated. This can also be used to evaluate the simple XPATH methods. Double Curly Braces is denoted by **\{\{ \}\}**. 
You can use this syntax during transformation to implement the business logics in the following ways. 

![doublecurlybraces](/staticfiles/Transformation/media/doublecurlybraces.png)

>You can use any attribute, xml function, complex xpath, or variable inside Double Curly Braces .

### Single Squared Bracket Syntax 

Single Squared Bracket is used to call external functions as well as expression synatxes. While using [generic function](/processflow/Working-with-functions/#generic-function), source functions 
destination function and choose-when mapping, you need to use `Single Squared Bracket`. `APPSeCONNECT` also provides the usage of **case statement**. In order to case statement, 
you need to use this syntax as well. Single Squared Bracket is denoted by `[]`. During transformation, you can use this syntax to implement the business logics in the following ways.

![singlesquraedbraces](/staticfiles/Transformation/media/singlesquraedbraces.png)

#### choose-when mapping

`choose-when` mapping is a type of case statement, analogous to `if-else` statement used in mapping. This type of statement is essential 
when you want the value of a field of the destination schema to be conditionally dependent on the value of the corresponding field of the source schema. 
In other words, the value of the destination field would depend on the source field, such that for every different value 
of the source field, there is a corresponding value for the destination field. 

Take the analogy of the `if-else` statement to understand this. 
Say, you want to set up the value of a variable `x` such that it depends on another variable `y`. 
If the value of `y` is 1, `x` will be 2, if `y` is 3,
`x` will be `100` and so on.

Similarly, consider the `customer entity` and you are transferring data from the source application to the destination application. 
Suppose, you want the value of the `country` field from the source schema to be mapped with the same field of the destination schema. 
However, you want to setup such that, if the country is `USA` in the source application, in the destination application it will be 1. 
On the other hand, if it is `India`, at the destination it will be `2`. In such a case, we deploy `choose-when` mapping.

The generalised structure of the `choose-when` condition is :

`[choose][when](condition)statement[endwhen][otherwise]statement[endotherwise][endchoose]`

>You can also use `Double Curly Braces` inside Single Squared Bracket but the reverse is not possible.

### Special Language Syntax 

These are special syntaxes that lets you define complex object expression in simple terms. You can use this syntax while peforming [look up mapping](/deployment/implementing-lookup-in-mapping/#steps-to-implement-lookup-in-attribute-mapping) in mapper. 

![speciallanguagesyntax](/staticfiles/Transformation/media/speciallanguagesyntax.png)


## Different Mapping Types available in APPSeCONNECT

### Hard Coded Mapping 

Hardcoded mapping is implemented when it is required that a field of the destination schema bears a 
constant value such that the value of the field does not change with every transformation carried out.

As an example, if a customer wants every business partner, added from the source to the destination application to come with a flag of constant value, 
then he can deploy hard-coded mapping.

### Field to Field Mapping 

Field to Field mapping is required when your business demands mapping a field of the destination schema to directly fetch 
its value from the source schema. 

As an example, if you want the `Customer` schema of SAP B1 to fetch the value of the field `Country` directly from the country field of the source schema, 
you can map the `country` field of both the schemas.   
![field-field-mapping](/staticfiles/Transformation/media/field-field-mapping.png)       
For this example, let us say, you wish to map the destination field `email` with the source field `email` of the schema `customer`. 
These fields exist as nodes in the corresponding XML document. Then you can directly map the fields together, by providing the name 
of the source field in the destination field. However if you wish to map the field `PIN` of the destination field, you cannot access the node directly. 
The node `PIN` exists as a child node of the parent node `shipping` and `billing` which in turn are child nodes to the node 
`address`. 

- **Direct field mapping** - To access the node `PIN`, we provide the entire path up to the node so that it can be accessed.    
- **Field mapping via XPATH** - To access the node `PIN` of the node `billing`, we provide the following XPATH as address/billing/PIN.  

### Function Mapping 

Prerequisite : Knowledge about [AppResource functions](/transformation/using-library-methods/).

* AppResource functions can be deployed for facilitating the required data transformation between the source and destination application.
* To use AppResource functions you only require to know the fields/variable you desire to map along with the name of the function.
* To understand the utility of these functions let us look at the example below.
Suppose when developing a particular processflow, you come to learn that, destination application accepts date time in a different format 
what is sent by the source application. Let the accepted date time format be like "yyyy/MM/dd HH:mm:ss" and received format be like "dd-MM-yyyy". To get around this dilemma, we use AppResource functions.

Refer this [link](https://www.youtube.com/watch?v=mwcLjXwu6fQ&t=0s&index=5&list=PLSZUUcH5fP9_msXnLwdGp0Mb4Bu0i0g-y) to know in details about functional mapping. 

### Query Mapping

As the name suggests, Direct Query mapping is actually running a query in the source schema so as to store the resultant data from the query in the destination field.
For example, when we run a SQL query we provide the name of the field whose result we require, the name of the table from where the data is to be fetched and the parameters, on the basis of which the results would be filtered.

Structure of an SQL query is : select `name` from `student` where `rollno` = 1.
`Name` is the output field, `student` is the schema and `rollno` is the parameter whose value we are checking to filter the data.
We use a similar format when we wish to fetch data from the source or destination schema in APPSeCONNECT. 
We provide the name of the desired field, the schema and the parameters in the query.

The native AppResource function that we use for this purpose is 'sourcelib' or 'destinationlib' depending on from where we wish to receive the data.
`Structure of a query in mapping is`
destinationlib:GetUniqueId(",",",") where we provide the required field, the schema and the parameters in order.

### Variable Mapping 

Click [Variable Mapping](/transformation/defining-variables-in-processflow-mapping/) to know in details.

### LookUp Mapping 

Click [Lookups Mapping](/deployment/implementing-lookup-in-mapping/#prerequisites-for-mapping-lookups) to know in details.


