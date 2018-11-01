---
title: "ApplicationPoolContainsApplication Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7d574944-1324-9e06-bd93-c1c69280cc53
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# ApplicationPoolContainsApplication Class1
Provides a relationship between an application pool and its applications.  
  
## Syntax  
  
```vbs  
class ApplicationPoolContainsApplication : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties for the `ApplicationPoolContainsApplication` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [ApplicationPool](../../reference/admin/applicationpool-class1.md) object that represents an IIS application pool. A key property.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [Application](../../reference/admin/application-class1.md) object that represents an IIS application. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 To implement this association, use the configuration API to enumerate the applications in an application pool.  
  
## Example  
 The following example shows how to use the `ApplicationPoolContainsApplication` class to retrieve all the applications in an application pool.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the application pool.  
Set oAppPool = oWebAdmin.Get("ApplicationPool.Name='DefaultAppPool'")  
  
' Use the ApplicationPoolContainsApplication class to return the set of  
' application instances in the 'DefaultAppPool' application pool.  
Set oApps = oAppPool.Associators_("ApplicationPoolContainsApplication")  
For Each oApp In oApps  
    WScript.Echo oApp.Path   
Next  
```  
  
 Note the following syntax from the preceding code example.  
  
 `Set oApps = oAppPool.Associators_("ApplicationPoolContainsApplication")`  
  
 To simplify your code, you can instead use the following syntax, which enables you to use the association without having to remember its exact name.  
  
 `Set oApps = oAppPool.Associators_(, "Application")`  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `ApplicationPoolContainsApplication`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)