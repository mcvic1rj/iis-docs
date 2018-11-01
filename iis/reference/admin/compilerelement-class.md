---
title: "CompilerElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d2f44e2f-ae63-421b-9071-ddf9809fc21c
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# CompilerElement Class
Specifies a compiler that is used for Web applications.  
  
## Syntax  
  
```vbs  
class CompilerElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `CompilerElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`CompilerOptions`|A read/write `string` value that specifies compiler-specific options to use during compilation. Overrides any previously defined values.|  
|`Extensions`|A required unique read/write `string` value that contains a semicolon-delimited list of file name extensions used for dynamic code-behind files, files in the code directory, and other referenced files. A key property.|  
|`Language`|A required unique read/write `string` value that contains a semicolon-delimited list of programming languages to use in dynamic compilation files. A key property.|  
|`Type`|A read/write `string` value that specifies the type name of the language compiler to use for dynamic compilation files. **Note:**  The `Type` property specifies the type name of the language provider, including the name of the assembly that contains the provider implementation.|  
|`WarningLevel`|A read/write `sint32` value that specifies the compiler warning level. **Note:**  The compiler warning level determines the level at which the language provider treats compilation warnings as errors.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Compilers` array property of the [CompilerSettings](../../reference/admin/compilersettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `CompilerElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [CompilerSettings Class](../../reference/admin/compilersettings-class.md)