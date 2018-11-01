---
title: "ProvidersSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b333c163-5099-493a-b4ac-da50c029fd55
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# ProvidersSettings Class
Specifies managed providers that manage membership or roles for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application, or encrypt and decrypt configuration data.  
  
## Syntax  
  
```vbs  
class ProvidersSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ProvidersSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Providers`|An array of [NameTypeElement](../../reference/admin/nametypeelement-class.md) values that specify managed providers.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Providers` array property on the following classes:  
  
-   [ConfigProtectedDataSection](../../reference/admin/configprotecteddatasection-class.md)  
  
-   [MembershipSection](../../reference/admin/membershipsection-class.md)  
  
-   [RoleManagerSection](../../reference/admin/rolemanagersection-class.md)  
  
> [!NOTE]
>  Do not confuse this class with the ASP.NET-related [ProviderSettings](../../reference/admin/providersettings-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ProvidersSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigProtectedDataSection Class](../../reference/admin/configprotecteddatasection-class.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [MembershipSection Class](../../reference/admin/membershipsection-class.md)   
 [NameTypeElement Class](../../reference/admin/nametypeelement-class.md)   
 [RoleManagerSection Class](../../reference/admin/rolemanagersection-class.md)