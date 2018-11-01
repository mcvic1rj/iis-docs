---
title: "ConfiguredObject.GetAllSections Method1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4c7fc67c-c762-1cc8-b9b4-6cb0a099dc57
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# ConfiguredObject.GetAllSections Method1
Retrieves all configuration sections under a configured object.  
  
## Syntax  
  
```jscript#  
ConfiguredObject.GetAllSections(Sections);  
```  
  
```vbs  
ConfiguredObject.GetAllSections Sections  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`Sections`|A [ConfigurationSection](../../reference/admin/configurationsection-class1.md) variable into which the configuration sections for the configured object are copied.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 The `GetAllSections` method is useful for discovering the full set of available sections for a configured object. For regular setting and getting of configuration properties, see the [ConfiguredObject.GetSection](../../reference/admin/configuredobject-getsection-method.md) method.  
  
> [!NOTE]
>  The `GetAllSections` method signature contains an `[OUT]` parameter that receives the sections that the method returns.  
  
## Example  
 The following example retrieves the [Site](../../reference/admin/site-class1.md) object for the default Web site and uses the `GetAllSections` method to retrieve and enumerate the configuration section objects for the site.  
  
 Only one instance of each section is returned. The returned values are the effective configuration for the level of the [ConfiguredObject](../../reference/admin/configuredobject-class1.md) that is being used. The path for all returned objects will match that of the `ConfiguredObject`.  
  
> [!NOTE]
>  Only the objects at the level of the `ConfiguredObject` that you specify will be returned.  
  
```  
' Connect to the WMI WebAministration namespace.  
Set oWebAdmin = _  
    GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Retrieve all configuration sections for the default Web  
' site and place them into an array variable.  
oSite.GetAllSections arySect  
  
' Display the number of configuration sections.  
WScript.Echo "There are " & UBound(arySect) + 1 & _  
    " configuration sections for [" & oSite.Name & "]."  
WScript.Echo vbCrLf  
  
' Iterate through the sections.  
For aryIdx = 0 To UBound(arySect)  
  
    ' Number the section for display.  
    WScript.Echo aryIdx + 1 & "."  
  
    ' Show the section name.  
    WScript.Echo "[" & arySect(aryIdx).Path_.Class & "]"  
  
    ' Show the section path and location.  
    WScript.Echo "Path: " & arySect(aryIdx).Path  
    WScript.Echo "Location: " & arySect(aryIdx).Location  
  
    ' Show the SectionInformation properties.  
    WScript.Echo "SectionInformation.OverrideMode: " & _  
        arySect(aryIdx).SectionInformation.OverrideMode  
    WScript.Echo _  
        "SectionInformation.EffectiveOverrideMode: " & _  
        arySect(aryIdx).SectionInformation.EffectiveOverrideMode  
    WScript.Echo "SectionInformation.IsLocked: " & _  
        arySect(aryIdx).SectionInformation.IsLocked  
    WScript.Echo "SectionInformation.LockItem: " & _  
        arySect(aryIdx).SectionInformation.LockItem  
  
    WScript.Echo vbCrLf  
Next  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfiguredObject Class](../../reference/admin/configuredobject-class1.md)   
 [ConfiguredObject.GetSection Method](../../reference/admin/configuredobject-getsection-method.md)