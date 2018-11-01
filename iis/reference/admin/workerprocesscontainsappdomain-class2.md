---
title: "WorkerProcessContainsAppDomain Class2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c7172642-0b13-5b01-450d-874b79e798d5
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# WorkerProcessContainsAppDomain Class2
Provides a relationship between a worker process and its application domains.  
  
## Syntax  
  
```vbs  
class WorkerProcessContainsAppDomain : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `WorkerProcessContainsAppDomain` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [WorkerProcess](../../reference/admin/workerprocess-class2.md) object that represents an IIS worker process. A key property.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [AppDomain](../../reference/admin/appdomain-class.md) object that represents an IIS application domain. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This association class is useful for retrieving all the loaded application domains for each worker process on a Web server.  
  
## Example  
 The following example displays the loaded application domains on a Web server. The first part uses a WMI query. The second part uses the `WorkerProcessContainsAppDomain` association class.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get application domains on the server by using a WMI query.  
Set AppDomains = oWebAdmin.ExecQuery ("Select * from AppDomain")  
  
WScript.Echo "AppDomain Count: " & AppDomains.Count  
WScript.Echo  
For Each AppDomain In AppDomains  
    WScript.Echo "AppDomain site name: " + AppDomain.SiteName  
    WScript.Echo "AppDomain process ID: " & AppDomain.ProcessID  
    WScript.Echo "AppDomain ID: " + AppDomain.Id  
    WScript.Echo "AppDomain application path: " & _  
        AppDomain.ApplicationPath  
    WScript.Echo       
Next  
  
WScript.Echo  
  
' Get the application domains for each worker process by using  
' the WorkerProcessContainsAppDomain association.  
Set oWorkerProcesses = oWebAdmin.InstancesOf("WorkerProcess")  
  
For Each oWorkerProcess In oWorkerProcesses  
    WScript.Echo "Worker Process Process ID: " & oWorkerProcess.ProcessID  
    Set oAppDomains = _  
    oWorkerProcess.Associators_("WorkerProcessContainsAppDomain")  
  
    WScript.Echo "AppDomainCount: " & oAppDomains.Count  
    WScript.Echo  
    WScript.Echo "List of AppDomains"  
    WScript.Echo "------------------"  
    For Each oAppDomain In oAppDomains  
        WScript.Echo "Application domain process ID: " & _  
            oAppDomain.ProcessId  
        WScript.Echo "Application domain application path:" & _  
            oAppDomain.ApplicationPath  
        WScript.Echo " Application domain physical path: " & _  
            oAppDomain.PhysicalPath  
        WScript.Echo  
    Next   
Next  
```  
  
 Note the following syntax from the preceding code example.  
  
 `Set oAppDomains = _`  
  
 `oWorkerProcess.Associators_("WorkerProcessContainsAppDomain")`  
  
 To simplify your code, you can instead use the following syntax, which enables you to use the association without having to remember its exact name.  
  
 `Set oAppDomains = oWorkerProcess.Associators_(, "AppDomain")`  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `WorkerProcessContainsAppDomain`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AppDomain Class](../../reference/admin/appdomain-class.md)   
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)   
 [WorkerProcess Class](../../reference/admin/workerprocess-class2.md)