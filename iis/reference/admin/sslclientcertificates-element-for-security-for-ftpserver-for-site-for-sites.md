---
title: "sslClientCertificates Element for security for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1fbd9b66-6009-4ec1-872b-adc11ee0b2d0
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# sslClientCertificates Element for security for ftpServer for site for sites
> [!NOTE]
>  For more information about the `sslClientCertificates` element, see the following topic on the Microsoft IIS.net Web site: [FTP SSL Client Certificates \<sslClientCertificates>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/sslClientCertificates).  
  
 Specifies the SSL client certificate options for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`clientCertificatePolicy`|Optional `enum` attribute.<br /><br /> Specifies the client certificate policy.<br /><br /> `CertIgnore`<br /><br /> - Specifies that client certificates will not be negotiated for SSL session.<br /><br /> - The numeric value is 0.<br /><br /> `CertAllow`<br /><br /> - Specifies that client certificates will be allowed. If the client chooses to send a certificate, then certificate must be valid and the server must be able to successfully validate it.<br /><br /> - The numeric value is 1.<br /><br /> `CertRequire`<br /><br /> - Specifies that client certificates will be required. FTP clients will not be allowed to connect unless they send a valid client certificate to the server.<br /><br /> - The numeric value is 2.<br /><br /> The default value is `CertIgnore`.|  
|`validationFlags`|Optional `flags` attribute.<br /><br /> Specifies the flags that affect client certificate validation.<br /><br /> `NoRevocationCheck`<br /><br /> - Specifies that certificate revocation checks will be skipped.<br /><br /> Note:<br /><br /> It is not recommended to skip revocation validation.<br /><br /> - The numeric value is 1.<br /><br /> `CertChainRevocationCheckCacheOnly`<br /><br /> - Specifies that revocation checking only accesses cached URLs.<br /><br /> - The numeric value is 2.<br /><br /> `CertChainCacheOnlyUrlRetrieval`<br /><br /> - Specifies only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects.<br /><br /> - The numeric value is 4.<br /><br /> `CertNoUsageCheck`<br /><br /> - Does not check client certificate for usage flags. Usage check is enabled by default and it is meant to assure that only client certificates that allow "Client authentication" are allowed.<br /><br /> - The numeric value is 8.<br /><br /> There is no default value.|  
|`revocationFreshnessTime`|Optional `timeSpan` attribute.<br /><br /> Specifies the amount of time the revocation list is valid.<br /><br /> The default value is 00:00:00.|  
|`revocationUrlRetrievalTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the timeout for retrieving certificate revocation information.<br /><br /> The default value is 00:01:00.|  
|`useActiveDirectoryMapping`|Optional `Boolean` attribute.<br /><br /> tr`u`e if Active Directory mapping should be allowed for client certificates; otherwise, f`a`lse. Active Directory mapping allows domain users to log on by using a client certificate that is configured in Active Directory.<br /><br /> Note:<br /><br /> This feature only allows the SSL layer to attempt to map a client certificate to a user token; the token will not be used automatically. The `clientCertAuthentication` element is used to enable the mapped token for use by FTP instead of credentials specified through "USER" and "PASS" commands.<br /><br /> The default value is `false`.|  
  
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
 For more information about the `sslClientCertificates` element, see the following topic on the Microsoft IIS.net Web site: [FTP SSL Client Certificates \<sslClientCertificates>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/sslClientCertificates).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<security>](../../reference/admin/security-element-for-ftpserver-for-site-for-sites.md)