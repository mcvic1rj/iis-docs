---
title: "HttpLoggingSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 28d7825f-54f6-d715-c32b-13d911e6763d
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# HttpLoggingSection Class1
Configures the logging of HTTP requests.  
  
## Syntax  
  
```vbs  
class HttpLoggingSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `HttpLoggingSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `HttpLoggingSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DontLog`|A read/write `boolean` value. `true` if logging is disabled for successful requests; `false` if successful requests are logged. A request is considered successful if its status code is less than 400. The default is `false`. **Note:**  This property is the same as the [DontLog](http://go.microsoft.com/fwlink/?LinkId=73544) metabase property in IIS 6.0.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`SelectiveLogging`|A `sint32` enumeration that specifies the events to log. The possible values are listed later in the Remarks section.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class corresponds to the `<system.webServer/httpLogging>` section in the ApplicationHost.config file.  
  
 The following table lists the possible values for the `SelectiveLogging` property. The default is 0 (`LogAll`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`LogAll`|All requests are logged.|  
|1|`LogSuccessful`|Only successful requests are logged. A request is considered successful if its status code is less than 400.|  
|2|`LogError`|Only failed requests are logged. A request is considered failed if its status code is greater than or equal to 400.|  
  
## Example  
 The following code example sets the `SelectiveLogging` property to `LogError`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the HTTP logging section.  
Set oSection = oWebAdmin.Get( _  
    "HttpLoggingSection.Path=" & _  
    "'MACHINE/WEBROOT/APPHOST',Location=''")  
  
' Display the class name of the section.  
WScript.Echo "[ " & oSection.Path_.Class & " ]" & vbCrLf  
  
' Display the initial settings.  
Call DisplaySettings("Initial Values", oSection)  
  
' Set the SelectiveLogging property to LogError.  
    oSection.SelectiveLogging = 2  
  
' Save new values to configuration.  
oSection.Put_  
  
' Refresh the oSection object variable with new values.  
oSection.Refresh_  
  
' Show changed settings.  
Call DisplaySettings("New Values", oSection)  
  
' ==== DisplaySettings helper function. ====  
Function DisplaySettings(HeadingText, oSection)  
  
    ' Display a heading.  
    WScript.Echo String(Len(HeadingText), "-")  
    WScript.Echo HeadingText  
    WScript.Echo String(Len(HeadingText), "-")  
  
    ' Display configuration history section properties.  
    WScript.Echo "Path: " & oSection.Path  
    WScript.Echo "Location: " & oSection.Location  
    WScript.Echo "DontLog: " & oSection.DontLog  
    WScript.Echo "SelectiveLogging: " & _  
        oSection.SelectiveLogging  
    WScript.Echo  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `HttpLoggingSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CentralBinaryLogFile Class](../../reference/admin/centralbinarylogfile-class1.md)   
 [CentralW3CLogFile Class](../../reference/admin/centralw3clogfile-class1.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [OdbcLoggingSection Class](../../reference/admin/odbcloggingsection-class1.md)   
 [LogSection Class](../../reference/admin/logsection-class1.md)   
 [SiteLogFile Class](../../reference/admin/sitelogfile-class1.md)   
 [DontLog Metabase Property (IIS 6.0)](http://go.microsoft.com/fwlink/?LinkId=73544)