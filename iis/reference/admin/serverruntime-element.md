---
title: "serverRuntime Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f52a14e7-3d22-41cc-966b-a90c6930d4a0
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# serverRuntime Element
> [!NOTE]
>  For more information about the `serverRuntime` element, see the following topic on the Microsoft IIS.net Web site: [Server Runtime \<serverRuntime>](http://www.iis.net/ConfigReference/system.webServer/serverRuntime).  
  
 Configures request limits for applications on a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`alternateHostName`|Optional `string` attribute.<br /><br /> Specifies the host name to use for redirection.|  
|`appConcurrentRequestLimit`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of requests that can be queued for an application.<br /><br /> The default value is 5000.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether applications on the Web server are able to serve content (`true`) or not are not able to serve content (`false`).<br /><br /> The default value is `true`.|  
|`enableNagling`|Optional `Boolean` attribute.<br /><br /> Specifies whether nagling is enabled (`true`) or disabled (`false`). The default value is `false`. **Note:**  Nagling is an optimization for HTTP over TCP that increases efficiency by trying to minimize the number of packets that are required before data is sent. It works by waiting to send a packet until its data area is full, until a 200-millisecond time-out period expires, or until the sender indicates that it is finished sending data. IIS versions 5.1 and earlier use nagling for all data sent to the client. Nagling has a possible downside. If an extension does not fill up the packet, there is still a delay of 200 milliseconds before the response is sent. This behavior is seen most often when you use ISAPI extensions that support an HTTP `Keep-Alive` header in the response to the client. In this case, IIS does not close the connection after the response, so the final packet ends up waiting for 200 milliseconds.|  
|`frequentHitThreshold`|Optional `uint` attribute.<br /><br /> Specifies the number of times a URL must be requested, within the time span specified in the `frequentHitTimePeriod` attribute, to be considered frequently hit. The value must be between 1 and 2147483647.<br /><br /> The default value is 2.|  
|`frequentHitTimePeriod`|Optional `timeSpan` attribute.<br /><br /> Specifies the time interval in which a URL must be requested the number of times specified in the `frequentHitThreshold` attribute before it is considered to be frequently hit.<br /><br /> The default value is 00:00:10 (10 seconds).|  
|`maxRequestEntityAllowed`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of bytes that can be in an entity body of a request. If the `Content-Length` header specifies a larger number, IIS sends a 403 error response.<br /><br /> The default value is 4294967295 (unlimited).|  
|`uploadReadAheadSize`|Optional `uint` attribute.<br /><br /> Specifies the number of bytes that a Web server will read into a buffer and pass to an ISAPI extension or module. This occurs once per client request. The ISAPI extension or module receives any additional data directly from the client. The value must be between 0 and 2147483647.<br /><br /> The default value is 49152.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `serverRuntime` element, see the following topic on the Microsoft IIS.net Web site: [Server Runtime \<serverRuntime>](http://www.iis.net/ConfigReference/system.webServer/serverRuntime).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|