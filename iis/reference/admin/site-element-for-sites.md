---
title: "site Element for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e7bab6be-0fc6-42c9-be8a-d98fc5499b01
caps.latest.revision: 34
author: "shirhatti"
manager: "wpickett"
---
# site Element for sites
> [!NOTE]
>  For more information about the `site` element, see the following topic on the Microsoft IIS.net Web site: [Site \<site>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/sslClientCertificates).  
  
 Specifies configuration settings for a site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`id`|Optional `uint` attribute.<br /><br /> Specifies the random numeric identifier that is assigned by IIS when the site is created.<br /><br /> The default Web site is numbered 1. Other Web sites have random numbers composed of multiple digits.|  
|`name`|Optional `string` attribute.<br /><br /> Specifies a friendly name that uniquely identifies a Web site, for example, "Contoso HR Forms".|  
|`serverAutoStart`|Optional `Boolean` attribute.<br /><br /> Specifies whether the site should start automatically when the Management Service is started.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`application`|Optional element.<br /><br /> Specifies configuration settings for an application in the parent site.|  
|`applicationDefaults`|Optional element.<br /><br /> Specifies default settings for all applications in the parent site.|  
|`bindings`|Optional element.<br /><br /> Specifies bindings to access the site.|  
|`ftpServer`|Optional element.<br /><br /> Specifies the site-level settings for FTP features on FTP sites.|  
|`limits`|Optional element.<br /><br /> Configures settings to limit the amount of bandwidth, the number of connections, or the amount of time for connections to a site.|  
|`logFile`|Optional element.<br /><br /> Configures settings for handling and storage of log files for the site.|  
|`traceFailedRequestsLogging`|Optional element.<br /><br /> Specifies settings for logging failed-request traces for the site.|  
|`virtualDirectoryDefaults`|Optional element.<br /><br /> Specifies the default settings for all virtual directories in the parent site.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
  
## Remarks  
 For more information about the `site` element, see the following topic on the Microsoft IIS.net Web site: [Site \<site>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/security/sslClientCertificates).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<application>](../../reference/admin/application-element-for-site-for-sites.md)   
 [\<applicationDefaults>](../../reference/admin/applicationdefaults-element-for-site-for-sites.md)   
 [\<bindings>](../../reference/admin/bindings-element-for-site-for-sites.md)   
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)   
 [\<limits>](../../reference/admin/limits-element-for-site-for-sites.md)   
 [\<logFile>](../../reference/admin/logfile-element-for-site-for-sites.md)   
 [\<traceFailedRequestsLogging>](../../reference/admin/tracefailedrequestslogging-element-for-site-for-sites.md)   
 [\<virtualDirectoryDefaults>](../../reference/admin/virtualdirectorydefaults-element-for-site-for-sites.md)