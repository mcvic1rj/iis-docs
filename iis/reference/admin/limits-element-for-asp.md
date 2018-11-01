---
title: "limits Element for asp | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 30a6ed90-6d53-4716-9367-904275f60d85
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# limits Element for asp
> [!NOTE]
>  For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [ASP Limits \<limits>](http://www.iis.net/ConfigReference/system.webServer/asp/limits).  
  
 Specifies limits for various Active Server Pages (ASP) properties.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`bufferingLimit`|Optional `integer` attribute.<br /><br /> Specifies the maximum size, in bytes, of the ASP buffer. If response buffering is turned on, this property controls the maximum number of bytes that an ASP page can write to the response buffer before a flush occurs. This value is an integer range from 0 to 2147483647.<br /><br /> The default value is 4194304.|  
|`maxRequestEntityAllowed`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of bytes allowed in the entire body of an ASP request. This value is an integer range from 0 to 2147483647.<br /><br /> The default value is 200000.|  
|`processorThreadMax`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of worker threads per processor that ASP can create.<br /><br /> The default value is 25.|  
|`queueConnectionTestTime`|Optional `timespan` attribute.<br /><br /> Specifies the time interval (hh:mm:ss) after which ASP will check to see whether the client is still connected before executing a request. If the client is no longer connected, the request is not processed and is deleted from the queue.<br /><br /> The default value is 00:00:03.|  
|`queueTimeout`|Optional `timespan` attribute.<br /><br /> Specifies the maximum period of time (hh:mm:ss) that an ASP request can wait in the request queue.<br /><br /> The default value is 00:00:00.|  
|`requestQueueMax`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of concurrent ASP requests that are allowed into the request queue.<br /><br /> The default value is 3000.|  
|`scriptTimeout`|Optional `timespan` attribute.<br /><br /> Specifies the maximum period of time (hh:mm:ss) that ASP pages allow a script to run run before terminating the script and writing an event to the Windows Event Log.<br /><br /> The default value is 00:01:30.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`asp`|Configures settings for ASP applications.|  
  
## Remarks  
 For more information about the `limits` element, see the following topic on the Microsoft IIS.net Web site: [ASP Limits \<limits>](http://www.iis.net/ConfigReference/system.webServer/asp/limits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<cache>](../../reference/admin/cache-element-for-asp.md)   
 [\<comPlus>](../../reference/admin/complus-element-for-asp.md)   
 [\<session>](../../reference/admin/session-element-for-asp.md)