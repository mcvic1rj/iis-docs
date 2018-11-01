---
title: "recycling Element for applicationPoolDefaults for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8e392bc1-2191-446b-acbb-f261428e35b9
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# recycling Element for applicationPoolDefaults for applicationPools
> [!NOTE]
>  For more information about the `recycling` element, see the following topic on the Microsoft IIS.net Web site: [Recycling Settings for an Application Pool \<recycling>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling).  
  
 Configures default recycling settings for all application pools on a server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`disallowOverlappingRotation`|Optional `Boolean` attribute.<br /><br /> Specifies whether the WWW Service should start another worker process to replace the existing worker process while that process is shutting down. The value of this property should be set to `true` if the worker process loads any application code that does not support multiple worker processes.<br /><br /> The default value is `false`.|  
|`disallowRotationOnConfigChange`|Optional `Boolean` attribute.<br /><br /> Specifies whether the WWW Service should rotate worker processes in an application pool when the configuration has changed.<br /><br /> The default value is `false`.|  
|`logEventOnRecycle`|Optional `flags` attribute.<br /><br /> Specifies that IIS should log an event when an application pool is recycled. The `logEventOnRecycle` property must have a bit set corresponding to the reason for the recycle if IIS is to log the event.<br /><br /> The `logEventOnRecycle` attribute can be one or more of the following possible values. If you specify more than one value, separate them with a comma (,). The default values are `Time`, `Memory`, and `PrivateMemory`.<br /><br /> `ConfigChange`:<br /><br /> - Log an event when an application pool recycles because of a configuration change.<br /><br /> - The numeric value is 64.<br /><br /> `IsapiUnhealthy`:<br /><br /> - Log an event when an application pool recycles after an ISAPI extension reports to the worker process that it is in an unhealthy state.<br /><br /> - The numeric value is 16.<br /><br /> `Memory`:<br /><br /> - Log an event when an application pool recycles after it uses a specified amount of virtual memory.<br /><br /> - The numeric value is 8.<br /><br /> `OnDemand`:<br /><br /> - Log an event when an application pool is recycled immediately to correct a problem.<br /><br /> - The numeric value is 32.<br /><br /> `PrivateMemory`:<br /><br /> - Log an event when an application pool recycles after it uses a specified amount of virtual memory.<br /><br /> - The numeric value is 128.<br /><br /> `Requests`:<br /><br /> - Log an event when an application pool recycles after it reaches a configured number of requests.<br /><br /> - The numeric value is 2.<br /><br /> `Schedule`:<br /><br /> - Log an event when an application pool recycles after it reaches a configured time of day.<br /><br /> - The numeric value is 4.<br /><br /> `Time`:<br /><br /> - Log an event when an application pool recycles after a configured time.<br /><br /> - The numeric value is 1.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`periodicRestart`|Optional element.<br /><br /> Specifies settings for application pool recycling.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Specifies the root element for the configuration for all application pools on a server.|  
|`applicationPoolDefaults`|Specifies default settings for all application pools on a server.|  
  
## Remarks  
 For more information about the `recycling` element, see the following topic on the Microsoft IIS.net Web site: [Recycling Settings for an Application Pool \<recycling>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<periodicRestart>](../../reference/admin/periodicrestart-element-for-recycling-for-applicationpooldefaults.md)