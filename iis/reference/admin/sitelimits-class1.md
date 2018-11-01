---
title: "SiteLimits Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3116f8b2-608a-930d-92d0-35a952e1f4aa
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# SiteLimits Class1
Exposes connection-related limits for a site.  
  
## Syntax  
  
```vbs  
class SiteLimits : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SiteLimits` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ConnectionTimeout`|A read/write `datetime` value that specifies the time that IIS waits before it considers a connection inactive and terminates it. The default is 2 minutes.|  
|`MaxBandwidth`|A read/write `uint32` value that specifies the maximum network bandwidth, in bytes per second, used for IIS. You can use `MaxBandwidth` help prevent excessive IIS network traffic. **Note:**  Although the IIS_Schema.xml file specifies 4294967295 (unlimited) as the default for this property, the default returned by the WMI provider is -1.|  
|`MaxConnections`|A read/write `uint32` value that specifies the maximum number of simultaneous connections to a server. **Note:**  Although the IIS_Schema.xml file specifies 4294967295 (unlimited) as the default for this property, the default returned by the WMI provider is -1.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Limits` property of the [Site](../../reference/admin/site-class1.md) class and the [SiteElementDefaults](../../reference/admin/siteelementdefaults-class1.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `SiteLimits`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [SiteElementDefaults Class](../../reference/admin/siteelementdefaults-class1.md)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)