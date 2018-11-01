---
title: "ApplicationContainsVirtualDirectory Class2 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f0d66fa9-7661-4f48-99e1-c14e72d3c045
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# ApplicationContainsVirtualDirectory Class2
Provides a relationship between an IIS application and its virtual directories.  
  
## Syntax  
  
```vbs  
class ApplicationContainsVirtualDirectory : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationContainsVirtualDirectory` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [Application](../../reference/admin/application-class1.md) object that represents an IIS application. A key property.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [VirtualDirectory](../../reference/admin/virtualdirectory-class2.md) object that represents an IIS virtual directory. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This association enumerates the virtual directories for a given application.  
  
## Example  
 The following example lists the virtual directory paths and physical paths for the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the application for the default Web site.  
Set oApp = oWebAdmin.Get("Application.SiteName='Default Web Site',Path='/'")  
  
' Return the set of virtual directory instances in the application.  
Set oVDirs = oApp.Associators_("ApplicationContainsVirtualDirectory")  
  
' Print out the virtual directories and their physical paths.  
For Each oVDir In oVDirs  
    WScript.Echo "Virtual Path: " & oVDir.Path  
    WScript.Echo "PhysicalPath: " & oVDir.PhysicalPath  
    WScript.Echo  
Next  
```  
  
 Note the following syntax from the preceding code example.  
  
 `Set oVDirs = oApp.Associators_("ApplicationContainsVirtualDirectory")`  
  
 To simplify your code, you can instead use the following syntax, which enables you to use the association without having to remember its exact name.  
  
 `Set oVDirs = oApp.Associators_(, "VirtualDirectory")`  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `ApplicationContainsVirtualDirectory`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)   
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)