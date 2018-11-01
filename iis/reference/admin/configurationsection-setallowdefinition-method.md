---
title: "ConfigurationSection.SetAllowDefinition Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 20e44a9a-b022-4e7b-88e6-a32bca75946e
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSection.SetAllowDefinition Method
Sets the `allowDefinition` attribute for a configuration section.  
  
## Syntax  
  
```vbs  
ConfigurationSection.SetAllowDefinition(AllowDefinition)  
```  
  
```jscript#  
ConfigurationSection.SetAllowDefinition(AllowDefinition);  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`AllowDefinition`|A `string` variable that specifies the value to which the `allowDefinition` attribute will be set. The possible attribute values are listed later in the Remarks section.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 `allowDefinition` attributes specify where in the configuration hierarchy values may be set for a given configuration section. These attributes are specified in the `<configSections>` section of the ApplicationHost.config file.  
  
 Because `SetAllowDefinition` is a static method, you should call it by getting a class object, as in the following example.  
  
```  
' Correct syntax:  
Set oAnonAuth = oWebAdmin.Get("AnonymousAuthenticationSection")  
oAnonAuth.SetAllowDefinition "MachineOnly"  
```  
  
 The following syntax fails because it tries to call `SetAllowDefinition` on a concrete instance of the `Site` class. The call to the method will cause an "SWbemObjectEx: Not found" error.  
  
```  
' Incorrect syntax:  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "AnonymousAuthenticationSection", oAnonAuth  
oAnonAuth.SetAllowDefinition "MachineOnly"  
```  
  
 The following table lists the possible values for the `allowDefinition` attribute.  
  
|Keyword|Description|  
|-------------|-----------------|  
|`Everywhere`|The section can be set anywhere in the hierarchy.|  
|`MachineOnly`|The section can be set only in the Machine.config file. **Note:**  The default location for the Machine.config file is *%systemroot%* Microsoft.NET\Framework\\*\<version>*\config\\.|  
|`MachineToWebRoot`|The section can be set only in the Machine.config file or the root Web.config file. **Note:**  The default location for the root Web.config file is *%systemroot%* Microsoft.NET\Framework\\*\<version>*\config\\.|  
|`AppHostOnly`|The section can be set only in the ApplicationHost.config file.|  
|`MachineToApplication`|The section can be set only at the global level. For [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] sections, the global level is the root Web.config or Machine.config file; for IIS sections, it is the ApplicationHost.config file; and for applications, it is the Web.config file for the root application.|  
  
## Example  
 The following example sets the `allowDefinition` attribute for the Anonymous authentication configuration section.  
  
```  
' Get the WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the AnonymousAuthenticationSection.  
Set oAnonAuth = oWebAdmin.Get( _  
    "AnonymousAuthenticationSection")  
  
' Set the AllowDefinition attribute.  
oAnonAuth.SetAllowDefinition "MachineToApplication"  
  
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