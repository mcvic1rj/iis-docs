---
title: "firewallSupport Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 80324dc2-fc56-41e2-8091-c57e2263b344
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# firewallSupport Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `firewallSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Firewall Support \<firewallSupoort>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/firewallSupport).  
  
 Configures the way that the FTP service works with firewalls.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`externalIp4Address`|Optional `string` attribute.<br /><br /> Specifies the external IPv4 address for your firewall.<br /><br /> There is no default value.|  
  
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
 For more information about the `firewallSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Firewall Support \<firewallSupoort>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/firewallSupport).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)