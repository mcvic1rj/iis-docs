---
title: "periodicRestart Element for recycling for applicationPoolDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0378bb1b-7419-47a1-93d1-2a5521267038
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# periodicRestart Element for recycling for applicationPoolDefaults
> [!NOTE]
>  For more information about the `periodicRestart` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Settings for Application Pool Recycling \<periodicRestart>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart).  
  
 Specifies conditions under which application pools are recycled.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`memory`|Optional `uint` attribute.<br /><br /> Specifies the amount of virtual memory (in kilobytes) that a worker process can use before the worker process is recycled. The maximum value supported for this property is 4,294,967 KB.<br /><br /> The default value is `0`, which disables the attribute.|  
|`privateMemory`|Optional `uint` attribute.<br /><br /> Specifies the amount of private memory (in kilobytes) that a worker process can use before the worker process recycles. The maximum value supported for this property is 4,294,967 KB.<br /><br /> The default value is `0`, which disables the attribute.|  
|`requests`|Optional `uint` attribute.<br /><br /> Specifies that the worker process should be recycled after it processes a specific number of requests.<br /><br /> The default value is `0`, which disables the attribute.|  
|`time`|Optional `timeSpan` attribute.<br /><br /> Specifies that the worker process should be recycled after a specified amount of time has elapsed.<br /><br /> The default value is `29:00:00` (29 hours).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`schedule`|Optional element.<br /><br /> Specifies the scheduling of periodic restarts of application pools.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPoolDefaults`|Specifies default settings for all application pools on the server.|  
|`recycling`|Specifies application pool recycling settings.|  
  
## Remarks  
 For more information about the `periodicRestart` element, see the following topic on the Microsoft IIS.net Web site: [Periodic Restart Settings for Application Pool Recycling \<periodicRestart>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/recycling/periodicRestart).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<schedule>](../../reference/admin/schedule-element-for-periodicrestart-for-applicationpooldefaults.md)