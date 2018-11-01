---
title: "BindingElement Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 359250eb-6680-f075-7ccb-cebc4850903e
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# BindingElement Class1
Represents a binding element for a Web site.  
  
## Syntax  
  
```vbs  
class BindingElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `BindingElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`BindingInformation`|A nonempty read/write `string` value with three colon-delimited fields that specify binding information for a Web site. The first field is a specific IP address or an asterisk (an asterisk specifies all unassigned IP addresses). The second field is the port number; the default is 80. The third field is an optional host header.|  
|`Protocol`|A required unique nonempty read/write `string` value that specifies the protocol that the site binding uses. The default is "HTTP". The key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Bindings` array property of the [Site](../../reference/admin/site-class1.md) class.  
  
## Example  
 The following example retrieves the bindings for all of the sites on a Web server.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get all Web site instances.  
Set oSites = oWebAdmin.InstancesOf("Site")  
  
' Display the name of each site and its bindings.  
For Each oSite In oSites  
  
    WScript.Echo oSite.Name  
  
    For Each objItem in oSite.Bindings  
        Wscript.Echo "Binding Info: " & objItem.BindingInformation  
        Wscript.Echo "Protocol: " & objItem.Protocol  
    Next  
    WScript.Echo  
Next  
```  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `BindingElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [SSLBinding Class](../../reference/admin/sslbinding-class.md)   
 [Site Class](../../reference/admin/site-class1.md)