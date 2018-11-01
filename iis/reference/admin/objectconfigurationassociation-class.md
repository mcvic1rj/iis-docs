---
title: "ObjectConfigurationAssociation Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c67f2a8d-efac-9e05-784d-82333e1017d5
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# ObjectConfigurationAssociation Class
Associates a configured object with its configuration section.  
  
## Syntax  
  
```vbs  
class ObjectConfigurationAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ObjectConfigurationAssociation` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ConfigurationSection`|An `object ref` value that represents the configuration section for an object.|  
|`ConfiguredObject`|An `object ref` value that represents an object that is configured.|  
  
## Subclasses  
 The following table lists the subclasses exposed by the `ObjectConfigurationAssociation` class.  
  
|Name|Description|  
|----------|-----------------|  
|[ApplicationContainsConfigurationSection](../../reference/admin/applicationcontainsconfigurationsection-class1.md)|Provides a relationship between an IIS Web application and a configuration section.|  
|[SiteContainsConfigurationSection](../../reference/admin/sitecontainsconfigurationsection-class1.md)|Provides a relationship between a Web site and its configuration sections.|  
|[VirtualDirectoryContainsConfigurationSection](../../reference/admin/virtualdirectorycontainsconfigurationsection-class2.md)|Provides a relationship between a virtual directory and a configuration section.|  
  
## Remarks  
 This abstract class describes a strict containment association between two different namespace objects. It is the base type from which all object–configuration section associations derive.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [WMI Provider](../../reference/admin/wmi-provider.md)   
 [ApplicationContainsConfigurationSection Class](../../reference/admin/applicationcontainsconfigurationsection-class1.md)   
 [SiteContainsConfigurationSection Class](../../reference/admin/sitecontainsconfigurationsection-class1.md)   
 [VirtualDirectoryContainsConfigurationSection Class](../../reference/admin/virtualdirectorycontainsconfigurationsection-class2.md)