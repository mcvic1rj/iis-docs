---
title: "ClientTarget Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 987b6112-75ff-8330-f1d0-4314881e0883
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# ClientTarget Class
Represents the mapping of a user agent to an alias.  
  
## Syntax  
  
```vbs  
class ClientTarget : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ClientTarget` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Alias`|A read-only `string` value that contains an alias that is mapped to the user agent specified in the `UserAgent` property. The key property.|  
|`UserAgent`|A read/write `string` value that identifies a specific user agent.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `ClientTarget` property of the [ClientTargetSection](../../reference/admin/clienttargetsection-class.md) class.  
  
 The following `ClientTarget` values are configured in the root Web.config file in the [!INCLUDE[dnprdnlong](../../reference/admin/includes/dnprdnlong-md.md)].  
  
|Alias|User Agent|  
|-----------|----------------|  
|"ie5"|"Mozilla/4.0 (compatible; MSIE 5.5; Windows NT 4.0)"|  
|"ie4"|"Mozilla/4.0 (compatible; MSIE 4.0; Windows NT 4.0)"|  
|"uplevel"|"Mozilla/4.0 (compatible; MSIE 5.5; Windows NT 5.1)"|  
|"downlevel"|"Generic Downlevel"|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ClientTarget`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.ClientTarget?displayProperty=fullName>   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)