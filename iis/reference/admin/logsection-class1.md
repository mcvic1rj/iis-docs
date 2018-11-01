---
title: "LogSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: cc93d19f-64ef-2ee5-5266-93f14570d30c
caps.latest.revision: 25
author: "shirhatti"
manager: "wpickett"
---
# LogSection Class1
Configures the logging for a server or site.  
  
## Syntax  
  
```vbs  
class LogSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `LogSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `LogSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`CentralBinaryLogFile`|A read/write [CentralBinaryLogFile](../../reference/admin/centralbinarylogfile-class1.md) value that specifies the configuration of centralized binary logging for all sites on a server.|  
|`CentralLogFileMode`|A read/write `sint32` value that specifies the centralized logging mode for the server. The possible values are listed later in the Remarks section.|  
|`CentralW3CLogFile`|A read/write [CentralW3CLogFile](../../reference/admin/centralw3clogfile-class1.md) value that specifies the configuration of World Wide Web Consortium (W3C) centralized logging for all sites on a server.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`LogInUTF8`|A read/write `boolean` value. `true` if IIS logs all strings in UCS Transformation Format 8 (UTF-8); otherwise, `false`. The default is `true`. This setting applies serverwide to all text-mode logging.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class corresponds to the `<system.applicationHost/log>` section in ApplicationHost.config.  
  
 The following table lists the possible values for the `CentralLogFileMode` property. The default is 0 (`Site`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Site`|All client requests are logged at the site level, not centrally at the server level. Log files are generated per site.|  
|1|`CentralBinary`|All client requests for all sites are logged to a single log file in centralized binary format on the server.|  
|2|`CentralW3C`|All client requests for all sites are logged to a single log file in W3C centralized format on the server.|  
  
## Example  
 The following code example displays the value of the `CentralLogFileMode` property. A helper function translates the enumeration value to text.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the log section.  
Set oSection = oWebAdmin.Get("LogSection.Path=" & _  
    "'MACHINE/WEBROOT/APPHOST',Location=''")  
  
' Display the class name of the section.  
WScript.Echo "[ " & oSection.Path_.Class & " ]"  
  
' Display the path and location.  
WScript.Echo "Path: " & oSection.Path  
WScript.Echo "Location: " & oSection.Location  
  
' Display the central log file mode.  
WScript.Echo "CentralLogFileMode: " & _  
                GetModeText(oSection.CentralLogFileMode)  
  
' ==== GetModeText helper function. ====  
Function GetModeText(intMode)  
    Select Case intMode  
        Case 0  
            GetModeText="Site"  
        Case 1  
            GetModeText="CentralBinary"  
        Case 2  
            GetModeText="CentralW3C"  
        Case Else  
            GetModeText="Undefined value"  
    End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `LogSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [CentralBinaryLogFile Class](../../reference/admin/centralbinarylogfile-class1.md)   
 [CentralW3CLogFile Class](../../reference/admin/centralw3clogfile-class1.md)   
 [SiteLogFile Class](../../reference/admin/sitelogfile-class1.md)