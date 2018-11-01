---
title: "CacheSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 399f2fd6-95c6-908a-a7ea-312cca9b1107
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# CacheSection Class
Defines cache settings for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] Web application.  
  
## Syntax  
  
```vbs  
class CacheSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `CacheSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `CacheSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DisableExpiration`|An optional read/write `boolean` value. `true` if cache expiration is disabled; otherwise, `false`. The default is `false`.<br /><br /> When disabled, cached items do not expire and background cleanup of expired cache items does not occur.|  
|`DisableMemoryCollection`|An optional read/write `boolean` value. `true` if the cache memory collection that occurs when the computer is under memory pressure is disabled; otherwise, `false`. The default is `false`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`PercentagePhysicalMemoryUsedLimit`|An optional read/write `sint32` value that specifies the maximum percentage of a computer's physical memory that can be consumed by an application before the cache starts to flush expired items and attempts to reclaim memory. The default is 89.<br /><br /> The specified percentage includes both memory used by the cache as well as the normal memory used by the running application. A setting of 0 indicates that [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] will use its own heuristics for determining when to start reclaiming memory.|  
|`PrivateBytesLimit`|An optional read/write `string` value that specifies the maximum size, in bytes, of an application's private memory cache before the cache starts to flush expired items and attempts to reclaim memory. The default is 0.<br /><br /> The specified limit includes both memory used by the cache as well as normal memory used by the running application. A setting of 0 indicates that [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] will use its own heuristics for determining when to start reclaiming memory.|  
|`PrivateBytesPollTime`|An optional read/write `datetime` value that specifies the time interval between successive pollings for an application's private memory usage. The default is 2 minutes.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `CacheSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CachingProfileElement Class](../../reference/admin/cachingprofileelement-class.md)   
 [CachingSection Class](../../reference/admin/cachingsection-class.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [OutputCacheSection Class](../../reference/admin/outputcachesection-class.md)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)