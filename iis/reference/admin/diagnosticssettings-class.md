---
title: "DiagnosticsSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fcaedf87-b8b1-4520-1213-c8d107069ec6
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# DiagnosticsSettings Class
Specifies whether a Web service returns exceptions to the client.  
  
## Syntax  
  
```vbs  
class DiagnosticsSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `DiagnosticsSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`SuppressReturningExceptions`|A read/write `boolean` value. `true` if the XML Web service suppresses return exceptions to the client; otherwise, `false`. The default is `false`.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Diagnostics` property of the [WebServicesSection](../../reference/admin/webservicessection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `DiagnosticsSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [WebServicesSection Class](../../reference/admin/webservicessection-class.md)