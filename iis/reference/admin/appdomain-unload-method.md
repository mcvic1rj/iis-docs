---
title: "AppDomain.Unload Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 79c8dac8-62d9-2d41-6948-19907d73dad5
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# AppDomain.Unload Method
Unloads an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application domain from a Web server.  
  
## Syntax  
  
```vbs  
oAppDomain.Unload  
```  
  
```jscript#  
oAppDomain.Unload();  
```  
  
#### Parameters  
 This method takes no parameters.  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 The IIS 6.0 `AppUnload` command unloaded out-of-process ASP applications. The [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] `AppDomain.Unload` method unloads [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application domains. This method applies only to managed code. [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] has no method that corresponds to `AppUnload` because the IIS 5.0 compatibility mode that `AppUnload` supported is now deprecated.  
  
## Example  
 The following example demonstrates how to unload an application domain. The first section of the example unloads all application domains on a Web server. The second section unloads only the application domain named "Northwind".  
  
```  
' ---- Unload all application domains. ----  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get all of the application domains on the Web server.  
Set oAppDomains = oWebAdmin.ExecQuery("SELECT * FROM AppDomain")  
  
' Unload all of the application domains.  
  
For Each oAppDomain In oAppDomains  
    oAppDomain.Unload  
Next  
  
' ---- Unload only the Northwind application domain. ----  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get all of the application domains on the Web server.  
Set oAppDomains = oWebAdmin.ExecQuery("SELECT * FROM AppDomain")  
  
' Unload the Northwind application domain.  
For Each oAppDomain In oAppDomains  
    If oAppDomain.ApplicationPath = "/Northwind/" Then  
        oAppDomain.Unload  
    End If  
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
 [AppDomain Class](../../reference/admin/appdomain-class.md)