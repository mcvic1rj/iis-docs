---
title: "ConfiguredObject Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fbc82145-2355-3b59-ad74-3eb7b5f3f5ec
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# ConfiguredObject Class1
Acts as a base type for namespace objects whose configuration can be specified in configuration sections.  
  
## Syntax  
  
```vbs  
class ConfiguredObject : Object  
```  
  
## Methods  
 The following table lists the methods exposed by the `ConfiguredObject` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllSections](../../reference/admin/configuredobject-getallsections-method1.md)|Retrieves all configuration sections under a configured object.|  
|[GetSection](../../reference/admin/configuredobject-getsection-method.md)|Retrieves the contents of a configuration section for a configured object.|  
  
## Properties  
 This class contains no properties.  
  
## Subclasses  
 The following table lists the subclasses exposed by the `ConfiguredObject` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Application](../../reference/admin/application-class1.md)|Represents an IIS Web application.|  
|[Site](../../reference/admin/site-class1.md)|Represents an IIS Web site.|  
|[VirtualDirectory](../../reference/admin/virtualdirectory-class2.md)|Represents an IIS virtual directory.|  
  
## Inheritance Hierarchy  
 [Object](../../reference/admin/object-class1.md)  
  
 `ConfiguredObject`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [Object Class](../../reference/admin/object-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)