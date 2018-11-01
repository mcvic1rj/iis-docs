---
title: "FileExtensionsSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b437c7ab-64b4-f7b7-6f22-a699a37cead7
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# FileExtensionsSettings Class
Configures the filtering of file extensions in requests.  
  
## Syntax  
  
```vbs  
class FileExtensionsSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `FileExtensionsSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AllowUnlisted`|A read/write `boolean` value. `true` if file extensions not listed in the `FileExtensions` property are allowed in requests; otherwise, `false`. The default is `true`.|  
|`ApplyToWebDAV`|A read/write `boolean` value. `true` if the `AllowUnlisted` and `FileExtensions` properties are applied to WebDAV requests; otherwise, `false`. The default is `true`.|  
|`FileExtensions`|An array of read/write [FileExtensionElement](../../reference/admin/fileextensionelement-class.md) values that specifies file extensions that are allowed or denied.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `FileExtensions` property of the [RequestFilteringSection](../../reference/admin/requestfilteringsection-class.md) class. In the ApplicationHost.config file, this class represents the `<fileExtensions>` element of the `<requestFiltering>` section  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `FileExtensionsSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [FileExtensionElement Class](../../reference/admin/fileextensionelement-class.md)   
 [RequestFilteringSection Class](../../reference/admin/requestfilteringsection-class.md)