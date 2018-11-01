---
title: "Application.RevertToParent Method1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 18b70a15-3c52-44be-a411-7b2b89216936
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# Application.RevertToParent Method1
Reverts an application's configuration value or values to the default.  
  
## Syntax  
  
```vbs  
Application.RevertToParent(PropertyName)  
```  
  
```jscript#  
Application.RevertToParent(PropertyName);  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`PropertyName`|An optional `string` value that contains the name of the application property that is to be reverted to the default specified by the [ApplicationElementDefaults](../../reference/admin/applicationelementdefaults-class2.md) class that is exposed as the `ApplicationDefaults` property on the parent [Site](../../reference/admin/site-class1.md) class. The property to revert can be nested (for example, "VirtualDirectoryDefaults.PhysicalPath").|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 When you call `RevertToParent` without parameters, all settings for the application that are in the ApplicationHost.config file will be removed. If this is not the behavior you want, revert specific properties by using separate parameterized calls to the method.  
  
## Example  
 The following example reverts the name of the default Web site's `MyApp` application pool from "MyAppPool" to "DefaultAppPool".  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Retrieve the MyApp application from the default Web site.  
Set oApp = oWebAdmin.Get( _  
    "Application.SiteName='Default Web Site',Path='/MyApp'")  
  
' Display the site name, path, and application pool.  
WScript.Echo "Web site name: " & oApp.SiteName  
WScript.Echo "Application path: " & oApp.Path      
Wscript.Echo "ApplicationPool: " & oApp.ApplicationPool  
  
' Revert the MyApp application pool to the application pool  
' specified by the parent site's ApplicationDefaults property.  
oApp.RevertToParent("ApplicationPool")  
  
' Update the contents of the application object variable.  
oApp.Refresh_  
  
' Display the change.  
Wscript.Echo "ApplicationPool after revert: " & _  
    oApp.ApplicationPool  
  
' Example output:  
' Web site name: Default Web Site  
' Application path: /MyApp  
' ApplicationPool: MyAppPool  
' ApplicationPool after revert: DefaultAppPool  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [ApplicationElementDefaults Class](../../reference/admin/applicationelementdefaults-class2.md)   
 [Site Class](../../reference/admin/site-class1.md)