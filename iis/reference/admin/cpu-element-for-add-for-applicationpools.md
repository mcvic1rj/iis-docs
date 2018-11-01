---
title: "cpu Element for add for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d5416180-5a16-46a7-941c-4b009e2e6215
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# cpu Element for add for applicationPools
> [!NOTE]
>  For more information about the `cpu` element, see the following topic on the Microsoft IIS.net Web site: [CPU Settings for an Application Pool \<cpu>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/cpu).  
  
 Configures values for CPU usage parameters and CPU actions that will be used an application pools.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`action`|Optional `enum` attribute.<br /><br /> Configures the action(s) that IIS takes when an worker process exceeds its configured CPU limit. The `action` attribute is configured on a per-application pool basis.<br /><br /> The `action` attribute can be one of the following possible values. The default value is `NoAction`.<br /><br /> -   `KillW3wp:`<br />     - Application pool worker processes that exceed their CPU limit will be forced to shut down.<br />     - The numeric value is 1.<br /><br /> -   `NoAction:`<br />     - No action is taken when the CPU limit is exceeded. A warning is written to the event log.<br />     - The numeric value is 0.|  
|`limit`|Optional `uint` attribute.<br /><br /> Configures the maximum percentage of CPU time (in 1/1000ths of one percent) that the worker processes in an application pool are allowed to consume over a period of time as indicated by the `resetInterval` attribute. If the limit set by the `limit` attribute is exceeded, an event is written to the event log and an optional set of events can be triggered. These optional events are determined by the `action` attribute.<br /><br /> The default value is `0`, which disables CPU limiting.|  
|`resetInterval`|Optional `timeSpan` attribute.<br /><br /> Specifies the reset period (in minutes) for CPU monitoring and throttling limits on an application pool. When the number of minutes elapsed since the last process accounting reset equals the number specified by this property, IIS resets the CPU timers for both the logging and limit intervals.<br /><br /> **Important** The value in `resetInterval` must be greater than the time between logging operations, otherwise IIS will reset counters before logging has occurred, and process accounting will not occur.<br /><br /> Because process accounting in IIS uses Windows job objects to monitor CPU times for the whole process, process accounting will only log and throttle applications that are isolated in a separate process from IIS.<br /><br /> The default value is `0`, which disables CPU monitoring.|  
|`smpAffinitized`|Optional `Boolean` attribute.<br /><br /> Specifies whether a particular worker process assigned to an application pool should also be assigned to a given CPU. This property is used together with the `smpProcessorAffinityMask` attribute.<br /><br /> The default value is `false`.|  
|`smpProcessorAffinityMask`|Optional `uint` attribute.<br /><br /> Configures the hexadecimal processor mask for multi-processor computers, which indicates to which CPU the worker processes in an application pool should be bound. Before this property takes effect, the `smpAffinitized` attribute must be set to `true` for the application pool.<br /><br /> Do not set this property to `0`. Doing so disables symmetric multiprocessing (SMP) affinity and creates an error condition. This means that processes running on one CPU will not remain affiliated with that CPU throughout their lifetime.<br /><br /> The default value is 4294967295. If you set the value to 1 (which corresponds to 00000000000000001 in binary), the worker processes in an application pool run on only the first processor. If you set the value to 2 (which corresponds to 0000000000000010 in binary), the worker processes run on only the second processor. If you set the value to 3 (which corresponds to 0000000000000011 in binary) the worker processes run on both the first and second processors.|  
|`smpProcessorAffinityMask2`|Optional uint attribute.<br /><br /> Specifies the high-order DWORD hexadecimal processor mask for 64-bit multi-processor computers, which indicates to which CPU the worker processes in an application pool should be bound. Before this property takes effect, the smpAffinitized attribute must be set to true for the application pool.<br /><br /> Note: On 64-bit computers, the smpProcessorAffinityMask attribute contains the low-order DWORD for the processor mask, and the smpProcessorAffinityMask2 attribute contains the high-order DWORD for the processor mask. On 32-bit computers, the smpProcessorAffinityMask2 attribute has no effect.<br /><br /> The default value is 4294967295.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
  
## Remarks  
 For more information about the `cpu` element, see the following topic on the Microsoft IIS.net Web site: [CPU Settings for an Application Pool \<cpu>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/cpu).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|