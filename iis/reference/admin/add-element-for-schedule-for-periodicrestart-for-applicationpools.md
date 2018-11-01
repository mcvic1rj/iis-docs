---
title: "add Element for schedule for periodicRestart for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6c2339ba-8624-4253-8d77-4611970c71ff
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# add Element for schedule for periodicRestart for applicationPools
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
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
|`recycling`|Configures recycling settings for an application pool.|  
|`periodicRestart`|Specifies conditions under which an application pool is recycled.|  
|`schedule`|Specifies the time interval for when the worker processes in an application pool are restarted.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Periodic Restart Schedules \<add>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|