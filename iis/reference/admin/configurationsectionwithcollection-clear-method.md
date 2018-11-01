---
title: "ConfigurationSectionWithCollection.Clear Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f37e0c33-fc7d-b3ce-32b4-e980b4ffff06
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSectionWithCollection.Clear Method
Clears all elements from a collection in a configuration section.  
  
## Syntax  
  
```jscript#  
ConfigurationSectionWithCollection.Clear(collectionName);  
```  
  
```vbs  
ConfigurationSectionWithCollection.Clear(collectionName)  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`collectionName`|A `string` value that contains the name of the collection to be removed.|  
  
## Return Value  
 This method does not return a value.  
  
## Example  
 The following example clears the default documents, including all inherited default documents, for the default Web site. The code will cause the following XML to be added to the `<system.webServer>` section of the Web.config file for the default Web site:  
  
 `<defaultDocument>`  
  
 `<files>`  
  
 `<clear />`  
  
 `</files>`  
  
 `</defaultDocument>`  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite= oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Get the default documents section.  
oSite.GetSection "DefaultDocumentSection", oDefaultDocumentSection  
  
' Clear the default documents that are listed in the  
' DefaultDocumentSection.Files.Files property.  
oDefaultDocumentSection.Clear("Files.Files")  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [DefaultDocumentSection Class](../../reference/admin/defaultdocumentsection-class1.md)   
 [FileSettings Class](../../reference/admin/filesettings-class1.md)