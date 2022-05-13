---
title: "Working with Functions"
description: "Learn how to use our default and user defined functions."
keywords: "generic function, native function, user-defined function, cloud function"
toc: true
tag: developers
category: "Processflow"
menus: 
    mapperprocessflow:
        title: "Working with Functions"
        weight: 8
        icon: fa fa-file-word-o
        identifier: different functions
---

**Functions** are small piece of executable code which is used from various sections of APPSeCONNECT to perform complex activity on data. 
These functions in APPSeCONNECT are libraries that enables you to implement any repeatable complex algorithm in mapping,action filter,variables,rules etc. 
They gives more power to the implementor as they are written in high level language,capable of calling different APIs through functions which are not accesable by mapping.
In APPSeCONNECT, you can use the following Appresource Functions :

## Generic Function

Generic functions are utility functions capable of performing some basic manipulation of data. 
They are defined and delivered by APPSeCONNECT product team and are accessible to any project on the platform.  

|Function_Name|Description|Example|
|-----------------------|---|----------------------|
|GetLocalDateTime(format)|Gets the local date time|[genericlib:GetLocalDateTime('yyyy-dd-MM')]|
|Base64Decode(base64String)|Base64Decode(base64String)|Base64Decode(base64String)|
|Base64Encode(dataString)|Encodes the data into base64 encoded string|[genericlib:Base64Encode(dataString)]|
|ReformatToDecimal(data)|Reformats a decimal value using the number format specified to local environment|[genericlib:ReformatToDecimal(data)]|
|GetContextualDataObject(key)|Gets a contextual data for a particular sync operation|[genericlib:GetContextualDataObject(key)]|
|SetContextualDataObject(key,value)|Stores contextual sync data|[genericlib:SetContextualDataObject(key, value)]|
|ReplaceAllCharacters(data,characters,replacechar)|Replaces a set of characters from data with a replacement string|[genericlib:ReplaceAllCharacters(data,characters,replacechar)]|
|GetBase64String(data)|Gets base64 string from a data|[genericlib:GetBase64String(data)]|
|GetStringFromBase64(data)|Gets a data from a base64 string|[genericlib:GetStringFromBase64(data)]|
|FormatByCulture(data)|Formats a data to local culture string|[genericlib:FormatByCulture(data)]|
|GetShortUniqueId()|Gets short hand representation of a globally unique identifier|[genericlib:GetShortUniqueId()]|
|GetMappingOrDefault(value,type)|Gets a look up type for a specific value or return the value itself|[genericlib:GetMappingOrDefault(value,type)]|
|GetIntFormattedOutput(data,formatspecifier,defaultvalue)|Returns the formatted output for an integer data passed in or the default value specified|[genericlib:GetIntFormattedOutput(data, formatspecifier, defaultvalue)]|
|GetDoubleFormattedOutput(data,format,defaultvalue)|Returns the formatted output for a double value or the default value specified|[genericlib:GetDoubleFormattedOutput(data, format, defaultvalue)]|
|TimeFromParts(hour,minute,seconds,fractions,precision)|Creates a time from values passed in as parameter|[genericlib:TimeFromParts(hour,minute,seconds,fractions,precision)]|
|GetDataFromStore(key,objecttype)|Gets data from storage for a unique key and object type|[genericlib:GetDataFromStore(key,schema)]|
|SetDataToStore(key,value,objecttype)|Saves data by key and object types|[genericlib:SetDataToStore(key,value,objecttype)]|
|GetUniqueId()|Generates a globally unique identifier|[genericlib:GetUniqueId()]|
|IsDate()|Checks whether the string is a valid date|[genericlib:IsDate()]|
|DateDifference(date1,date2,range)|Gets difference of two dates in terms of range value. Valid string values of range is "month", "day" or "year". The difference is calculated based on the range passed in|[genericlib:DateDifference(date1,date2,range)]|
|DateFromParts(year,month,day)|Creates a date from values passed in|[genericlib:DateFromParts(year,month,day)]|
|GetUtcTime()|Converts a local time to universal time|[genericlib:GetUtcTime()]|
|GetUniversalDateTime(format)|Gets a string representation of universal time|[genericlib:GetUniversalDateTime(format)]|
|FormatDate(date,format)|Changes format of a particular date|[genericlib:FormatDate(date,format)]|
|GetCurrentEntityData()|Returns an XML representation of APPSeCONNECT generated entity bucket|[genericlib:GetCurrentEntityData()]|
|GetLocalTime(datetime)|Converts an UTC date time to local datetime equivalent|[genericlib:GetLocalTime(datetime)]|
|GetLowerString(data)|Converts the data to a lower string case|[genericlib:GetUpperString(data)]|
|GetTitleCaseString(data)|Converts data to title case string|[genericlib:GetTitleCaseString(data)]|
|WrapInCData(data)|Wrap the data passed to a CData construct|[genericlib:WrapInCData(data)]|
|GetDataOrDefault(data,defaultText)|Gets the string equivalent of data passed or default text|[genericlib:GetDataOrDefault(data,"insync")]|
|GetDateFormattedOutput(data,formatspecifier,defaultDate)|Gets formatted date based on Format specified or default date passed|[genericlib:GetDateFormattedOutput(data,"dd/mm/yyyy","01/01/2010")]|
|RegexReplace(data,regex,replaceString)|Replaces the data string using a regular expression with either nothing or with the replacestring passed|[genericlib:RegexReplace(data,"[a-z]+"," ")]|
|TrimAllCharacters(data,characters)|Converts data to string and removes all characters passed in|[genericlib:TrimAllCharacters(data,"$@^")]|
|TrimSpaceAllSides(data)|Converts data to string and removes all leading white spaces|[genericlib:TrimSpaceAllSides(data)]|
|GetDoubleFormattedOutput(data,formatspecifier,defaultDate)|Gets formatted double based on Format specified or default double value passed|[genericlib:GetDoubleFormattedOutput(data,"%00d","30")]|
|getMapping(ObjectType,Value)|Gets value mapping for a particular type from either source or destination|[genericlib:getMapping("Currency" ,"$")]|
|GetUpperString(data)|Converts the data to an upper string case|[genericlib:GetUpperString(data)]|

**Note : Click [here](/transformation/using-library-methods/) to know how to use generic functions in your processflow.

## User Defined Function

The User - defined functions are used while creating or editing a processflow. These functions are written within the cloud portal itself. The user-defined function are referred by *cloudResourcelib.** You can create and use such functions by following the below mentioned steps.

###### Steps to Implement User-Defined Functions for ProcessFlow :

a.	Create a new ProcessFlow or open an existing ProcessFlow for which you need to implement user-defined functions. 
![cloud1](/staticfiles/processflow/media/mapper/cloudfunction1.png)    
b. Click on the Node Configuration icon for the Mapper Node. The Mapper/Transformation window for that Process flow opens. Expand the [transformation node](/transformation/getting-started-with-mapping/#structure-of-mapping). 
**Open** the attribute for which you need to implement and map the function. Expand the Function node to view **Cloud** sub node.
![cloud2](/staticfiles/processflow/media/mapper/cloudfunction2.png)  
c. Click on **Blue coloured ADD (Plus Symbol) icon**,the code editor window opens up where you can create/edit your own function.
d. Provide the **Description** and **Example** to the user defined for easy user reference as why and how the function is needed to be implemented.
![cloud5](/staticfiles/processflow/media/mapper/cloudfunction3.png)  
e. The user can choose from the **Code snippet template** and **language fundamentals templates** also. The templates can be added in the code panel by drag and drop. 
![cloud6](/staticfiles/processflow/media/mapper/cloudappresource-6.png)  
f.	Code the Appresource and click on **Validate**. In case of error, validator will provide the area of the cause in the error message as shown below. 
![cloud7](/staticfiles/processflow/media/mapper/cloudappresource-7.png)  
g. Once validated successfully, close the Code validator screen & click on the **SAVE** button.
h.	Expand the Cloud appresource Node for viewing the created function. Clicking on any of the function, will make it appear in the mapping Panel. You can also click on the **edit button** available beside the function name in the tree node, for making changes in the created Appresource function.
![cloud8](/staticfiles/processflow/media/mapper/cloudappresource-8.png)  
i. Once the mapping is done, click on the **Save button** to save the mapping.
Following the process, you can successfully create & define a Process Flow.  

**_Note:_**

- Cloud Appresource functions can be created from Process Flow Mapper Node level & from [App level](/accessing%20portal/accessing-portal/#b-choosing-app).

- You need to define Cloud Appresource every-time while working with Mapper node for a new Process Flow.

- Also, you need to define the Cloud Appresource every-time while working with Multiple Mapper nodes.

- Cloud Appresource created & defined in App level of your organisation will be available when the app is used in the Process Flow, you need not have to create & define a new function.


## Native Function

These are powerful functions defined within the adapters such that they can be used in our platform to retrieve and post data to respective business application. 
To know,how to use source and destination function during transformation click [here](/transformation/using-library-methods/).

