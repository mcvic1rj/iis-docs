---
title: "session Element for asp | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e88b7cd8-4231-4954-bcf3-3e58ffbfcbbd
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# session Element for asp
> [!NOTE]
>  For more information about the `session` element, see the following topic on the Microsoft IIS.net Web site: [ASP Session \<session>](http://www.iis.net/ConfigReference/system.webServer/asp/session).  
  
 Specifies Active Server Pages (ASP) session state settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowSessionState`|Optional `Boolean` attribute.<br /><br /> Specifies whether session state persistence for an ASP application is enabled.<br /><br /> The default value is `true`.|  
|`keepSessionIdSecure`|Optional `Boolean` attribute.<br /><br /> Specifies whether a session ID is sent as a secure cookie if assigned over a secure session channel.<br /><br /> The default value is `true`.|  
|`Max`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of concurrent sessions.<br /><br /> The default value is -1.|  
|`timeout`|Optional `timespan` attribute.<br /><br /> Specifies the maximum period of time (hh:mm:ss) that a session object is maintained after the last request associated with the object is made.<br /><br /> The default value is 00:20:00.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`asp`|Configures settings for ASP applications.|  
  
## Remarks  
 For more information about the `session` element, see the following topic on the Microsoft IIS.net Web site: [ASP Session \<session>](http://www.iis.net/ConfigReference/system.webServer/asp/session).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<cache>](../../reference/admin/cache-element-for-asp.md)   
 [\<limits>](../../reference/admin/limits-element-for-asp.md)   
 [\<comPlus>](../../reference/admin/complus-element-for-asp.md)