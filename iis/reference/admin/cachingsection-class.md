---
title: "CachingSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0353b00e-efaf-761b-2218-178cf807c834
caps.latest.revision: 25
author: "shirhatti"
manager: "wpickett"
---
# CachingSection Class
Configures output and kernel caching.  
  
## Syntax  
  
```vbs  
class CachingSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `CachingSection` class.  
  
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
 The following table lists the properties exposed by the `CachingSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Enabled`|A read/write `boolean` value. `true` if the output cache is enabled; otherwise, `false`. If the output cache is disabled, no response output caching or kernel caching will occur. The default is `true`.|  
|`EnableKernelCache`|A read/write `boolean` value. `true` if kernel caching is enabled; otherwise, `false`. The default is `true`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`MaxCacheSize`|A read/write `uint32` value that specifies the maximum size, in megabytes, of the output cache. The default is 0. A value of 0 means that the cache memory size is managed automatically. A size of `MaxValue` means that there is no limit on cache size. **Note:**  This setting is effective only at the level of the ApplicationHost.config file. If you set this property at a lower level, it will have no effect.|  
|`MaxResponseSize`|A read/write `uint32` value that specifies the maximum size, in bytes, of a response that can be stored in the output cache. The default is 262144 (256KB). A setting of 0 means no limit. **Note:**  This setting is effective only at the level of the ApplicationHost.config file. If you set this property at a lower level, it will have no effect.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Profiles`|A [CachingProfileSettings](../../reference/admin/cachingprofilesettings-class.md) value that configures caching for specific request extensions.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Example  
 The following example displays properties in the `CachingSection` object for the default Web site, including the `CachingProfileSettings` values in the `Profiles` array property. Two helper functions are provided to display text for the `Policy`, `KernelCachePolicy`, and `Location` enumerations.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the CachingSection for the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "CachingSection", oSection  
  
' Display the path and location.  
Wscript.Echo "Path: " & oSection.Path  
Wscript.Echo "Location: " & oSection.Location  
Wscript.Echo   
  
' Display other non-array CachingSection properties.  
WScript.Echo "Enabled: " & oSection.Enabled  
Wscript.Echo "EnableKernelCache: " & oSection.EnableKernelCache  
Wscript.Echo "MaxCacheSize: " & oSection.MaxCacheSize  
Wscript.Echo "MaxResponseSize: " & oSection.MaxResponseSize  
Wscript.Echo   
  
' Display the caching profiles from the Profiles property.  
For Each oCachingProfileElement In oSection.Profiles.Profiles  
    Wscript.Echo   
    WScript.Echo "[ " & oCachingProfileElement.Extension & _  
        " ] Caching Profile"  
    WScript.Echo "-----------------------------------"  
    WScript.Echo "Duration: " & oCachingProfileElement.Duration  
    WScript.Echo "KernelCachePolicy: " & _  
        CachePolicyText(oCachingProfileElement.KernelCachePolicy)  
    WScript.Echo "Location: " & _  
        LocationText(oCachingProfileElement.Location)  
    WScript.Echo "Policy: " & _  
        CachePolicyText(oCachingProfileElement.Policy)  
    WScript.Echo "VaryByHeaders: " & _  
        oCachingProfileElement.VaryByHeaders  
    WScript.Echo "VaryByQueryString: " & _  
        oCachingProfileElement.VaryByQueryString  
    WScript.Echo               
Next  
  
' Provide text for KernelCachePolicy and Policy enumeration values.  
Function CachePolicyText(enumval)  
Select Case enumval  
    Case 0  
        CachePolicyText="DontCache"  
    Case 1  
        CachePolicyText="CacheUntilChange"  
    Case 2  
        CachePolicyText="CacheForTimePeriod"  
    Case Else  
        CachePolicyText="Undefined enumeration value"  
End Select  
End Function  
  
' Provide text for Location enumeration values.  
Function LocationText(enumval)  
Select Case enumval  
    Case 0  
        LocationText="Any"  
    Case 1  
        LocationText="Client"  
    Case 2  
        GetLocationText="Downstream"  
    Case 3  
        LocationText="Server"  
    Case 4  
        LocationText="None"  
    Case 5  
        LocationText="ServerAndClient"  
    Case Else  
        LocationText="Undefined enumeration value"  
End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `CachingSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AspCache Class](../../reference/admin/aspcache-class.md)   
 [CachingProfileElement Class](../../reference/admin/cachingprofileelement-class.md)   
 [CachingProfileSettings Class](../../reference/admin/cachingprofilesettings-class.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [HttpClientCache Class](../../reference/admin/httpclientcache-class.md)