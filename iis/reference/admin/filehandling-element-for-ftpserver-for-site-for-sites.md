---
title: "fileHandling Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0bc37e62-8107-452a-992a-21aebadb9fd8
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# fileHandling Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `fileHandling` element, see the following topic on the Microsoft IIS.net Web site: [FTP File Handling \<fileHandling>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/fileHandling).  
  
 Specifies the way that the FTP service handles file operations.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowReadUploadsInProgress`|Optional `Boolean` attribute.<br /><br /> `true` if the FTP service should allow read access to files that are currently being uploaded; otherwise, `false`.<br /><br /> The default value is `false`.|  
|`allowReplaceOnRename`|Optional `Boolean` attribute.<br /><br /> `true` if the FTP service should allow files that are being renamed to overwrite existing files; otherwise, `false`.<br /><br /> The default value is `false`.|  
|`keepPartialUploads`|Optional `Boolean` attribute.<br /><br /> `true` if the FTP service should keep files that have been partially uploaded; otherwise, `false`.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features on FTP sites.|  
  
## Remarks  
 For more information about the `fileHandling` element, see the following topic on the Microsoft IIS.net Web site: [FTP File Handling \<fileHandling>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/fileHandling).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)