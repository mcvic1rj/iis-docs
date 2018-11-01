---
title: "AuthorizationRule Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f334ec89-73af-4b83-5c45-0fc379b053fe
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# AuthorizationRule Class
Represents a rule in the authorization section of a configuration file.  
  
## Syntax  
  
```vbs  
class AuthorizationRule : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `AuthorizationRule` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AccessType`|A read/write `sint32` enumeration that specifies whether access to a URL resource is granted based on the combination of values specified by the `Roles`, `Users`, and `Verbs` properties. The possible values are listed later in the Remarks section. **Note:**  At run time, the authorization module iterates through `AuthorizationRule` elements until it finds the first rule that fits a particular user. It then grants or denies access to a URL resource depending on the value of the `AccessType` property.|  
|`Roles`|A required unique read/write `string` value that contains a comma-delimited list of roles for which access to a URL resource is granted or denied. A key property. **Note:**  There must be at least one value in either the `Users` property or the `Roles` property, or both.|  
|`Users`|A required unique read/write `string` value that contains a comma-delimited list of users for whom access to a URL resource is granted or denied. The default is "\*". A key property. **Note:**  There must be at least one value in either the `Users` property or the `Roles` property, or both.|  
|`Verbs`|A required unique read/write `string` value that contains a comma-delimited list of HTTP transmission methods for which access to a URL resource is granted or denied. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Authorization` property of the [AuthorizationSection](../../reference/admin/authorizationsection-class1.md) class.  
  
 The following table lists the possible values for the `AccessType` property.  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Allow`|Grants access to a URL resource for the combination of values you specify in the `Roles`, `Users`, and `Verbs` properties.|  
|1|`Deny`|Denies access to a URL resource for the combination of values you specify in the `Roles`, `Users`, and `Verbs` properties.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `AuthorizationRule`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.AuthorizationRule?displayProperty=fullName>   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)