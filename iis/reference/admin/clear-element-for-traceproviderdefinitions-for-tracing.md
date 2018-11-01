---
title: "clear Element for traceProviderDefinitions for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7da207df-b2c2-4abd-887b-ecc768c82a8a
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# clear Element for traceProviderDefinitions for tracing
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Provider Definitions \<traceProviderDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions).  
  
 Removes all references to trace providers from the trace provider collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceProviderDefinitions`|Defines the trace providers that are used on the Web server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Provider Definitions \<traceProviderDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceproviderdefinitions-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceproviderdefinitions-for-tracing.md)