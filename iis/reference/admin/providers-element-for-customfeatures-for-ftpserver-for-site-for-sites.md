---
title: "providers Element for customFeatures for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a17f4bcd-360d-42e9-866f-b0951b13211d
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# providers Element for customFeatures for ftpServer for site for sites
> [!NOTE]
>  For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [FTP Custom Feature Providers \<providers>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures/providers).  
  
 Specifies a collection of FTP custom feature providers for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a feature provider to the collection of FTP custom providers for an FTP site.|  
|`remove`|Optional element.<br /><br /> Removes a feature provider from the collection of FTP custom providers for an FTP site.|  
|`clear`|Optional element.<br /><br /> Clears the collection of FTP custom providers for an FTP site.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
|`customFeatures`|Specifies the collection of FTP providers that will implement custom functionality for an FTP site.|  
  
## Remarks  
 For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [FTP Custom Feature Providers \<providers>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures/providers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-providers-for-customfeatures-for-ftpserver-for-site-for-sites.md)