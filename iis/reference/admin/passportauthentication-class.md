---
title: "PassportAuthentication Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 499ec9c2-244d-83e0-88a5-3003ef7114bd
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# PassportAuthentication Class
Configures Microsoft Passport Network authentication in [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications.  
  
## Syntax  
  
```vbs  
class PassportAuthentication : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `PassportAuthentication` class.  
  
|Name|Description|  
|----------|-----------------|  
|`RedirectUrl`|A read/write `string` value that specifies the URL of the page to which the request must be redirected if Passport Network authentication is required and the user has not signed on by using Passport Network credentials. The default is "internal".|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Passport` property of the [AuthenticationSection](../../reference/admin/authenticationsection-class1.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `PassportAuthentication`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AnonymousAuthenticationSection Class](../../reference/admin/anonymousauthenticationsection-class1.md)   
 [AuthenticationSection Class](../../reference/admin/authenticationsection-class1.md)   
 [BasicAuthenticationSection Class](../../reference/admin/basicauthenticationsection-class.md)   
 [ClientCertificateMappingAuthenticationSection Class](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)   
 [DigestAuthenticationSection Class](../../reference/admin/digestauthenticationsection-class.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [FormsAuthenticationConfiguration Class](../../reference/admin/formsauthenticationconfiguration-class.md)   
 [FormsAuthenticationCredentials Class](../../reference/admin/formsauthenticationcredentials-class.md)   
 [FormsAuthenticationUser Class](../../reference/admin/formsauthenticationuser-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [WindowsAuthenticationSection Class](../../reference/admin/windowsauthenticationsection-class.md)