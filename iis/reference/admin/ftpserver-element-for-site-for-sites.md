---
title: "ftpServer Element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a0e548ab-9c95-4da1-8c55-5379442d7036
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# ftpServer Element for site for sites
> [!NOTE]
>  For more information about the `ftpServer` element, see the following topic on the Microsoft IIS.net Web site: [FTP Site Level-Settings \<ftpServer>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer).  
  
 Specifies the site-level settings for FTP features on FTP sites.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUTF8`|Optional `Boolean` attribute.<br /><br /> Specifies whether UTF8 activity should be allowed (includes UTF8 filenames).<br /><br /> The default value is `true`.|  
|`serverAutoStart`|Optional `Boolean` attribute.<br /><br /> Specifies whether the FTP site should start automatically.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`connections`|Optional element.<br /><br /> Specifies the idle timeout (in seconds) between when a new connection is made and authentication is attempted.|  
|`customFeatures`|Optional element.<br /><br /> Specifies providers for custom home directory lookup, custom command handling and logging|  
|`directoryBrowse`|Optional element.<br /><br /> Specifies FTP settings for browsing site directories.|  
|`fileHandling`|Optional element.<br /><br /> Specifies settings that control how content is uploaded to the Web server.|  
|`firewallSupport`|Optional element.<br /><br /> Specifies the external address of the firewall that is sent to clients when passive connections using PASV command are negotiated. PASV command responses contain the IP address and Port of the Web server. By default, the local IP address is returned.|  
|`logFile`|Optional element.<br /><br /> Specifies settings for FTP site logging.|  
|`messages`|Optional element.<br /><br /> Specifies FTP-specific messages.|  
|`security`|Optional element.<br /><br /> Specifies security settings for FTP sites.|  
|`userIsolation`|Optional element.<br /><br /> Specifies FTP directory access settings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `ftpServer` element, see the following topic on the Microsoft IIS.net Web site: [FTP Site Level-Settings \<ftpServer>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<connections>](../../reference/admin/connections-element-for-ftpserver-for-site-for-sites.md)   
 [\<customFeatures>](../../reference/admin/customfeatures-element-for-ftpserver-for-site-for-sites.md)   
 [\<directoryBrowse>](../../reference/admin/directorybrowse-element-for-ftpserver-for-site-for-sites.md)   
 [\<fileHandling>](../../reference/admin/filehandling-element-for-ftpserver-for-site-for-sites.md)   
 [\<firewallSupport>](../../reference/admin/firewallsupport-element-for-ftpserver-for-site-for-sites.md)   
 [\<logFile>](../../reference/admin/logfile-element-for-ftpserver-for-site-for-sites.md)   
 [\<messages>](../../reference/admin/messages-element-for-ftpserver-for-site-for-sites.md)   
 [\<security>](../../reference/admin/security-element-for-ftpserver-for-site-for-sites.md)   
 [\<sessions>](../../reference/admin/sessions-element-for-ftpserver-for-site-for-sites.md)   
 [\<userIsolation>](../../reference/admin/userisolation-element-for-ftpserver-for-site-for-sites.md)