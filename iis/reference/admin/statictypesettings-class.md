---
title: "StaticTypeSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 32237c1b-06b3-44e4-b682-5a6abc7b3df7
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# StaticTypeSettings Class
Specifies the MIME types that IIS serves with static compression.  
  
## Syntax  
  
```vbs  
class StaticTypeSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `StaticTypeSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`StaticTypes`|An array of [HttpCompressionMimeTypeElement](../../reference/admin/httpcompressionmimetypeelement-class.md) values that specify whether IIS will statically compress a particular MIME type before serving it.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `StaticTypes` array property of the [HttpCompressionSection](../../reference/admin/httpcompressionsection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `StaticTypeSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Compression Modules](http://go.microsoft.com/fwlink/?LinkId=64721)   
 [DynamicTypeSettings Class](../../reference/admin/dynamictypesettings-class.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [HttpCompressionMimeTypeElement Class](../../reference/admin/httpcompressionmimetypeelement-class.md)   
 [HttpCompressionSchemeElement Class](../../reference/admin/httpcompressionschemeelement-class.md)   
 [HttpCompressionSection Class](../../reference/admin/httpcompressionsection-class.md)