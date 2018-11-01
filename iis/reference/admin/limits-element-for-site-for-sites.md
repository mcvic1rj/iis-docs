---
title: "limits element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: adaa8d9b-5730-4d0b-9b45-7411adc5241b
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# limits element for site for sites
> [!NOTE]
>  For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [Limits for a Web Site \<limits>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/limits).  
  
 Configures settings to limit the amount of bandwidth, the number of connections, or the amount of time for connections to a site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`connectionTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the time (in seconds) that IIS waits before it disconnects a connection that is considered inactive. Connections can be considered inactive for the following reasons:<br /><br /> -   The HTTP.sys Timer_ConnectionIdle timer expired. The connection expired and remains idle.<br />-   The HTTP.sys Timer_EntityBody timer expired. The connection expired before the request entity body arrived. When it is clear that a request has an entity body, the HTTP API turns on the Timer_EntityBody timer. Initially, the limit of this timer is set to the `connectionTimeout` value. Each time another data indication is received on this request, the HTTP API resets the timer to give the connection more minutes as specified in the `connectionTimeout` attribute.<br />-   The HTTP.sys Timer_AppPool timer expired. The connection expired because a request waited too long in an application pool queue for a server application to dequeue and process it. This timeout duration is `connectionTimeout`.<br /><br /> The default value is 00:02:00 (two minutes).|  
|`maxBandwidth`|Optional `uint` attribute.<br /><br /> Specifies the maximum network bandwidth used for a site. Use this setting to help prevent overloading the network with IIS activity.<br /><br /> The default value is 4294967295.|  
|`maxConnections`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of simultaneous connections to the site. The valid range is 0 to 4294967295 (unlimited).<br /><br /> The default value is 4294967295.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [Limits for a Web Site \<limits>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/limits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|