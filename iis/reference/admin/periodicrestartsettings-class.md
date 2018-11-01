---
title: "PeriodicRestartSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dfb46d88-0d13-f66b-440b-dd7eeef10582
caps.latest.revision: 28
author: "shirhatti"
manager: "wpickett"
---
# PeriodicRestartSettings Class
Specifies the conditions under which worker processes will be recycled.  
  
## Syntax  
  
```vbs  
class PeriodicRestartSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `PeriodicRestartSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Memory`|A read/write `uint32` value that specifies the amount of virtual memory, in kilobytes, that a worker process can use before the worker process recycles. The maximum value is 4,294,967. The default is 0 kilobytes, which means that the amount of virtual memory that a worker process uses will not be a condition for recycling the worker process.|  
|`PrivateMemory`|A read/write `uint32` value that specifies the amount of private memory, in kilobytes, that a worker process can use before the worker process recycles. The maximum value is 4,294,967. The default is 0 kilobytes, which means that the amount of private memory that a worker process uses will not be a condition for recycling the worker process.|  
|`Requests`|A read/write `uint32` value that indicates the number of requests an out-of-process application should process before it is recycled. The default is 0, which means that the number of requests an out-of-process application handles will not be a condition for recycling it.|  
|`Schedule`|An array of [ScheduleElement](../../reference/admin/scheduleelement-class.md) values that specify the local times at which an application will be recycled.|  
|`Time`|A read/write `datetime` value that specifies the amount of time before IIS recycles an isolated out-of-process application. The default value is 0, which disables the recycling.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `PeriodicRestart` property of the [RecyclingSettings](../../reference/admin/recyclingsettings-class1.md) class.  
  
 For more information about the Windows Management Instrumentation (WMI) date/time format, see [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551).  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `PeriodicRestartSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [RecyclingSettings Class](../../reference/admin/recyclingsettings-class1.md)   
 [ScheduleElement Class](../../reference/admin/scheduleelement-class.md)