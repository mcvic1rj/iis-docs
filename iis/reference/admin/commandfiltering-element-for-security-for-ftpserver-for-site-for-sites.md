---
title: "commandFiltering Element for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 66e272d5-cf6c-4d94-af69-9d12f95cf97c
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# commandFiltering Element for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the commandFiltering element, see the following topic on the Microsoft IIS.net Web site: [FTP Command Filtering \<commandFiltering>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/commandFiltering).  
  
 Specifies a collection of FTP commands that the FTP service will allow or deny.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`maxCommandLine`|Optional `uint` attribute.<br /><br /> Specifies the maximum command line length. It includes the command and parameters. Lines longer than the configured limit will not be processed.<br /><br /> The default value is 4096.|  
|`allowUnlisted`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow unlisted commands.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an entry to the collection of FTP commands.|  
|`remove`|Optional element.<br /><br /> Removes an entry from the collection of FTP commands.|  
|`clear`|Optional element.<br /><br /> Clears the collection of FTP commands.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
|`security`|Specifies the site-level security options for an FTP site.|  
  
## Remarks  
 For more information about the commandFiltering element, see the following topic on the Microsoft IIS.net Web site: [FTP Command Filtering \<commandFiltering>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/commandFiltering).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-commandfiltering-for-security-for-ftpserver-for-site-for-sites.md)