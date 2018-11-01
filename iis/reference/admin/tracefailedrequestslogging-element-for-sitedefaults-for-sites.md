---
title: "traceFailedRequestsLogging Element for siteDefaults for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 26283186-e923-4b27-b511-43fd3a393a54
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# traceFailedRequestsLogging Element for siteDefaults for sites
> [!NOTE]
>  For more information about the `traceFailedRequestsLogging` element, see the following topic on the Microsoft IIS.net Web site: [Default Trace Failed Requests Logging for a Site \<traceFailedRequestsLogging>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/traceFailedRequestsLogging).  
  
 Specifies default settings for logging failed-request traces for all sites.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the failed request trace logging directory for a site.<br /><br /> The default value is %systemdrive%\inetpub\logs\FailedReqLogFiles.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether failed request trace logging is enabled for a site (`true`) or disabled (`false`).<br /><br /> The default value is `false`.|  
|`maxLogFiles`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of failed request tracing log files to keep for the site.<br /><br /> The default value is 50.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`siteDefaults`|Specifies default settings for all sites on the server.|  
  
## Remarks  
 For more information about the `traceFailedRequestsLogging` element, see the following topic on the Microsoft IIS.net Web site: [Default Trace Failed Requests Logging for a Site \<traceFailedRequestsLogging>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/traceFailedRequestsLogging).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|