---
title: "add Element for commandFiltering for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f066997d-6cb9-45c1-820e-2b23fda320d0
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# add Element for commandFiltering for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Command Filtering \<add>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/commandFiltering/add).  
  
 Adds a unique entry to the collection of FTP commands that the FTP service will allow or deny.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Element|Description|  
|-------------|-----------------|  
|`command`|Required unique `string` attribute.<br /><br /> Specifies the FTP command for the rule.<br /><br /> There is no default value.|  
|`allowed`|Required `Boolean` attribute.<br /><br /> `true` if the command is allowed; otherwise, `false`.<br /><br /> There is no default value.|  
  
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
|`security`|Specifies the site-level security options for an FTP site.|  
|`commandFiltering`|Specifies a collection of FTP commands that the FTP service will allow or deny.|  
  
## Remarks  
 For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Command Filtering \<add>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/commandFiltering/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<commandFiltering>](../../reference/admin/commandfiltering-element-for-security-for-ftpserver-for-site-for-sites.md)