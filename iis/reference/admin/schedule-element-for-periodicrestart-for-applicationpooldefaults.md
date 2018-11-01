---
title: "schedule Element for periodicRestart for applicationPoolDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a8ada079-18a9-4172-b09b-ebfa0161face
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# schedule Element for periodicRestart for applicationPoolDefaults
> [!NOTE]
>  For more information about the `schedule` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule).  
  
 Specifies the time interval between system restarts of the worker processes in an application pool.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Specifies a value for starting the periodic recycling of an application pool.|  
|`clear`|Optional element.<br /><br /> Specifies that the parent-level configuration settings should be removed from the configuration at this level.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Specifies configuration settings for application pools on a server.|  
|`applicationPoolDefaults`|Specifies default configuration settings that apply to all application pools on a server, unless the settings are overridden at lower levels of the configuration hierarchy.|  
|`recycling`|Specifies configuration settings for application pool recycling.|  
|`periodicRestart`|Specifies configuration settings for periodic restarting of application pools.|  
  
## Remarks  
 For more information about the `schedule` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule).  
  
 The time in the schedule element is expressed as hours and minutes on a 24-hour clock.  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-schedule-for-periodicrestart-for-applicationpooldefaults.md)   
 [\<clear>](../../reference/admin/clear-element-for-schedule-element-for-applicationpooldefaults.md)