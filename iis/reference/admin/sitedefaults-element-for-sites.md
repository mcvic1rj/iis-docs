---
title: "siteDefaults Element for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e0117d0b-fb35-41d4-b39d-6608ee5a7494
caps.latest.revision: 28
author: "shirhatti"
manager: "wpickett"
---
# siteDefaults Element for sites
> [!NOTE]
>  For more information about the `siteDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Default Settings for All Sites \<siteDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults).  
  
 Specifies default settings for all sites on the server. If the same attribute or child element is configured in both the siteDefaults section and in the sites section for a specific site, the configuration in the sites section is used for that site.  
  
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
|`bindings`|Optional element.<br /><br /> Specifies the default bindings to access all sites on the server.|  
|`limits`|Optional element.<br /><br /> Configures default settings to limit the amount of bandwidth, the number of connections, or the amount of time for connections to sites on the server.|  
|`logFile`|Optional element.<br /><br /> Configures default settings for handling and storage of log files for all sites.|  
|`traceFailedRequestsLogging`|Optional element.<br /><br /> Specifies default settings for logging failed-request traces for all sites.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
  
## Remarks  
 For more information about the `siteDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Default Settings for All Sites \<siteDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<bindings>](../../reference/admin/bindings-element-for-sitedefaults-for-sites.md)   
 [\<limits>](../../reference/admin/limits-element-for-sitedefaults-for-sites.md)   
 [\<logFile>](../../reference/admin/logfile-element-for-sitedefaults-for-sites.md)   
 [\<traceFailedRequestsLogging>](../../reference/admin/tracefailedrequestslogging-element-for-sitedefaults-for-sites.md)