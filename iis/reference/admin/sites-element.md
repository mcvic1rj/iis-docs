---
title: "sites Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: cc4c6d88-bf65-478e-b824-e2ff4d46d664
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# sites Element
> [!NOTE]
>  For more information about the `sites` element, see the following topic on the Microsoft IIS.net Web site: [Sites \<sites>](http://www.iis.net/ConfigReference/system.applicationHost/sites).  
  
 Defines all sites on the server, and all applications and virtual directories in those sites.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`applicationDefaults`|Optional element.<br /><br /> Specifies default settings for all applications on the server.|  
|`site`|Optional element.<br /><br /> Specifies configuration settings for a site.|  
|`siteDefaults`|Optional element.<br /><br /> Specifies default settings for all sites on the server.|  
|`virtualDirectoryDefaults`|Optional element.<br /><br /> Specifies default settings for all virtual directories on the server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `sites` element, see the following topic on the Microsoft IIS.net Web site: [Sites \<sites>](http://www.iis.net/ConfigReference/system.applicationHost/sites).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<applicationDefaults>](../../reference/admin/applicationdefaults-element-for-sites-element.md)   
 [\<site>](../../reference/admin/site-element-for-sites.md)   
 [\<siteDefaults>](../../reference/admin/sitedefaults-element-for-sites.md)   
 [\<virtualDirectoryDefaults>](../../reference/admin/virtualdirectorydefaults-element-for-sites-iis-settings-schema.md)