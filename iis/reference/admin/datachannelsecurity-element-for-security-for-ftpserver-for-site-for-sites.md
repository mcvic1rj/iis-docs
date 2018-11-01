---
title: "dataChannelSecurity Element for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5693ab00-bd89-48e2-b721-b51605f6183a
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# dataChannelSecurity Element for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the dataChannelSecurity element, see the following topic on the Microsoft IIS.net Web site: [FTP Data Channel Security \<dataChannelSecurity>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/dataChannelSecurity).  
  
 Specifies FTP data channel security settings for server-to-server and third party transfers. These settings allow administrators to disable enforcement of matching client IP addresses for the control and data channel.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`matchClientAddressForPort`|Optional `Boolean` attribute.<br /><br /> Specifies whether to match the client’s IP address on PORT/EPRT commands.<br /><br /> The default value is `true`.|  
|`matchClientAddressForPasv`|Optional `Boolean` attribute.<br /><br /> Specifies whether to match the client’s IP address on PASV/EPSV commands.<br /><br /> The default value is `true`.|  
  
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
  
## Remarks  
 For more information about the dataChannelSecurity element, see the following topic on the Microsoft IIS.net Web site: [FTP Data Channel Security \<dataChannelSecurity>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/dataChannelSecurity).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<security>](../../reference/admin/security-element-for-ftpserver-for-site-for-sites.md)