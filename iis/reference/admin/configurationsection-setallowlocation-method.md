---
title: "ConfigurationSection.SetAllowLocation Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ef360cdc-bd3f-4731-8e6c-87d0219903b2
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSection.SetAllowLocation Method
Sets the `allowLocation` attribute for a configuration section.  
  
## Syntax  
  
```vbs  
ConfigurationSection.SetAllowLocation(AllowLocation)  
```  
  
```jscript#  
ConfigurationSection.SetAllowLocation(AllowLocation);  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`AllowLocation`|A case-sensitive `string` variable that sets the `allowLocation` attribute for the configuration section. The possible attribute values are "true" or "false". The default is "true". **Note:**  This parameter is a `string`, not a `boolean`.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 The `allowLocation` attribute specifies whether a configuration section can appear inside a pair of location tags.  
  
 Because `SetAllowLocation` is a static method, you should call it by getting a class object, as in the following example.  
  
```  
' Correct syntax:  
Set oAnonAuth = oWebAdmin.Get("AnonymousAuthenticationSection")  
oAnonAuth.SetAllowLocation "false"  
```  
  
 The following syntax fails because it tries to call `SetAllowLocation` on a concrete instance of the `Site` class. The call to the method will cause an "SWbemObjectEx: Not found" error.  
  
```  
  
' Incorrect syntax:  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "AnonymousAuthenticationSection", oAnonAuth  
oAnonAuth.SetAllowLocation "false"  
```  
  
## Example  
 The following example sets the `allowLocation` attribute for the Anonymous authentication configuration section.  
  
```  
' Get the WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the AnonymousAuthenticationSection.  
Set oAnonAuth = oWebAdmin.Get( _  
    "AnonymousAuthenticationSection")  
  
' Set the allowLocation attribute.  
oAnonAuth.GetAllowLocation "false"  
  
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
 [ConfigurationSection.GetAllowLocation Method](../../reference/admin/configurationsection-getallowlocation-method.md)