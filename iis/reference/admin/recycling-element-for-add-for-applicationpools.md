---
title: "recycling Element for add for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2f8c3a72-2249-4934-9a13-8fe76c3ca31b
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# recycling Element for add for applicationPools
> [!NOTE]
>  For more information about the `recycling` element, see the following topic on the Microsoft IIS.net Web site: [Recycling Settings for an Application Pool \<recycling>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling).  
  
 Configures recycling settings for an application pool.  
  
> [!NOTE]
>  Individual application pool settings override default settings unless the default settings are locked.  
  
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
|`periodicRestart`|Optional element.<br /><br /> Specifies conditions under which application pools are recycled.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
  
## Remarks  
 For more information about the `recycling` element, see the following topic on the Microsoft IIS.net Web site: [Recycling Settings for an Application Pool \<recycling>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<periodicRestart>](../../reference/admin/periodicrestart-element-for-recycling-for-add-for-applicationpools.md)