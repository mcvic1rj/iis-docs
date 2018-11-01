---
title: "AspSession Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 56b14f51-9718-e5b5-28ab-12687cb8167f
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# AspSession Class
Configures properties related to ASP sessions.  
  
## Syntax  
  
```vbs  
class AspSession : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `AspSession` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AllowSessionState`|A read/write `boolean` value. `true` if session state persistence is enabled for the ASP application; otherwise, `false`. The default is `true`.|  
|`KeepSessionIdSecure`|A read/write `boolean` value. `true` if a session ID is sent as a secure cookie when it is assigned over a secure channel; otherwise, `false`. The default is `true`.|  
|`Max`|A read/write `uint32` value that specifies the maximum number of concurrent sessions that IIS will permit. **Note:**  Although the IIS_Schema.xml file specifies 4294967295 (unlimited) as the default for this property, the default returned by the WMI provider is -1.|  
|`Timeout`|A read/write `datetime` value that specifies the default amount of time that a session object is maintained after the last request associated with the object is made. The default is 20 minutes.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Session` property of the [AspSection](../../reference/admin/aspsection-class1.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `AspSession`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AspCache Class](../../reference/admin/aspcache-class.md)   
 [AspComPlus Class](../../reference/admin/aspcomplus-class.md)   
 [AspLimits Class](../../reference/admin/asplimits-class.md)   
 [AspSection Class](../../reference/admin/aspsection-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)