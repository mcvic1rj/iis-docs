---
title: "ModuleSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 760f4adf-3e89-4a5d-9648-ca4753f5eb65
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# ModuleSettings Class
Represents the type information for a custom [System.Net.IWebProxy](http://go.microsoft.com/fwlink/?LinkId=70961) module.  
  
## Syntax  
  
```vbs  
class ModuleSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ModuleSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Type`|A read/write `string` value that specifies the type and assembly information for the current instance.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Module` property of the [DefaultProxySection](../../reference/admin/defaultproxysection-class.md) class.  
  
 This class specifies a Web proxy that handles requests made with the [System.Net.WebRequest](http://go.microsoft.com/fwlink/?LinkId=70962) and [System.Net.WebClient](http://go.microsoft.com/fwlink/?LinkId=70963) classes.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ModuleSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [DefaultProxySection Class](../../reference/admin/defaultproxysection-class.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [System.Net.IWebProxy Interface](http://go.microsoft.com/fwlink/?LinkId=70961)   
 [System.Net.WebRequest Class](http://go.microsoft.com/fwlink/?LinkId=70962)   
 [System.Net.WebClient Class](http://go.microsoft.com/fwlink/?LinkId=70963)