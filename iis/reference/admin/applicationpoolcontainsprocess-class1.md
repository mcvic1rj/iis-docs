---
title: "ApplicationPoolContainsProcess Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b5947055-8ec9-28bb-9b49-978ea2ae5e7d
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# ApplicationPoolContainsProcess Class1
Provides a relationship between an application pool and its worker processes.  
  
## Syntax  
  
```vbs  
class ApplicationPoolContainsProcess : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationPoolContainsProcess` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [ApplicationPool](../../reference/admin/applicationpool-class1.md) object that represents an IIS application pool. A key property.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [WorkerProcess](../../reference/admin/workerprocess-class2.md) object that represents a Windows Process Activation Service (WAS) worker process. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 A `WorkerProcess` object is transient; it may cease to exist when its application pool is recycled or when it reaches its idle time-out. Be prepared for this possibility if you write a script that interacts with a `WorkerProcess` object over any significant length of time.  
  
## Example  
 The following example returns the ID for every worker process in each application pool on a server.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Return all application pools that are present on the server.  
Set colAppPools = oWebAdmin.ExecQuery("SELECT * FROM ApplicationPool")  
  
' Return the name of each application pool.  
For Each oAppPool In colAppPools  
        WScript.Echo "Application Pool Name: " & oAppPool.Name  
  
        ' Get all worker processes in the application pool.  
        Set oProcesses = oAppPool.Associators_("ApplicationPoolContainsProcess")  
  
        ' Return the ID of each worker process in the application pool.  
        For Each oProcess In oProcesses  
                WScript.Echo "Worker Process ID: " & oProcess.ID  
        Next  
Next  
```  
  
 Note the following line from the preceding code example.  
  
 `Set colAppPools = oWebAdmin.ExecQuery("SELECT * FROM ApplicationPool")`  
  
 Instead of using the `ExecQuery` method, you can alternatively use the WMI `InstancesOf` method, as follows:  
  
 `Set colAppPools = oWebAdmin.InstancesOf("ApplicationPool")`  
  
 The latter approach enables you to achieve the same result without specifying a query syntax.  
  
 With either approach, the script produces an output similar to the following:  
  
 `Application Pool Name: DefaultAppPool`  
  
 `Application Pool Name: Classic .NET AppPool`  
  
 `Application Pool Name: NewAppPool1`  
  
 `Application Pool Name: NewAppPool2`  
  
 `Application Pool Name: NewAppPool3`  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `ApplicationPoolContainsProcess`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)   
 [ProcessModelSettings Class](../../reference/admin/processmodelsettings-class1.md)   
 [WorkerProcess Class](../../reference/admin/workerprocess-class2.md)