---
title: "VirtualDirectory.RevertToParent Method2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4cae86e8-cbbf-4e0b-a0aa-f32d32412e25
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# VirtualDirectory.RevertToParent Method2
Reverts a virtual directory's configuration value or values to the default.  
  
## Syntax  
  
```vbs  
VirtualDirectory.RevertToParent(PropertyName)  
```  
  
```jscript#  
VirtualDirectory.RevertToParent(PropertyName);  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`PropertyName`|An optional `string` value that contains the name of a virtual directory property to revert to the default specified by the [VirtualDirectoryElementDefaults](../../reference/admin/virtualdirectoryelementdefaults-class1.md) class that is exposed as the `VirtualDirectoryDefaults` property on the [Application](../../reference/admin/application-class1.md) class.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 When you call the `RevertToParent` method without parameters, all custom configuration values for the virtual directory will be removed. If this is not the behavior you want, revert specific properties by using parameterized calls to the method.  
  
## Example  
 The following example reverts the `AllowSubDirConfig` property of the `MyVDir` virtual directory from its current value of `false` to its default value of `true`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Assign the virtual directory instances to a variable.  
Set oVDirs = oWebAdmin.InstancesOf("VirtualDirectory")  
  
' Retrieve the MyVDir virtual directory.  
For Each oVDir In oVDirs  
    If oVDir.Path = "/MyVDir" Then  
  
        ' Display the virtual directory path.  
        WScript.Echo "Virtual Path: " & oVDir.Path  
  
        ' Display the current value.  
        WScript.Echo "AllowSubDirConfig before revert: " & _  
                oVDir.AllowSubDirConfig      
  
        ' Revert the AllowSubDirConfig property.  
        oVdir.RevertToParent("AllowSubDirConfig")  
  
        ' Refresh the oVdir object variable.  
        oVdir.Refresh_  
  
        ' Display the changed value.  
        WScript.Echo "AllowSubDirConfig after revert: " & _  
                oVDir.AllowSubDirConfig   
  
        ' Exit the loop.  
        Exit For   
    End If  
Next  
  
' Output:  
' Virtual Path: /MyVDir  
' AllowSubDirConfig before revert: False  
' AllowSubDirConfig after revert: True  
  
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
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)   
 [VirtualDirectoryElementDefaults Class](../../reference/admin/virtualdirectoryelementdefaults-class1.md)