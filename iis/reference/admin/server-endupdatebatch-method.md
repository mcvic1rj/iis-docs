---
title: "Server.EndUpdateBatch Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 49d4a5bc-0c8e-4e51-9ab6-60285a97257b
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# Server.EndUpdateBatch Method
Ends a batch of configuration changes.  
  
## Syntax  
  
```vbs  
oServer.EndUpdateBatch  
```  
  
```jscript#  
oServer.EndUpdateBatch();  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`DoCommitChanges`|An optional `boolean` value. `true` if the batch changes of configuration changes that have been made will be committed; otherwise, `false`.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 Batch updates should be done between calls to the [BeginUpdateBatch](../../reference/admin/server-beginupdatebatch-method.md) method of the [Server](../../reference/admin/server-class1.md) class and this method. All updates should be made to the same commit path that you specify in the `Path` parameter of the `BeginUpdateBatch` method. If you want to discard the changes that have been made in memory, set the `DoCommitChanges` parameter to `false`.  
  
> [!NOTE]
>  The `BeginUpdateBatch` and `EndUpdateBatch` methods work only while the current WMI worker process is running. If the process is shut down by WMI due to idle timeout (normally after 30 seconds), any changes that have been made will be lost.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Server Class](../../reference/admin/server-class1.md)   
 [Server.BeginUpdateBatch Method](../../reference/admin/server-beginupdatebatch-method.md)