---
title: "Server.BeginUpdateBatch Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6a748c8c-c7a4-4adc-846b-5388f8064b2f
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# Server.BeginUpdateBatch Method
Begins a batch of configuration changes for the specified path.  
  
## Syntax  
  
```vbs  
oServer.BeginUpdateBatch  
```  
  
```jscript#  
oServer.BeginUpdateBatch();  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`Path`|A `string` value that specifies the path to which the configuration changes will be applied.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 This method sets a flag in the provider after which incoming change notifications and calls to commit changes are ignored.  
  
 The configuration changes that are made will be stored in memory until the [EndUpdateBatch](../../reference/admin/server-endupdatebatch-method.md) method of the [Server](../../reference/admin/server-class1.md) object is called.  
  
 Batch updates should be done between calls to the `BeginUpdateBatch` method and the `EndUpdateBatch` method. All updates should be made to the same commit path.  
  
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
 [Server.EndUpdateBatch Method](../../reference/admin/server-endupdatebatch-method.md)