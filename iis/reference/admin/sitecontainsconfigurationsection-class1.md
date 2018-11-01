---
title: "SiteContainsConfigurationSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 41e78754-a0bb-4800-aaad-4c6ed9392d4d
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# SiteContainsConfigurationSection Class1
Provides a relationship between a Web site and its configuration sections.  
  
## Syntax  
  
```vbs  
class SiteContainsConfigurationSection : ObjectConfigurationAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties for the `SiteContainsConfigurationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|A read-only [Site](../../reference/admin/site-class1.md) object that represents an IIS Web site.|  
|`Element`|A read-only [ConfigurationSection](../../reference/admin/configurationsection-class1.md) object that exposes the configuration section for a Web site.|  
  
## Subclasses  
 This class has no subclasses.  
  
## Remarks  
 Associations return only instances of the object that are defined at the level of the object. For example, if the `<authentication>` section is the only section defined in the Web.config file at the site level, only the [AuthenticationSection](../../reference/admin/authenticationsection-class1.md) instance of the `ConfigurationSection` object will be returned.  
  
 To get all available sections, you should use the [GetAllSections](../../reference/admin/configuredobject-getallsections-method1.md) method of the [ConfiguredObject](../../reference/admin/configuredobject-class1.md) class.  
  
## Example  
 The following example lists all configuration sections that are defined at the Web.config level for the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' List the configuration sections present in the Web.config file  
' of the default Web site.  
Set oSections = oSite.Associators_("SiteContainsConfigurationSection")  
For Each oSection In oSections  
    WScript.Echo oSection.Path_.Class  
Next  
```  
  
## Inheritance Hierarchy  
 [ObjectConfigurationAssociation](../../reference/admin/objectconfigurationassociation-class.md)  
  
 `SiteContainsConfigurationSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfiguredObject.GetAllSections Method](../../reference/admin/configuredobject-getallsections-method1.md)   
 [ObjectConfigurationAssociation Class](../../reference/admin/objectconfigurationassociation-class.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [VirtualDirectoryContainsConfigurationSection Class](../../reference/admin/virtualdirectorycontainsconfigurationsection-class2.md)