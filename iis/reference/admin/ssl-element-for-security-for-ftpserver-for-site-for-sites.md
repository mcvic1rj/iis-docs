---
title: "ssl Element for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fb0a0ffa-1a45-4e00-b08e-446cd8b59c7b
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# ssl Element for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the ssl element, see the following topic on the Microsoft IIS.net Web site: [FTP Over SSL \<ssl>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/ssl).  
  
 Specifies the FTP over Secure Sockets Layer (SSL) settings for the FTP service.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`controlChannelPolicy`|Optional `enum` attribute.<br /><br /> Specifies the SSL policy for the FTP control channel.<br /><br /> There is no `enum` value that denies SSL for the command channel; to deny SSL, do not bind an SSL certificate to the FTP site by specifying a certificate hash in the `serverCertHash` attribute.<br /><br /> -   `SslAllow:`<br />     - Specifies that SSL is allowed for the control channel.<br />     - The numeric value is 0.<br /><br /> -   `SslRequire:`<br />     - Specifies that SSL is required for the control channel.<br />     - The numeric value is 1.<br /><br /> -   `SslRequireCredentialsOnly:`<br />     - Specifies that only the "USER" and "PASS" commands have to be sent over SSL session. After an FTP client has logged in, the client can switch to a non-secure mode.<br />     - The numeric value is 2.<br /><br /> The default value is `SslRequire`.|  
|`dataChannelPolicy`|Optional `enum` attribute.<br /><br /> Specifies the SSL policy for the FTP data channel.<br /><br /> -   `SslAllow:`<br />     - Specifies that SSL is allowed for the data channel.<br />     - The numeric value is 0.<br /><br /> -   `SslRequire:`<br />     - Specifies that SSL is required for the data channel.<br />     - The numeric value is 1.<br /><br /> -   `SslDeny:`<br />     - Specifies that SSL is denied for the data channel.<br />     - The numeric value is 2.<br /><br /> The default value is `SslRequire`.|  
|`serverCertHash`|Optional `string` attribute.<br /><br /> Specifies the thumbprint hash for the server side certificate to use for SSL connections.<br /><br /> There is no default value.|  
|`serverCertStoreName`|Optional `string` attribute.<br /><br /> Specifies the certificate store for server SSL certificates.<br /><br /> The default value is `MY`.|  
|`ssl128`|Optional `Boolean` attribute.<br /><br /> Specifies whether 128-bit SSL is required.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level security options for an FTP site.|  
|`security`|Specifies the site-level authentication settings for an FTP site.|  
  
## Remarks  
 For more information about the ssl element, see the following topic on the Microsoft IIS.net Web site: [FTP Over SSL \<ssl>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/ssl).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<security>](../../reference/admin/security-element-for-ftpserver-for-site-for-sites.md)