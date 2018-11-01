---
title: "WorkerProcess.GetState Method2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b12970b0-a05e-25a1-b3bd-f6dd7df2448c
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# WorkerProcess.GetState Method2
Returns the run-time state of a worker process.  
  
## Syntax  
  
```vbs  
oWorkerProcess.GetState  
```  
  
```jscript#  
var workerProcessState = objWorkerProcess.GetState();  
```  
  
#### Parameters  
 This method takes no parameters.  
  
## Return Value  
 A `uint32` that identifies the application pool state. The return values are shown in the following table.  
  
|Return value|Description|  
|------------------|-----------------|  
|0|Indicates that the worker process is starting.|  
|1|Indicates that the worker process is running.|  
|2|Indicates that the worker process is stopping.|  
|3|Indicates that the worker process is unknown.|  
  
## Remarks  
 This method is new to the [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] WMI provider and has no counterpart in IIS 6.0.  
  
## Example  
 The following example returns the state of every worker process in each application pool on a server.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Return all application pools that are present on the server.  
Set colAppPools = oWebAdmin.ExecQuery("SELECT * FROM ApplicationPool")  
  
' Return each application pool name.  
For Each oAppPool In colAppPools  
    WScript.Echo oAppPool.Name  
    WScript.Echo String(Len(oAppPool.Name), "-")  
  
    ' Get all worker processes in the application pool.  
    Set oWorkerProcesses = _  
        oAppPool.Associators_("ApplicationPoolContainsProcess")  
  
    ' Return each worker process ID and report its state by using  
    ' the GetStateDescription helper function.  
    For Each oWorkerProcess In oWorkerProcesses  
        WScript.Echo "Process ID " & oWorkerProcess.ID & _  
            " is " & GetStateDescription(oWorkerProcess.GetState) & "."  
    Next  
    WScript.Echo  
Next  
  
' Return the text string that corresponds to the state code.  
Function GetStateDescription(StateCode)  
    Select Case StateCode  
        Case 0  
            GetStateDescription = "starting"  
        Case 1  
            GetStateDescription = "running"  
        Case 2  
            GetStateDescription = "stopping"  
        Case 3  
            GetStateDescription = "unknown"  
        Case Else  
            GetStateDescription = _  
                "Attempt to retrieve worker process state failed."  
    End Select  
End Function  
```  
  
 Because [WorkerProcess](../../reference/admin/workerprocess-class2.md) is a transient object, the state reported by WMI when the script is run may no longer be valid after some time has elapsed.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolContainsProcess Class](../../reference/admin/applicationpoolcontainsprocess-class1.md)   
 [WorkerProcess Class](../../reference/admin/workerprocess-class2.md)