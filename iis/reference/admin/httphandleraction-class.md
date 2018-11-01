---
title: "HttpHandlerAction Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: db796fc2-75a0-88d1-9944-4e260581de09
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# HttpHandlerAction Class
Represents an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] HTTP handler.  
  
## Syntax  
  
```vbs  
class HttpHandlerAction : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `HttpHandlerAction` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Path`|A read-only `string` value that contains the path of a single URL or a wildcard string. A key property.|  
|`Type`|A read/write `string` value that specifies a managed type for an HTTP handler. [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] searches for the handler assembly DLL in the application's private \Bin directory first and then in the system assembly cache. **Note:**  The type reference is formed as follows (items in brackets are not required): *Namespace*.*Typename*, *Assemblyname*[,] [Version=*x*,] [Culture=*y*,] [PublicKeyToken=*z*] (for example, "ExampleNamespace.ExampleType, Example.Assembly, Version=%ASSEMBLY_VERSION%, Culture=neutral, PublicKeyToken=%MICROSOFT_PUBLICKEY%").|  
|`Validate`|A read/write `boolean` value. `true` if [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] waits to load the handler class until a matching request arrives; otherwise `false`. The default is `true`.|  
|`Verb`|A read-only `string` value that specifies a comma-delimited list of HTTP verbs (for example, "GET, PUT, POST"). A wildcard ("*") represents all verbs. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `HttpHandlers` property of the [HttpHandlersSection](../../reference/admin/httphandlerssection-class.md) class.  
  
 The HTTP handlers represented by the `HttpHandlerAction` class are specific to [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and are in the `<system.web>` section of the Web.config file. These handlers are contained in the [HttpHandlersSection](../../reference/admin/httphandlerssection-class.md) class.  
  
 The HTTP handlers represented by the [HandlerAction](../../reference/admin/handleraction-class.md) class are related to [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] and are in the `<system.webServer>` section of the ApplicationHost.config file. These handlers are contained in the [HandlersSection](../../reference/admin/handlerssection-class.md) class.  
  
## Example  
 The following example displays the `HttpHandlerAction` instances that are contained in the `HttpHandlers` property of the `HttpHandersSection` object.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the HttpHandlersSection.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "HttpHandlersSection", oSection  
  
' Display the HttpHandlerAction instances contained in the  
' HttpHandlers property of HttpHandlersSection.  
For Each oHttpHandler In oSection.HttpHandlers  
     Counter = Counter + 1  
     WScript.Echo "[" & Counter & "] Path: " & oHttpHandler.Path  
     WScript.Echo "Type: " & oHttpHandler.Type  
     WScript.Echo "Validate: " & oHttpHandler.Validate  
     WScript.Echo "Verb: " & oHttpHandler.Verb  
     WScript.Echo  
Next  
  
```  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `HttpHandlerAction`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [HandlerAction Class](../../reference/admin/handleraction-class.md)   
 [HandlersSection Class](../../reference/admin/handlerssection-class.md)   
 [HttpHandlersSection Class](../../reference/admin/httphandlerssection-class.md)