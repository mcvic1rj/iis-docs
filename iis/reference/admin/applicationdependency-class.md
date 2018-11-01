---
title: "ApplicationDependency Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a2b235cd-4d10-8d8a-648c-311f6c9465d4
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# ApplicationDependency Class
Represents a dependency between a Web application and one or more Web service extensions.  
  
## Syntax  
  
```vbs  
class ApplicationDependency : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationDependency` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Application`|An array of [GroupDependency](../../reference/admin/groupdependency-class.md) values that contains the group IDs of Web service extensions on which the application specified in the `Name` property depends.|  
|`GroupId`|A read/write `string` value that contains the primary group ID of the application specified in the `Name` property. This property is used to link a dependency with an entry in the `<isapiCgiRestriction>` configuration section. **Note:**  By default, [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] supports the group IDs "ASP" and "ASP.NET".|  
|`Name`|A read-only `string` value that specifies the friendly name of an application that depends on the Web service extensions specified in the `GroupDependency` property. The key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are exposed as members of the `ApplicationDependencies` property on the [ApplicationDependenciesSection](../../reference/admin/applicationdependenciessection-class1.md) class.  
  
> [!NOTE]
>  In IIS 6.0, Web service extension settings were serverwide. In [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)], you can configure these settings at a global or application pool level.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ApplicationDependency`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationDependenciesSection Class](../../reference/admin/applicationdependenciessection-class1.md)   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [GroupDependency Class](../../reference/admin/groupdependency-class.md)   
 [IsapiCgiRestrictionElement Class](../../reference/admin/isapicgirestrictionelement-class.md)   
 [IsapiCgiRestrictionSection Class](../../reference/admin/isapicgirestrictionsection-class.md)