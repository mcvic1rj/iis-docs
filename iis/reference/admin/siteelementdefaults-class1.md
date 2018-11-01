---
title: "SiteElementDefaults Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 62e333b7-58e0-15b1-af94-de7f6bb92567
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# SiteElementDefaults Class1
Contains the default values for IIS Web site properties.  
  
## Syntax  
  
```vbs  
class SiteElementDefaults : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SiteElementDefaults` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Limits`|A [SiteLimits](../../reference/admin/sitelimits-class1.md) ojbect that represents the connection-related limits for a site.|  
|`LogFile`|A [SiteLogFile](../../reference/admin/sitelogfile-class1.md) object that contains the log file configuration information for a Web site.|  
|`ServerAutoStart`|A read/write `boolean` value. `true` if the Web site will start when the World Wide Web Publishing Service (WWW Service) starts; otherwise, `false`. The default is `true`.|  
|`TraceFailedRequestsLogging`|A [TraceFailedRequestsLogging](../../reference/admin/tracefailedrequestslogging-class1.md) object that exposes the default read/write logging properties for Web sites.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `SiteDefaults` property of the [Server](../../reference/admin/server-class1.md) class.  
  
## Example  
 The following example sets the maximum number of allowed connections for all Web sites to 100, and then sets the `BytesSent`, `BytesRecv`, and `TimeTaken` flags of the `LogExtFileFlags` attribute to `true`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
Set oSvr = oWebAdmin.Get("Server=@")  
  
' Show the limit to be changed.  
WScript.Echo "Old maxiumum number of connections: " & oSvr.SiteDefaults.Limits.MaxConnections  
  
' Specify the new limit and save the result.  
oSvr.SiteDefaults.Limits.MaxConnections = 1000  
oSvr.Put_  
  
' Show the new limit.  
WScript.Echo "New maxiumum number of connections: " & oSvr.SiteDefaults.Limits.MaxConnections  
  
' Define the flag constants.  
CONST BYTES_SENT = 4096  
CONST BYTES_RECV = 8192  
CONST TIME_TAKEN = 16384  
  
' Configure the flags of the LogExtFileFlags attribute and save the result.  
oSvr.SiteDefaults.LogFile.LogExtFileFlags = oSvr.SiteDefaults.LogFile.LogExtFileFlags Or BYTES_SENT  
oSvr.SiteDefaults.LogFile.LogExtFileFlags = oSvr.SiteDefaults.LogFile.LogExtFileFlags Or BYTES_RECV  
oSvr.SiteDefaults.LogFile.LogExtFileFlags = oSvr.SiteDefaults.LogFile.LogExtFileFlags Or TIME_TAKEN  
oSvr.Put_  
  
```  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `SiteElementDefaults`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [SiteLogFile Class](../../reference/admin/sitelogfile-class1.md)