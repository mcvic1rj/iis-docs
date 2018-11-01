---
title: "SqlCacheDependencyDatabase Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 51602b5f-115f-373d-a75a-339b91c9ff94
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# SqlCacheDependencyDatabase Class
Exposes configuration settings for SQL data in an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] cache.  
  
## Syntax  
  
```vbs  
class SqlCacheDependencyDatabase : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SqlCacheDependencyDatabase` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ConnectionStringName`|A read/write `string` value that specifies the name of the connection string to the SQL data source.|  
|`Name`|A read-only `string` value that contains the name of the SQL database whose data is cached by [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)].|  
|`PollTime`|A read/write `sint32` value, in milliseconds, that specifies how often the SQL data source is queried for changes. The default is 60000. This property cannot be set to less than 500.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Databases` array property of the [SqlCacheDependencyDatabaseSettings](../../reference/admin/sqlcachedependencydatabasesettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `SqlCacheDependencyDatabase`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Caching.SqlCacheDependency?displayProperty=fullName>   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [SqlCacheDependencySection Class](../../reference/admin/sqlcachedependencysection-class.md)   
 [SqlCacheDependencyDatabaseSettings Class](../../reference/admin/sqlcachedependencydatabasesettings-class.md)