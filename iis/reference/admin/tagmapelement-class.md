---
title: "TagMapElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d7ab3ae1-eb52-436f-ae9b-8be91af32849
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# TagMapElement Class
Contains a statement that remaps a tag type.  
  
## Syntax  
  
```vbs  
class TagMapElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `TagMapElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`MappedTagType`|A read/write nonempty `string` value that specifies the name of the type to which the tag is remapped. **Note:**  An empty string value for this property will cause the configuration system to throw an exception when the object is serialized.|  
|`TagType`|A read-only nonempty `string` value that specifies the name of the original type for the tag that is being remapped. The key property. **Note:**  An empty string value for this property will cause the configuration system to throw an exception when the object is serialized.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are exposed as members of the `TagMapping` property on the [TagMapInfo](../../reference/admin/tagmapinfo-class.md) class.  
  
 Tag remapping, which occurs at compile time, replaces the original tag type (specified by the `TagType` property) with the mapped type (specified by the `MappedTagType` property) for all pages and controls in the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application in the scope of the configuration file.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `TagMapElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.TagMapInfo?displayProperty=fullName>   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [PagesSection Class](../../reference/admin/pagessection-class.md)   
 [TagMapInfo Class](../../reference/admin/tagmapinfo-class.md)