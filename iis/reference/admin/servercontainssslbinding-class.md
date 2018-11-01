---
title: "ServerContainsSSLBinding Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ef6ae9a0-9134-c320-1380-93cd00297da0
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# ServerContainsSSLBinding Class
Provides a relationship between a Secure Sockets Layer (SSL) binding and a Web server that is running IIS.  
  
## Syntax  
  
```vbs  
class ServerContainsSSLBinding : ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ServerContainsSSLBinding` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|(Inherited from [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md).) A read-only [Server](../../reference/admin/server-class1.md) object that represents a Web server running IIS.|  
|`Element`|(Inherited from `ObjectContainerAssociation`.) A read-only [SSLBinding](../../reference/admin/sslbinding-class.md) object that represents an SSL binding.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class is used to enumerate the SSL bindings that IIS uses on a Web server.  
  
## Inheritance Hierarchy  
 [ObjectContainerAssociation](../../reference/admin/objectcontainerassociation-class1.md)  
  
 `ServerContainsSSLBinding`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)   
 [SiteUsesSSLBinding Class](../../reference/admin/siteusessslbinding-class1.md)   
 [SSLBinding Class](../../reference/admin/sslbinding-class.md)