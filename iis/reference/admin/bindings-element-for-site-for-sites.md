---
title: "bindings Element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e3dcdfda-fa0a-4a7e-bfd5-3fb2fe2f8167
caps.latest.revision: 30
author: "shirhatti"
manager: "wpickett"
---
# bindings Element for site for sites
> [!NOTE]
>  For more information about the `bindings` element, see the following topic on the Microsoft IIS.net Web site: [Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings).  
  
 Specifies bindings to access the site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`binding`|Optional element.<br /><br /> Configures a binding in the parent site.|  
|`clear`|Optional element.<br /><br /> Clears references to default settings that are inherited from the parent level of the configuration.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `bindings` element, see the following topic on the Microsoft IIS.net Web site: [Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<binding>](../../reference/admin/binding-element-for-bindings-for-site-for-sites.md)   
 [\<clear>](../../reference/admin/clear-element-for-bindings-for-site-for-sites.md)