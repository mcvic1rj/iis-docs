---
title: "DynamicTypeSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: aad015a1-5db6-4792-aa51-300cde9889f9
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# DynamicTypeSettings Class
Specifies the MIME types that IIS serves with dynamic compression.  
  
## Syntax  
  
```vbs  
class DynamicTypeSettings: EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `DynamicTypeSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DynamicTypes`|An array of [HttpCompressionMimeTypeElement](../../reference/admin/httpcompressionmimetypeelement-class.md) values that specify whether IIS will dynamically compress a particular MIME type before serving it.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `DynamicTypes` array property of the [HttpCompressionSection](../../reference/admin/httpcompressionsection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `DynamicTypeSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Compression Modules](http://go.microsoft.com/fwlink/?LinkId=64721)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [HttpCompressionMimeTypeElement Class](../../reference/admin/httpcompressionmimetypeelement-class.md)   
 [HttpCompressionSchemeElement Class](../../reference/admin/httpcompressionschemeelement-class.md)   
 [HttpCompressionSection Class](../../reference/admin/httpcompressionsection-class.md)   
 [StaticTypeSettings Class](../../reference/admin/statictypesettings-class.md)