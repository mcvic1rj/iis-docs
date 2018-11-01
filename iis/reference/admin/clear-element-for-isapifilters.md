---
title: "clear Element for isapiFilters | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 716bd0b9-77fb-4e71-b747-aa1d8478ecb3
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# clear Element for isapiFilters
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
 Removes all references to inherited ISAPI `filter` settings and allows only those added at the current configuration level.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`isapiFilters`|Specifies configuration settings for ISAPI filters on a Web server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<isapiFilters>](../../reference/admin/isapifilters-element.md)