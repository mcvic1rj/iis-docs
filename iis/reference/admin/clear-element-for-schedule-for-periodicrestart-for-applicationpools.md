---
title: "clear Element for schedule for periodicRestart for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e8802f2d-8295-4ca8-b58a-f64cfcd012d8
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# clear Element for schedule for periodicRestart for applicationPools
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
 Removes all references to settings at the parent level of the configuration.  
  
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
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
|`recycling`|Configures recycling settings for an application pool.|  
|`periodicRestart`|Specifies conditions under which an application pool is recycled.|  
|`schedule`|Specifies the time interval for when the worker processes in an application pool are restarted.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|