---
title: "ApplicationPool.RevertToParent Method1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 919397d4-8c16-4d0b-83d7-b4be7052e3c9
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# ApplicationPool.RevertToParent Method1
Reverts an application pool's configuration value or values to the default.  
  
## Syntax  
  
```vbs  
ApplicationPool.RevertToParent(PropertyName)  
```  
  
```jscript#  
ApplicationPool.RevertToParent(PropertyName);  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`PropertyName`|An optional `string` value that contains the name of the application pool property that is to be reverted to the default specified by [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md). The property can be nested.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 When you call `RevertToParent` without parameters, all custom configuration values for the application pool will be removed. If this is not the behavior you want, revert specific properties by using separate parameterized calls to the method.  
  
## Example  
 The following example reverts the `AutoStart` property of the `ContosoAppPool` from its current value of `false` to the default value of `true`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject( _  
    "winmgmts:root\WebAdministration")  
  
' Get the application pools.  
Set oAppPools = oWebAdmin.InstancesOf("ApplicationPool")  
  
' Display the ContosoAppPool AutoStart property.  
For Each oAppPool In oAppPools  
    If oAppPool.Name = "ContosoAppPool" Then  
        WScript.Echo "Application pool name: " & oAppPool.Name  
        WScript.Echo "AutoStart mode before revert: " & _  
            oAppPool.AutoStart  
  
        ' Revert the AutoStart property.  
        oAppPool.RevertToParent("AutoStart")  
  
        ' Refresh the oAppPool object variable.  
        oAppPool.Refresh_  
  
        ' Display the changed property.  
        WScript.Echo "AutoStart mode after revert: " & _  
                oAppPool.AutoStart  
  
        Exit For  
    End If  
Next  
  
' Output:  
' Application pool name: ContosoAppPool  
' AutoStart mode before revert: False  
' AutoStart mode after revert: True  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md)