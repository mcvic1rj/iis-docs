---
title: "ApplicationElementDefaults Class2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a07c6d97-5338-8e18-a96e-ece01b6b7738
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# ApplicationElementDefaults Class2
Specifies the default application pool and enabled protocols for new applications.  
  
## Syntax  
  
```vbs  
class ApplicationElementDefaults : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationElementDefaults` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ApplicationPool`|A read/write `string` value that specifies the default application pool for new applications. The default is "DefaultAppPool".|  
|`EnabledProtocols`|A read/write array of `string` values that contains the protocols that are enabled by default for new applications.|  
|`Path`|A read-only `string` value that specifies the default virtual path of the application after the host header. For example, if you have an application at http://www.alpineskihouse.com/Skis/Downhill, the value of the `Path` property is "/Skis/Downhill". A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class is exposed as the `ApplicationDefaults` property on the [Server](../../reference/admin/server-class1.md) class and on the [Site](../../reference/admin/site-class1.md) class, and corresponds to the `<applicationDefaults>` element in the ApplicationHost.config file.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ApplicationElementDefaults`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)