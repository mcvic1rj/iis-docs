---
title: "BuildProvider Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 86c97635-9cea-7ced-e217-276667534258
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# BuildProvider Class
Represents a build provider that compiles custom resource files of a particular file type and generates code during compilation.  
  
## Syntax  
  
```vbs  
class BuildProvider : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `BuildProvider` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Extension`|A read-only `string` value that specifies a resource file extension (such as ".aspx" or ".ascx") that is compiled by the build provider specified in the `Type` property. The key property.|  
|`Type`|A read/write `string` value that contains the type of the build provider that compiles resource files that have the file extension specified in the `Extension` property. The string is a comma-delimited list that contains the fully qualified type name followed by the assembly information (for example, Corp.Net.Provider, Corp, Version=1.0.5000.0, Culture=neutral, PublicKeyToken="00000000000000000"). If you do not specify a string value, the property will contain a null reference.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `BuildProviders` array property of the [BuildProviderSettings](../../reference/admin/buildprovidersettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `BuildProvider`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.CompilationSection.BuildProviders%2A?displayProperty=fullName>   
 [BuildProviderSettings Class](../../reference/admin/buildprovidersettings-class.md)   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [CompilationSection Class](../../reference/admin/compilationsection-class.md)