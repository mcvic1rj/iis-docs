---
title: "FormsAuthenticationCredentials Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: da1e5777-c6cf-3de0-12cd-e02e1f24150a
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# FormsAuthenticationCredentials Class
Configures user credentials for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications that use Forms authentication.  
  
## Syntax  
  
```vbs  
class FormsAuthenticationCredentials : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `FormsAuthenticationCredentials` class.  
  
|Name|Description|  
|----------|-----------------|  
|`PasswordFormat`|A read/write `sint32` value that defines the encryption format for storing passwords. The possible values are listed later in the Remarks section.|  
|`Credentials`|An array of [FormsAuthenticationUser](../../reference/admin/formsauthenticationuser-class.md) values that specify user-name and password credentials.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Credentials` property of the [FormsAuthenticationConfiguration](../../reference/admin/formsauthenticationconfiguration-class.md) class.  
  
 The following table lists the possible values for the `PasswordFormat` property. The default is 1 (`SHA1`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Clear`|Specifies that passwords are not encrypted. This field is constant.|  
|1|`SHA1`|Specifies that passwords are encrypted by using the SHA1 hash algorithm. This field is constant.|  
|2|`MD5`|Specifies that passwords are encrypted by using the MD5 hash algorithm. This field is constant.|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `FormsAuthenticationCredentials`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.FormsAuthPasswordFormat?displayProperty=fullName>   
 [ClientCertificateMappingAuthenticationSection Class](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)   
 [DigestAuthenticationSection Class](../../reference/admin/digestauthenticationsection-class.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [FormsAuthenticationConfiguration Class](../../reference/admin/formsauthenticationconfiguration-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [PassportAuthentication Class](../../reference/admin/passportauthentication-class.md)