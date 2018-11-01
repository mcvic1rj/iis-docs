---
title: "ConfigurationSection.GetAllowLocation Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f0488c2d-152c-4b55-a96a-f43b33ee34e1
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSection.GetAllowLocation Method
Retrieves the `allowLocation` attribute for a configuration section.  
  
## Syntax  
  
```vbs  
ConfigurationSection.GetAllowLocation AllowLocation  
```  
  
```jscript#  
ConfigurationSection.GetAllowLocation(AllowLocation);  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`AllowLocation`|A `string` variable that receives the `allowLocation` attribute that the `GetAllowLocation` method returns. The possible attribute values are "true" or "false". The default is "true". **Note:**  This parameter is a `string`, not a `boolean`.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 The `allowLocation` attribute specifies whether a configuration section can appear inside a pair of location tags.  
  
 Because `GetAllowLocation` is a static method, you should call it by getting a class object, as in the following example.  
  
```  
' Correct syntax:  
Set oAnonAuth = oWebAdmin.Get("AnonymousAuthenticationSection")  
oAnonAuth.GetAllowLocation strAnonAuthAllowLocation  
```  
  
 The following syntax fails because it tries to call `GetAllowLocation` on a concrete instance of the `Site` class. The call to the method will cause an "SWbemObjectEx: Not found" error.  
  
```  
  
' Incorrect syntax:  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "AnonymousAuthenticationSection", oAnonAuth  
oAnonAuth.GetAllowLocation strAnonAuthAllowLocation  
```  
  
## Example  
 The following example displays the `allowLocation` attribute for the Anonymous authentication configuration section.  
  
```  
' Get the WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the AnonymousAuthenticationSection.  
Set oAnonAuth = oWebAdmin.Get( _  
    "AnonymousAuthenticationSection")  
  
' Get the allowLocation attribute.  
oAnonAuth.GetAllowLocation strAnonAuthAllowLocation  
  
' Display the allowLocation attribute.  
WScript.Echo _  
    "Anonymous Authentication Allow Location: " & _  
        strAnonAuthAllowLocation  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AnonymousAuthenticationSection Class](../../reference/admin/anonymousauthenticationsection-class1.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [ConfigurationSection.GetAllowDefinition Method](../../reference/admin/configurationsection-getallowdefinition-method.md)