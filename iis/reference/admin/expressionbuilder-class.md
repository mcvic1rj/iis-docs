---
title: "ExpressionBuilder Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d5626c9b-c688-06c7-df5d-abe450a477a5
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# ExpressionBuilder Class
Maps an expression prefix to an expression builder type.  
  
## Syntax  
  
```vbs  
class ExpressionBuilder : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ExpressionBuilder` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ExpressionPrefix`|A read-only `string` value that contains the prefix for the current expression builder object. The key property.|  
|`Type`|A read/write `string` value that contains a type associated with the prefix specified in the `ExpressionPrefix` property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `ExpressionBuilders` array property of the [ExpressionBuilderSettings](../../reference/admin/expressionbuildersettings-class.md) class.  
  
 Expression builders allow property values to be set and retrieved in a control during page parsing. When the page parser encounters an expression in the format `<%$ prefix:value %>`, it creates an expression builder based on `prefix` and passes the `value` to the expression builder for evaluation. The expression builder then returns the requested value to the page.  
  
 `ExpressionPrefix` values are associated with expression builders in the `<``expressionBuilders``>` section of a Web.config file, as the following example shows:  
  
 `<configuration>`  
  
 `<system.web>`  
  
 `<compilation>`  
  
 `<expressionBuilders>`  
  
 `<add expressionPrefix="TCO"`  
  
 `type="Contoso.Finance.TCOExpressionBuilder"/>`  
  
 `</expressionBuilders>`  
  
 `</compilation>`  
  
 `</system.web>`  
  
 `</configuration>`  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ExpressionBuilder`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Compilation.ExpressionPrefixAttribute?displayProperty=fullName>   
 <xref:System.Web.Configuration.CompilationSection.ExpressionBuilders%2A?displayProperty=fullName>   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [CompilationSection Class](../../reference/admin/compilationsection-class.md)   
 [ExpressionBuilderSettings Class](../../reference/admin/expressionbuildersettings-class.md)