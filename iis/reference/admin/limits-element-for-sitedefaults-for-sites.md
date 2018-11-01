---
title: "limits Element for siteDefaults for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1a4dc2c3-31d6-4284-8504-cbe88dd0fdd8
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# limits Element for siteDefaults for sites
> [!NOTE]
>  For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [Default Limits for Web Sites \<limits>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/limits).  
  
 Configures default settings to limit the amount of bandwidth, the number of connections, or the amount of time for connections to sites on the server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`connectionTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the time (in seconds) that IIS waits before it disconnects a connection that is considered inactive. Connections can be considered inactive for the following reasons:<br /><br /> -   The HTTP.sys Timer_ConnectionIdle timer expired. The connection expired and remains idle.<br />-   The HTTP.sys Timer_EntityBody timer expired. The connection expired before the request entity body arrived. When it is clear that a request has an entity body, the HTTP API turns on the Timer_EntityBody timer. Initially, the limit of this timer is set to the `connectionTimeout` value. Each time another data indication is received on this request, the HTTP API resets the timer to give the connection more minutes as specified in the `connectionTimeout` attribute.<br />-   The HTTP.sys Timer_AppPool timer expired. The connection expired because a request waited too long in an application pool queue for a server application to dequeue and process it. This time-out duration is `connectionTimeout`.<br /><br /> The default value is 00:02:00 (two minutes).|  
|`maxBandwidth`|Optional `uint` attribute.<br /><br /> Specifies the maximum network bandwidth used for a site. Use this setting to help prevent overloading the network with IIS activity. The valid range is 0 to 1023, or 4294967295 (unlimited).<br /><br /> The default value is 4294967295.|  
|`maxConnections`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of simultaneous connections to a site. The valid range is 0 to 4294967295 (unlimited).<br /><br /> The default value is 4294967295.|  
  
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
 For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [Default Limits for Web Sites \<limits>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/limits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|