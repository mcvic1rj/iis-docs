---
title: "security Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5e9edcd6-839a-442c-8d5f-1babcccbc979
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# security Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the security element, see the following topic on the Microsoft IIS.net Web site: [FTP Security \<security>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security).  
  
 Defines the parent element for the site-level security options of an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|authentication|Optional element.<br /><br /> Specifies the authentication settings for an FTP site.|  
|commandFiltering|Optional element.<br /><br /> Specifies the settings for FTP command filtering.|  
|dataChannelSecurity|Optional element.<br /><br /> Specifies the settings for FTP data channel security.|  
|ssl|Optional element.<br /><br /> Specifies the SSL settings for an FTP site.|  
|sslClientCertificates|Optional element.<br /><br /> Specifies the SSL client certificate options for an FTP site.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
  
## Remarks  
 For more information about the security element, see the following topic on the Microsoft IIS.net Web site: [FTP Security \<security>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authentication>](../../reference/admin/authentication-element-for-security-for-ftpserver-for-site-for-sites.md)   
 [\<commandFiltering>](../../reference/admin/commandfiltering-element-for-security-for-ftpserver-for-site-for-sites.md)   
 [\<dataChannelSecurity>](../../reference/admin/datachannelsecurity-element-for-security-for-ftpserver-for-site-for-sites.md)   
 [\<ssl>](../../reference/admin/ssl-element-for-security-for-ftpserver-for-site-for-sites.md)   
 [\<sslClientCertificates>](../../reference/admin/sslclientcertificates-element-for-security-for-ftpserver-for-site-for-sites.md)