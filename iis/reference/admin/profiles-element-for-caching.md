---
title: "profiles Element for caching | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 07877f08-1638-42da-ad63-84dae614cd41
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# profiles Element for caching
> [!NOTE]
>  For more information about the `profiles` element, see the following topic on the Microsoft IIS.net Web site: [Caching Profiles \<profiles>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles).  
  
 Configures the profile to use for output caching.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an output caching profile to the collection of output caching profiles.|  
|`remove`|Optional element.<br /><br /> Removes a reference to an output caching profile from the output caching profile collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to output caching profiles from the output caching profile collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`caching`|Configures output cache settings.|  
  
## Remarks  
 For more information about the `profiles` element, see the following topic on the Microsoft IIS.net Web site: [Caching Profiles \<profiles>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-profiles-for-caching.md)   
 [\<remove>](../../reference/admin/remove-element-for-profiles-for-caching.md)   
 [\<clear>](../../reference/admin/clear-element-for-profiles-for-caching.md)