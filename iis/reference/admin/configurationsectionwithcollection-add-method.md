---
title: "ConfigurationSectionWithCollection.Add Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ba05cc65-3f0e-35d5-f8a0-b4e3f82dc96e
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSectionWithCollection.Add Method
Adds an element to a collection in a configuration section.  
  
## Syntax  
  
```jscript#  
ConfigurationSectionWithCollection.Add collectionName, element;  
```  
  
```vbs  
ConfigurationSectionWithCollection.Add collectionName, element  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`collectionName`|A `string` value that contains the name of the collection that will be added to.|  
|`element`|A [CollectionElement](../../reference/admin/collectionelement-class.md) object to which the element will be added.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 When you use the `Add` method, the changes you make are saved automatically. You do not need to use the `Put_` method.  
  
## Example  
 The following example adds a MIME map to the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Get the static content section by using the GetSection method.  
oSite.GetSection "StaticContentSection", oStaticContentSection  
  
' Get the MimeMapElement class object.  
Set oMimeMapElement = oWebAdmin.Get("MimeMapElement")  
  
' Spawn a new instance of the MimeMapElement class.  
Set oNewMimeMap = oMimeMapElement.SpawnInstance_  
  
' Assign values to the FileExtension and MimeType properties.  
oNewMimeMap.FileExtension = "MyFileExtension"  
oNewMimeMap.MimeType = "application/MyApp"  
  
' Add the MIME map to the collection.  
oStaticContentSection.Add "StaticContent", oNewMimeMap  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [MimeMapElement Class](../../reference/admin/mimemapelement-class.md)