---
title: "BypassElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5169123e-c88c-f1a4-750f-159bb0db613a
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# BypassElement Class
Contains address information for resources that bypass the Web proxy server.  
  
## Syntax  
  
```vbs  
class BypassElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `BypassElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Address`|A required unique read/write `string` value that contains a regular expression that defines a resource address or addresses that bypass the proxy server. Requests for the resource are sent instead directly to the server where the resource resides. The key property. **Note:**  For more information about regular expressions, see the [System.Text.RegularExpressions](http://go.microsoft.com/fwlink/?LinkId=73545) namespace.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `BypassList` array property of the [BypassListSettings](../../reference/admin/bypasslistsettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `BypassElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [BypassListSettings Class](../../reference/admin/bypasslistsettings-class.md)   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [DefaultProxySection Class](../../reference/admin/defaultproxysection-class.md)   
 [System.Net.BypassElement Class](http://go.microsoft.com/fwlink/?LinkID=70908)   
 [System.Net.Configuration.BypassElement.Address Property](http://go.microsoft.com/fwlink/?LinkId=70909)   
 [System.Text.RegularExpressions Namespace](http://go.microsoft.com/fwlink/?LinkId=73545)