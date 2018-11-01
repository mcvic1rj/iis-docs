---
title: "IsapiCgiRestrictionSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c774177c-4c4b-8d8b-bfb4-b7b7cd985b65
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# IsapiCgiRestrictionSection Class
Configures ISAPI and Common Gateway Interface (CGI) restrictions for a Web server that runs in ISAPI mode.  
  
## Syntax  
  
```vbs  
class IsapiCgiRestrictionSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `IsapiCgiRestrictionSection` class.  
  
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
 The following table lists the properties exposed by the `IsapiCgiRestrictionSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`IsapiCgiRestriction`|An array of [IsapiCgiRestrictionElement](../../reference/admin/isapicgirestrictionelement-class.md) values that contain ISAPI or CGI restrictions.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`NotListedCgisAllowed`|A read/write `boolean` value. `true` if CGI restrictions that are not listed are allowed; otherwise, `false`. The default is `false`.|  
|`NotListedIsapisAllowed`|A read/write `boolean` value. `true` if ISAPI restrictions that are not listed are allowed; otherwise, `false`. The default is `false`.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 ISAPI and CGI restrictions are request handlers that allow dynamic content to execute on a server. These restrictions are either CGI files (.exe) or ISAPI extensions (.dll). The Asp.dll and Aspnet_isapi.dll files are included by default. You can add custom ISAPI or CGI restrictions if the IIS configuration permits.  
  
> [!NOTE]
>  If you are running [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] in ISAPI mode, you can use ISAPI or CGI restrictions on your Web server. This feature is not available if you are running [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] in integrated mode.  
  
## Example  
 The following example shows the values for the `NotListedCgisAllowed`, `NotListedIsapisAllowed`, and `Path` properties, and it lists the contents of the `IsapiCgiRestriction` array property.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Get the ISAPI-CGI restriction section.  
oSite.GetSection "IsapiCgiRestrictionSection", oSection  
  
' Display the non-array IsapiCgiRestrictionSection properties.  
WScript.Echo "ISAPI CGI Restriction Section"  
WScript.Echo "-----------------------------"  
WScript.Echo "Path: " & oSection.Path  
WScript.Echo "NotListedCgisAllowed: " & _  
    oSection.NotListedCgisAllowed  
WScript.Echo "NotListedIsapisAllowed: " & _  
    oSection.NotListedIsapisAllowed  
WScript.Echo   
  
' Display the contents of the IsapiCgiRestriction array property.  
WScript.Echo vbTab & "ISAPI CGI Restriction Elements"  
WScript.Echo vbtab & "------------------------------"  
For Each oIsapiCgiRestrictionElement In oSection.IsapiCgiRestriction  
    WScript.Echo  vbtab & "GroupID: " & _  
        oIsapiCgiRestrictionElement.GroupID  
    WScript.Echo  vbtab & "Description: " & _  
        oIsapiCgiRestrictionElement.Description  
    WScript.Echo  vbtab & "Path: " & _  
        oIsapiCgiRestrictionElement.Path  
    WScript.Echo  vbtab & "Allowed: " & _  
        oIsapiCgiRestrictionElement.Allowed  
    WScript.Echo  
Next  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `IsapiCgiRestrictionSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [IsapiCgiRestrictionElement Class](../../reference/admin/isapicgirestrictionelement-class.md)