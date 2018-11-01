---
title: "SiteContainsApplication Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bb56f880-ee3d-06b3-467c-d4f58a7c80cd
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# SiteContainsApplication Class1
Provides a relationship between a Web site and its applications.  
  
## Syntax  
  
```vbs  
class SiteContainsApplication : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SiteContainsApplication` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [Site](../../reference/admin/site-class1.md) object that represents an IIS Web site. A key property.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [Application](../../reference/admin/application-class1.md) object that represents an IIS application. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 To implement this association, use the configuration API to enumerate the applications for a given site.  
  
## Example  
 The following example shows how to use the `SiteContainsApplication` class to retrieve all the applications in a Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Use the SiteContainsApplication class to return the set of  
' application instances in the 'Default Web Site' Web site.  
Set oApps = oSite.Associators_("SiteContainsApplication")  
For Each oApp In oApps  
    WScript.Echo oApp.Path   
Next  
```  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `SiteContainsApplication`  
  
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
 [Site Class](../../reference/admin/site-class1.md)