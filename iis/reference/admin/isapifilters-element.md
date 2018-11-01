---
title: "isapiFilters Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7c3a8edc-968a-4bc4-8815-85eddb51ac2b
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# isapiFilters Element
> [!NOTE]
>  For more information about the `isapiFilters` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
 Specifies configuration settings for ISAPI filters on a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`clear`|Optional element.<br /><br /> Removes all references to ISAPI filters from the ISAPI filters collection.|  
|`filter`|Optional element.<br /><br /> Adds an ISAPI filter to the ISAPI filters collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to an ISAPI filter from the ISAPI filters collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `isapiFilters` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
> [!IMPORTANT]
>  The [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] implementation interacts with ISAPI filters created for IIS 6.0 running in worker process isolation mode. However, [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] does not support ISAPI filters that run in IIS 5.0 isolation mode on IIS 6.0.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<filter>](../../reference/admin/filter-element-for-isapifilters.md)   
 [\<remove>](../../reference/admin/remove-element-for-isapifilters.md)   
 [\<clear>](../../reference/admin/clear-element-for-isapifilters.md)