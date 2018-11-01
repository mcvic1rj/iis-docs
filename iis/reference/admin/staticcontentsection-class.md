---
title: "StaticContentSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0f53f631-c9e7-5eb6-5bc0-8516079ac610
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# StaticContentSection Class
Exposes configuration settings for static content on a Web site.  
  
## Syntax  
  
```vbs  
class StaticContentSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `StaticContentSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|(Inherited from [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md).)|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `StaticContentSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ClientCache`|A read/write [HttpClientCache](../../reference/admin/httpclientcache-class.md) value that exposes the client caching configuration.|  
|`DefaultDocFooter`|A read/write `string` value that contains either the default footer text for every Web page on a site, or the path to a file that contains the default footer text. How this property is read depends on the setting of the `IsDocFooterFileName` property. The default is `null`.|  
|`EnableDocFooter`|A read/write `boolean` value. `true` if the text indicated by `DefaultDocFooter` will appear on every static page on a Web site; otherwise, `false`. The default is `false`.|  
|`IsDocFooterFileName`|A read/write `boolean` value. `true` if the string in `DefaultDocFooter` contains a path to a file that contains the default footer text for every static Web page on a site; otherwise, `false`. The default is `false`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`StaticContent`|An array of read/write [MimeMapElement](../../reference/admin/mimemapelement-class.md) objects that contain the MIME maps for static content.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The properties in this class correspond to the attributes and elements in the `<staticContent>` section of the ApplicationHost.config file.  
  
## Example  
 The following example shows the footer-text and client-cache properties of the `StaticContentSection` class.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the static content section.  
Set oSection = oWebAdmin.Get("StaticContentSection.Path=" & _  
    "'MACHINE/WEBROOT/APPHOST',Location=''")  
' Show the path and location.  
WScript.Echo "Path: " & oSection.Path  
WScript.Echo "Location: " & oSection.Location  
WScript.Echo  
  
'Show the doc-footer-related properties.  
WScript.Echo "Doc Footer properties"  
WScript.Echo "---------------------"  
WScript.Echo "EnableDocFooter: " & oSection.EnableDocFooter  
WScript.Echo "IsDocFooterFileName: " & oSection.IsDocFooterFileName  
WScript.Echo "DefaultDocFooter: " & oSection.DefaultDocFooter  
WScript.Echo  
  
' Show the embedded client-cache properties.  
Set oClientCache = oSection.ClientCache  
WScript.Echo "ClientCache properties"  
WScript.Echo "----------------------"  
WScript.Echo "CacheControlCustom: " & _  
    oClientCache.CacheControlCustom  
WScript.Echo "CacheControlMaxAge: " & _  
    oClientCache.CacheControlMaxAge  
WScript.Echo "CacheControlMode: " & _  
    oClientCache.CacheControlMode  
WScript.Echo "HttpExpires: " & _  
    oClientCache.HttpExpires  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `StaticContentSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [HttpClientCache Class](../../reference/admin/httpclientcache-class.md)   
 [MimeMapElement Class](../../reference/admin/mimemapelement-class.md)