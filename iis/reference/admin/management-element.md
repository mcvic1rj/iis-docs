---
title: "management Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d0dbdfb9-f5df-429b-baf9-ac00044511e9
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# management Element
> [!NOTE]
>  For more information about the `management` element, see the following topic on the Microsoft IIS.net Web site: [Management \<management>](http://www.iis.net/ConfigReference/system.webServer/management).  
  
 Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`authentication`|Optional element.<br /><br /> Configures authentication settings for remote management of the Web server.|  
|`authorization`|Optional element.<br /><br /> Configures authorization settings for remote management of the Web server.|  
|`trustedProviders`|Optional element.<br /><br /> Configures the providers that are trusted by [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] and the Management Service (WMSVC).|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `management` element, see the following topic on the Microsoft IIS.net Web site: [Management \<management>](http://www.iis.net/ConfigReference/system.webServer/management).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authentication>](../../reference/admin/authentication-element-for-management.md)   
 [\<authorization>](../../reference/admin/authorization-element-for-management.md)   
 [\<trustedProviders>](../../reference/admin/trustedproviders-element-for-management.md)