---
title: "NamespaceInfo Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a8819e4f-ec68-13bd-3236-aecd0d743d23
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# NamespaceInfo Class
Contains namespace references similar to the `Import` directive.  
  
## Syntax  
  
```vbs  
class NamespaceInfo : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `NamespaceInfo` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AutoImportVBNamespace`|A read/write `boolean` value. `true` if the [Microsoft.VisualBasic](http://go.microsoft.com/fwlink/?LinkId=69333) namespace is imported automatically; otherwise, `false`. The default is `true`. **Note:**  For [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] pages written by using Visual Basic, the `VisualBasic` namespace is imported automatically unless the `AutoImportVBNamespace` property is set to `false`.|  
|`Namespaces`|An array of [NamespaceElement](../../reference/admin/namespaceelement-class.md) values that specify namespace references. **Note:**  No validation is performed to verify that the namespace references are valid.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Namespaces` property of the [PagesSection](../../reference/admin/pagessection-class.md) class.  
  
 Each `NamespaceInfo` object is the same as an `Import` (\<%@ Import %>) directive that applies to all pages and controls in the scope of the configuration file. The `Import` directive enables you to import a namespace into your [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] page, which makes all its classes available for use on your page.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `NamespaceInfo`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.NamespaceCollection>   
 <xref:System.Web.Configuration.NamespaceInfo>   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [NamespaceElement Class](../../reference/admin/namespaceelement-class.md)   
 [PagesSection Class](../../reference/admin/pagessection-class.md)   
 [Microsoft.VisualBasic Namespace](http://go.microsoft.com/fwlink/?LinkId=69333)