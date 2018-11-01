---
title: "RecyclingSettings Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dee0e6af-883c-f4ac-ee15-d2de53ddb010
caps.latest.revision: 25
author: "shirhatti"
manager: "wpickett"
---
# RecyclingSettings Class1
Specifies recycling settings for worker processes.  
  
## Syntax  
  
```vbs  
class RecyclingSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by `RecyclingSettings`.  
  
|Name|Description|  
|----------|-----------------|  
|`DisallowOverlappingRotation`|A read/write `boolean` value. `true` if the Windows Process Activation Service (WAS) starts up another worker process to replace one that is still running; otherwise, `false`. The default is `false`. Set `DisallowOverlappingRotation` to `true` if the worker process loads any application code that does not support two worker processes at the same time.|  
|`DisallowRotationOnConfigChange`|A read/write `boolean` value. `true` if WAS rotates worker processes in an application pool after the application pool configuration has changed; otherwise, `false`. The default is `false`.<br /><br /> Application pool configuration changes do not affect worker processes that are already running. Set `DisallowRotationOnConfigChange` to `true` if the worker process loads any application code that does not support two worker processes at the same time.|  
|`LogEventOnRecycle`|A read/write `sint32` value that contains a mask that specifies which recycling events will be logged. The possible values are listed later in the Remarks section.|  
|`PeriodicRestart`|A [PeriodicRestartSettings](../../reference/admin/periodicrestartsettings-class.md) object that specifies the conditions under which worker processes will be recycled.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Recycling` property of the [ApplicationPool](../../reference/admin/applicationpool-class1.md) class and the [ApplicationPoolElementDefaults](../../reference/admin/applicationpoolelementdefaults-class1.md) class. `ApplicationPoolElementDefaults` is in turn exposed as the `GlobalApplicationPoolDefaults` property on the [Server](../../reference/admin/server-class1.md) class.  
  
 The following table lists the possible values and the associated keywords and recycling events for the `LogEventOnRecycle` property. The defaults are 1 (`Time`), 8 (`Memory`), and 128 (`PrivateMemory`).  
  
|Value|Keyword|Recycling event|  
|-----------|-------------|---------------------|  
|1|`Time`|The time specified in [PeriodicRestartSettings.Time](../../reference/admin/periodicrestartsettings-class.md) has elapsed since the last recycle. Enabled by default.|  
|2|`Requests`|The number of requests specified in [PeriodicRestartSettings.Requests](../../reference/admin/periodicrestartsettings-class.md) has been reached.|  
|4|`Schedule`|A scheduled recycle specified in [PeriodicRestartSettings.Schedule](../../reference/admin/periodicrestartsettings-class.md) has occurred.|  
|8|`Memory`|A used or virtual memory limit specified in [PeriodicRestartSettings.Memory](../../reference/admin/periodicrestartsettings-class.md) has been reached. Enabled by default.|  
|16|`IsapiUnhealthy`|An ISAPI has failed to respond to a health-monitoring request.|  
|32|`OnDemand`|An administrator has manually triggered a recycle.|  
|64|`ConfigChange`|Application pool configuration changes have been made.|  
|128|`PrivateMemory`|Private memory has reached the amount specified in [PeriodicRestartSettings.PrivateMemory](../../reference/admin/periodicrestartsettings-class.md). Enabled by default.|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `RecyclingSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [PeriodicRestartSettings](../../reference/admin/periodicrestartsettings-class.md)