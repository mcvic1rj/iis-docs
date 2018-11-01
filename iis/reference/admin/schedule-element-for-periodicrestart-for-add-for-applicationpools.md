---
title: "schedule Element for periodicRestart for add for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 476552fb-52a1-4868-beb0-289363a7c624
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# schedule Element for periodicRestart for add for applicationPools
> [!NOTE]
>  For more information about the `schedule` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule).  
  
 Specifies the time interval for when the worker processes in an application pool are restarted.  
  
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
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
|`recycling`|Configures recycling settings for an application pool.|  
|`periodicRestart`|Specifies conditions under which an application pool is recycled.|  
  
## Remarks  
 For more information about the `schedule` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-schedule-for-periodicrestart-for-applicationpools.md)   
 [\<clear>](../../reference/admin/clear-element-for-schedule-for-periodicrestart-for-applicationpools.md)