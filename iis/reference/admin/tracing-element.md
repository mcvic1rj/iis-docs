---
title: "tracing Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d76909a5-6422-43c5-8e21-ae5abfee736c
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# tracing Element
> [!NOTE]
>  For more information about the `tracing` element, see the following topic on the Microsoft IIS.net Web site: [Tracing \<tracing>](http://www.iis.net/ConfigReference/system.webServer/tracing).  
  
 Configures request trace settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`traceFailedRequests`|Optional element.<br /><br /> Contains settings for tracing failed requests on the Web server.|  
|`traceProviderDefinitions`|Optional element.<br /><br /> Defines the trace providers that are used on the Web server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `tracing` element, see the following topic on the Microsoft IIS.net Web site: [Tracing \<tracing>](http://www.iis.net/ConfigReference/system.webServer/tracing).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<traceFailedRequests>](../../reference/admin/tracefailedrequests-element-for-tracing.md)   
 [\<traceProviderDefinitions>](../../reference/admin/traceproviderdefinitions-element-for-tracing.md)