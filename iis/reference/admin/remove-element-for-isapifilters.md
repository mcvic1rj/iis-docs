---
title: "remove Element for isapiFilters | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c520847b-6a57-457f-aca3-c3e73abe0e22
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# remove Element for isapiFilters
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
 Removes an ISAPI filter from the ISAPI filters collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of the ISAPI filter.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`isapiFilters`|Specifies configuration settings for ISAPI filters on a Web server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI Filters \<isapiFilters>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<isapiFilters>](../../reference/admin/isapifilters-element.md)