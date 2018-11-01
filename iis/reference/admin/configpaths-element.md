---
title: "configPaths Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8d30269d-4084-41a6-b11d-d3af962cc07c
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# configPaths Element
Lists the locations where a configuration setting is set across the distributed configuration file system.  
  
> [!NOTE]
>  These settings are read-only and are not configurable by the end user.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`searchResult`|Contains a collection of configuration search results.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `configPaths` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Paths \<configPaths>](http://www.iis.net/ConfigReference/configPaths).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|None.|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<searchResult>](../../reference/admin/searchresult-element-for-configpaths.md)