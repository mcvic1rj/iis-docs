---
title: "WorkerProcess Class2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dd8bf382-1523-1da8-f2b6-0cceb66fec82
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# WorkerProcess Class2
Represents a Windows Process Activation Service (WAS) worker process (w3wp.exe).  
  
## Syntax  
  
```vbs  
class WorkerProcess : Object  
```  
  
## Methods  
 The following table lists the methods exposed by the `WorkerProcess` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetExecutingRequests](../../reference/admin/workerprocess-getexecutingrequests-method2.md)|Gets the requests that are currently assigned to a worker process.|  
|[GetState](../../reference/admin/workerprocess-getstate-method2.md)|Returns the run-time state of a worker process.|  
  
## Properties  
 The following table lists the properties exposed by the `WorkerProcess` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AppPoolName`|A read-only `string` that contains the name of the application pool to which the worker process belongs. The default is "DefaultAppPool".|  
|`GUID`|A read-only `string` that contains the GUID for the worker process.|  
|`ProcessID`|A read-only `uint32` that contains the worker process ID. The only key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [Object](../../reference/admin/object-class1.md)  
  
 `WorkerProcess`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Object Class](../../reference/admin/object-class1.md)