---
title: "ProfileSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d8c0627e-0259-7d81-fc26-709f82ef2d18
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# ProfileSettings Class
Configures an event profile that determines how an event is collected by [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and raised to providers.  
  
## Syntax  
  
```vbs  
class ProfileSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ProfileSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Profiles`|An array of [ProfileElement](../../reference/admin/profileelement-class.md) objects that configures event profiles that determine how events are collected by [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and raised to providers.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Profiles` property of the [HealthMonitoringSection](../../reference/admin/healthmonitoringsection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ProfileSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.ProfileSettings>   
 <xref:System.Web.Management.IWebEventCustomEvaluator>   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [HealthMonitoringSection Class](../../reference/admin/healthmonitoringsection-class.md)   
 [ProfileElement Class](../../reference/admin/profileelement-class.md)   
 [System.Int32.MaxValue Field](http://go.microsoft.com/fwlink/?LinkId=69329)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)