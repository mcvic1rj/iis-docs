---
title: "ProviderSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a55acfd1-a520-a50d-c75e-488c090f1c6c
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# ProviderSettings Class
Specifies the name and type of [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)]-related providers.  
  
## Syntax  
  
```vbs  
class ProviderSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ProviderSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Providers`|An array of [ProviderElement](../../reference/admin/providerelement-class.md) values that specify [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)]-related providers.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Providers` property of the [HealthMonitoringSection](../../reference/admin/healthmonitoringsection-class.md), [SessionStateSection](../../reference/admin/sessionstatesection-class.md), and [SiteMapSection](../../reference/admin/sitemapsection-class.md) classes.  
  
> [!NOTE]
>  Do not confuse this class with the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)]–related [ProvidersSettings](../../reference/admin/providerssettings-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ProviderSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [HealthMonitoringSection Class](../../reference/admin/healthmonitoringsection-class.md)   
 [ProviderElement Class](../../reference/admin/providerelement-class.md)   
 [ProvidersSettings Class](../../reference/admin/providerssettings-class.md)   
 [SessionStateSection Class](../../reference/admin/sessionstatesection-class.md)   
 [SiteMapSection Class](../../reference/admin/sitemapsection-class.md)