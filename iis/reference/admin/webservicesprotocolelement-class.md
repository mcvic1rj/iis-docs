---
title: "WebServicesProtocolElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a9d8a894-5643-050e-f028-3af31e0202a3
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# WebServicesProtocolElement Class
Specifies a transmission protocol or protocols that are used to decrypt data sent from a client browser in an HTTP request.  
  
## Syntax  
  
```vbs  
class WebServicesProtocolElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `WebServicesProtocolElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Name`|A read-only `sint32` mask that specifies the transmission protocols that are used to decrypt data sent from a client browser in the HTTP request. The possible values are listed later in the Remarks section. The key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are exposed as members of the `Protocols` property in the [WebServicesProtocolSettings](../../reference/admin/webservicesprotocolsettings-class.md) class.  
  
 The following table lists the possible values for the `Name` property.  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Unknown`|An unknown protocol.|  
|1|`HttpSoap`|The HTTP SOAP protocol.|  
|2|`HttpGet`|The HTTP GET protocol.|  
|4|`HttpPost`|The HTTP POST protocol.|  
|8|`Documentation`|The XML Web services Documentation protocol.|  
|16|`HttpPostLocalhost`|The HTTP POST LOCALHOST protocol. **Note:**  This value checks only the request's host header to mitigate browser-redirect attacks. This value does not perform any other validation, authentication, or authorization checks. Authentication and authorization are still required to restrict access to a Web service.|  
|32|`HttpSoap12`|The HTTP SOAP version 1.2 protocol.|  
|33|`AnyHttpSoap`|Any version of the HTTP SOAP protocol.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `WebServicesProtocolElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [WebServicesProtocolSettings Class](../../reference/admin/webservicesprotocolsettings-class.md)   
 [WebServicesSection Class](../../reference/admin/webservicessection-class.md)   
 [System.Web.Services.Configuration.WebServiceProtocols Enumeration](http://go.microsoft.com/fwlink/?LinkId=69314)