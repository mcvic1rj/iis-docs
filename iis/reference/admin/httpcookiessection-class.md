---
title: "HttpCookiesSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 77afdef8-8d29-579c-e5f9-3b199fc2596f
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# HttpCookiesSection Class
Configures properties for cookies used by a Web application.  
  
## Syntax  
  
```vbs  
class HttpCookiesSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `HttpCookiesSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `HttpCookiesSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Domain`|An optional read/write `string` value that sets the cookie domain name.|  
|`HttpOnlyCookies`|A read/write `boolean` value. `true` if output of the <xref:System.Web.Configuration.HttpCookiesSection.HttpOnlyCookies%2A?displayProperty=fullName> property in Internet Explorer 6 SP1 or later is enabled; otherwise, `false`. The default is `false`.<br /><br /> This property can help mitigate cross-site scripting threats that result in stolen cookies. When a cookie that has `HttpOnlyCookies` set to `true` is received by a compliant browser, it is inaccessible to client-side script. Support for this type of cookie was added in Internet Explorer 6 SP1. For more information about possible attacks and how `HttpOnlyCookies` can help mitigate them, see [Mitigating Cross-Site Scripting with HTTP-Only Cookies](http://go.microsoft.com/fwlink/?LinkId=41580).|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`RequireSSL`|An optional read/write `boolean` value. `true` if Secure Sockets Layer (SSL) communication is required; otherwise, `false`. The default is `false`. **Note:**  This setting is overridden by any other feature that exposes the `RequireSSL` property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `HttpCookiesSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [httpCookies Element (ASP.NET Settings Schema)](http://go.microsoft.com/fwlink/?LinkId=67197)   
 [System.Web.Configuration.HttpCookiesSection.HttpOnlyCookies Property](http://go.microsoft.com/fwlink/?LinkId=67198)