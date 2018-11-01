---
title: "webLimits Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 882ac445-ad3d-422b-b139-96591c97a283
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# webLimits Element
> [!NOTE]
>  For more information about the `webLimits` element, see the following topic on the Microsoft IIS.net Web site: [Web Limits \<webLimits>](http://www.iis.net/ConfigReference/system.applicationHost/webLimits).  
  
 Configures TCP/IP connection and bandwidth limits.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`connectionTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the time that IIS waits before it disconnects a connection considered inactive.<br /><br /> The default value is 00:02:00.|  
|`demandStartThreshold`|Optional `int` attribute.<br /><br /> Specifies the maximum number of worker processes allowed to run concurrently on a Web server. You can use this property to prevent IIS servers from becoming unresponsive when too many worker processes have been started.<br /><br /> The default value is 2147483647.|  
|`dynamicIdleThreshold`|Optional `int` attribute.<br /><br /> Specifies the percentage of committed physical RAM. The valid integer range is from 0 through 10000. The Windows Process Activation Service (WAS) uses this threshold value to dynamically shorten the idle time-out of worker processes. For more information, see the Remarks section.<br /><br /> The default value is 0.|  
|`headerWaitTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the time that the server waits for all HTTP headers for the request to be received before disconnecting the client. The purpose of this attribute is to help prevent a common variant of the Denial of Service (DoS) attack that attempts to max out connection limits and keep those connections connected.<br /><br /> The default value is 00:00:00.|  
|`maxGlobalBandWidth`|Optional `int` attribute.<br /><br /> Specifies the maximum total bandwidth for the server. Setting the value to -1 enables unlimited bandwidth for the server.<br /><br /> The default value is -1.|  
|`minBytesPerSecond`|Optional `int` attribute.<br /><br /> Specifies the minimum throughput rate, in bytes, that HTTP.sys enforces when it sends data from the client to the server and back from the server to the client. The `minBytesPerSecond` attribute prevents malicious or malfunctioning software clients from using resources by holding a connection open with minimal data. If the throughput rate is lower than the `minBytesPerSecond` setting, the connection is terminated.<br /><br /> The default value is 240.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `webLimits` element, see the following topic on the Microsoft IIS.net Web site: [Web Limits \<webLimits>](http://www.iis.net/ConfigReference/system.applicationHost/webLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [WebLimitsSection Class](../../reference/admin/weblimitssection-class.md)