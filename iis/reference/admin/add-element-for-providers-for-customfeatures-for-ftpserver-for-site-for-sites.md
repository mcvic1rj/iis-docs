---
title: "add Element for providers for customFeatures for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1b4b016f-2bbc-4e5d-89ab-306e92206e05
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# add Element for providers for customFeatures for ftpServer for site for sites
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Custom Features \<add>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures/providers/add).  
  
 Adds a feature provider to the collection of FTP custom providers for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> The name of an FTP provider that is registered in the `providerDefinitions` collection. For information on the `providerDefinitions` element, see [\<providerDefinitiions>](../../reference/admin/providerdefinitions-element-for-system-ftpserver.md).<br /><br /> There is no default value.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> `true` if the provider is enabled; otherwise, `false`.<br /><br /> The default value is `true`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
|`customFeatures`|Specifies the collection of FTP providers that will implement custom functionality for an FTP site.|  
|`providers`|Specifies the collection of custom FTP features.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Custom Features \<add>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures/providers/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<providers>](../../reference/admin/providers-element-for-customfeatures-for-ftpserver-for-site-for-sites.md)