---
title: "Server Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 52fd13ed-2645-bc13-c04d-a5e82ca50c0f
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# Server Class1
Exposes default configuration settings for applications, application pools, Web sites, and virtual directories on a Web server running IIS.  
  
## Syntax  
  
```vbs  
class Server : Object  
```  
  
## Methods  
 The following table lists the methods exposed by the `Server` class.  
  
|Name|Description|  
|----------|-----------------|  
|[BeginUpdateBatch](../../reference/admin/server-beginupdatebatch-method.md)|Begins a batch of configuration changes for the specified path.|  
|[EndUpdateBatch](../../reference/admin/server-endupdatebatch-method.md)|Ends a batch of configuration changes.|  
  
## Properties  
 The following table lists the properties exposed by the `Server` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ApplicationDefaults`|A read/write [ApplicationElementDefaults](../../reference/admin/applicationelementdefaults-class2.md) value that specifies the default application pool and protocols for new applications.|  
|`ApplicationPoolDefaults`|A read/write [ApplicationPoolElementDefaults](../../reference/admin/applicationpoolelementdefaults-class1.md) value that contains the default properties for the [ApplicationPool](../../reference/admin/applicationpool-class1.md) class.|  
|`SiteDefaults`|A read/write [SiteElementDefaults](../../reference/admin/siteelementdefaults-class1.md) value that contains the default values for an IIS Web site.|  
|`VirtualDirectoryDefaults`|A read/write [VirtualDirectoryElementDefaults](../../reference/admin/virtualdirectoryelementdefaults-class1.md) value that exposes default configuration settings for IIS virtual directories.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The `Server` object is a singleton object (that is, there is only one instance per computer) and, therefore, does not have any key properties.  
  
## Inheritance Hierarchy  
 [Object](../../reference/admin/object-class1.md)  
  
 `Server`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationElementDefaults Class](../../reference/admin/applicationelementdefaults-class2.md)   
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md)   
 [ConfiguredObject Class](../../reference/admin/configuredobject-class1.md)   
 [SiteElementDefaults Class](../../reference/admin/siteelementdefaults-class1.md)   
 [VirtualDirectoryElementDefaults Class](../../reference/admin/virtualdirectoryelementdefaults-class1.md)