---
title: "authentication Element for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 38c6ee3d-294f-45db-8da8-4d0d7a4e37ee
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# authentication Element for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the authentication element, see the following topic on the Microsoft IIS.net Web site: [FTP Authentication \<authentication>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/authentication).  
  
 Specifies the site-level authentication settings for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|anonymousAuthentication|Optional element.<br /><br /> Specifies the Anonymous authentication settings for an FTP site.|  
|basicAuthentication|Optional element.<br /><br /> Specifies the Basic authentication settings for an FTP site.|  
|clientCertAuthentication|Optional element.<br /><br /> Specifies the Client Certificate authentication settings for an FTP site.|  
|customAuthentication|Optional element.<br /><br /> Specifies the Custom authentication settings for an FTP site. **Note:**  Custom authentication is implemented through custom authentication providers.|  
  
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
 For more information about the authentication element, see the following topic on the Microsoft IIS.net Web site: [FTP Authentication \<authentication>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/authentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<anonymousAuthentication>](../../reference/admin/e3fbafc0-0f25-4546-bf47-f419b893eacc.md)   
 [\<basicAuthentication>](../../reference/admin/f413c235-54a3-4ae7-9ecb-758c9a816b61.md)   
 [\<clientCertAuthentication>](../../reference/admin/fc62dacd-0a60-4c9e-9a2e-b85b974d2ef7.md)   
 [\<customAuthentication>](../../reference/admin/686ab803-25a1-47c4-bd16-4815a232d3ae.md)