---
title: "Site.Stop Method1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3364b705-8777-3927-4016-d35a36d3c433
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# Site.Stop Method1
Stops a currently running Web site.  
  
## Syntax  
  
```vbs  
oSite.Stop  
```  
  
```jscript#  
oSite.Stop();  
```  
  
#### Parameters  
 This method takes no parameters.  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 This method is new to the [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] WMI provider and has no counterpart in IIS 6.0.  
  
## Example  
 The following example stops the Web site named `IISWebSite`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Specify the Web site name.  
Set oSite = oWebAdmin.Get("Site.Name='IISWebSite'")  
  
' Stop the Web site.  
oSite.Stop  
```  
  
 To check the state of the Web site after you call the `Stop` method, use the [GetState](../../reference/admin/site-getstate-method1.md) method.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Site Class](../../reference/admin/site-class1.md)   
 [Site.GetState Method](../../reference/admin/site-getstate-method1.md)   
 [Site.Start Method](../../reference/admin/site-start-method1.md)