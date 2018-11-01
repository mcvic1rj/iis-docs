---
title: "HttpHandlersSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6172d775-56fd-b3a6-ef47-803f372aeebd
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# HttpHandlersSection Class
Configures settings for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] handlers.  
  
## Syntax  
  
```vbs  
class HttpHandlersSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `HttpHandlersSection` class.  
  
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
 The following table lists the properties exposed by the `HttpHandlersSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`HttpHandlers`|An array of [HttpHandlerAction](../../reference/admin/httphandleraction-class.md) values that contain [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] handlers.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The HTTP handlers contained in the `HttpHandlersSection` class are specific to [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and are in the `<system.web>` section of the Web.config file. Each of these handlers is represented by an instance of the `HttpHandlerAction` class.  
  
 The HTTP handlers in the [HandlersSection](../../reference/admin/handlerssection-class.md) class are related to [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] and are in the `<system.webServer>` section of the ApplicationHost.config file. Each of these handlers is represented by an instance of the [HandlerAction](../../reference/admin/handleraction-class.md) class.  
  
## Example  
 The following example displays `HttpHandlersSection` properties, including the `HttpHandlerAction` values that are in the `HttpHandlers` property.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the HttpHandlersSection.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "HttpHandlersSection", oSection  
  
' Display the Path and Location properties.  
WScript.Echo "Path: " & oSection.Path  
WScript.Echo "Location: " & oSection.Location  
WScript.Echo   
  
' Display the HttpHandlerAction instances that are contained  
' in the HttpHandlers property.  
WScript.Echo "----------( Http Handlers )----------"  
Counter = 0  
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
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `HttpHandlersSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [HandlerAction Class](../../reference/admin/handleraction-class.md)   
 [HandlersSection Class](../../reference/admin/handlerssection-class.md)   
 [HttpHandlerAction Class](../../reference/admin/httphandleraction-class.md)