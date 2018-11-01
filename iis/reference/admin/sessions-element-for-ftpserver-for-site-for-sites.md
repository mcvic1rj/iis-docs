---
title: "sessions Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1f8e9e42-88b9-4412-86c2-e5e97f0b554b
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# sessions Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `sessions` element, see the following topic on the Microsoft IIS.net Web site: [FTP Sessions \<sessions>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/sessions).  
  
 A collection of elements which are dynamically created by the FTP service as clients connect to your FTP server. The data within these elements can be queried but not modified.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`session`|Dynamically created element.<br /><br /> Specifies information about an FTP session.|  
  
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
  
## Remarks  
 For more information about the `sessions` element, see the following topic on the Microsoft IIS.net Web site: [FTP Sessions \<sessions>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/sessions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<session>](../../reference/admin/session-element-for-sessions-for-ftpserver-for-site-for-sites.md)