---
title: "SegmentElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: cf01de87-faab-2713-2b85-8d18629dd664
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# SegmentElement Class
Specifies a URL segment whose content will not be served to the client.  
  
## Syntax  
  
```vbs  
class SegmentElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SegmentElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Segment`|A required unique read/write `string` value that specifies a URL segment whose content will not be served to the client. Wildcard or regular expressions are not supported. The key property. **Note:**  A segment is the part of a URL between two slashes or the part of the URL following the last slash. For example, the URL /segment1/segment2/segment3.asp has three segments: segment1, segment2, and segment3.asp. **Note:**  The following segments are blocked by default: bin, App_code, App_GlobalResources, App_LocalResources, App_WebReferences, App_Data, and App_Browsers.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `HiddenSegments` property of the [HiddenSegmentSettings](../../reference/admin/hiddensegmentsettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `SegmentElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [HiddenSegmentSettings Class](../../reference/admin/hiddensegmentsettings-class.md)   
 [RequestFilteringSection Class](../../reference/admin/requestfilteringsection-class.md)