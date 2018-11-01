---
title: "clear Element for schedule element for applicationPoolDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0c286133-6845-40bd-85da-db0be6e3d56f
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# clear Element for schedule element for applicationPoolDefaults
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
|`applicationPools`|Specifies configuration settings for application pools on a server.|  
|`applicationPoolDefaults`|Specifies default configuration settings that apply to all application pools on a server, unless the settings are overridden at lower levels of the configuration hierarchy.|  
|`recycling`|Specifies configuration settings for application pool recycling.|  
|`periodicRestart`|Specifies configuration settings for periodic restarting of application pools.|  
|`schedule`|Specifies the scheduled recycling interval for the application pool.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Schedules \<schedule>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart/schedule/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|