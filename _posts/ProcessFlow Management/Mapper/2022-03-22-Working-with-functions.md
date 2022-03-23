---
title: "Working with AppResource Functions"
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

**Appresource Functions** are the functions in APPSeCONNECT that are written in the adapter(APPSeCONNECT supports calling external functions written in C# inside the adapter) which is used for the data transformation from the source Application to the Destination Application. 
In APPSeCONNECT, you can use the following Appresource Functions :

1)**Generic AppResource Functions** - The generic appresources are the functions that have general defined task which are provided by APPSeCONNECT itself. APPSeCONNECT supports following generic functions.

|Function_Name|Description|Example|
|----------------------|---|----------------------|
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

**Note : Click [here]](/transformation/using-library-methods/) to know how to use generic functions in your processflow.

2)**Cloud Appresource** -  The Cloud Appresources are the functions that are used when creating or editing a processflow. These functions are written within the cloud portal itself. The function of the cloud appresources are referred by *cloudResourcelib.**

**Note : Click [here]](/transformation/using-library-methods/) to know how to use generic functions in your processflow.

3)User-Defined Function - 

