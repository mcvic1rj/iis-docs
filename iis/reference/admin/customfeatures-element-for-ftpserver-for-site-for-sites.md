---
title: "customFeatures Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 115da274-65b5-4cc7-ab11-bc31a69ee6ec
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# customFeatures Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `customFeatures` element, see the following topic on the Microsoft IIS.net Web site: [FTP Custom Features \<customFeatures>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures).  
  
 Specifies the collection of FTP providers that will implement custom functionality for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`providers`|Optional element.<br /><br /> Specifies the collection of custom FTP features.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
  
## Remarks  
 For more information about the `customFeatures` element, see the following topic on the Microsoft IIS.net Web site: [FTP Custom Features \<customFeatures>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/customFeatures).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<providers>](../../reference/admin/providers-element-for-customfeatures-for-ftpserver-for-site-for-sites.md)