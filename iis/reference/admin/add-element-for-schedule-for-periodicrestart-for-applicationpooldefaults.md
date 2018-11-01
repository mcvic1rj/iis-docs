---
title: "add Element for schedule for periodicRestart for applicationPoolDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: efd29cd1-bc12-45ab-ba6f-64254f45b5d0
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# add Element for schedule for periodicRestart for applicationPoolDefaults
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Periodic Restart Schedules \<add>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
 Specifies a time to initiate scheduled periodic restarts of an application pool.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`value`|Required `timeSpan` attribute.<br /><br /> Specifies a unique local time, on a 24-hour clock, to begin a scheduled periodic restart of an application pool.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Specifies configuration settings for application pools on a server.|  
|`applicationPoolDefaults`|Specifies default configuration settings that apply to all application pools on a server.|  
|`recycling`|Specifies configuration settings for application pool recycling.|  
|`periodicRestart`|Specifies configuration settings for restarting an application pool.|  
|`schedule`|Specifies configuration settings for restarting an application pool according to a schedule.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Periodic Restart Schedules \<add>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|