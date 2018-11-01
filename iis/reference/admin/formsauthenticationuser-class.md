---
title: "FormsAuthenticationUser Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2f57cdd1-9ec2-dc0b-7332-47cbca2b8f46
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# FormsAuthenticationUser Class
Configures user credentials for Web applications that use Forms authentication.  
  
## Syntax  
  
```vbs  
class FormsAuthenticationUser : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `FormsAuthenticationUser` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Name`|A read-only `string` value that contains the logon user name that is required by the Web application. The key property.|  
|`Password`|A read/write `string` value that specifies the user password that is required by the Web application.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Credentials` property of the [FormsAuthenticationCredentials](../../reference/admin/formsauthenticationcredentials-class.md) class.  
  
 A `FormsAuthenticationUser` object can write information into the related section of the configuration file at computer, site, or application level only. Any attempt to write in a configuration file at a different level in the hierarchy will result in a parser-generated error message. However, you can use this class to read configuration information at any level in the hierarchy. For safety and scalability, you should use an external repository, such as a database, to keep user credentials.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `FormsAuthenticationUser`  
  
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
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [DigestAuthenticationSection Class](../../reference/admin/digestauthenticationsection-class.md)   
 [FormsAuthenticationConfiguration Class](../../reference/admin/formsauthenticationconfiguration-class.md)   
 [FormsAuthenticationCredentials Class](../../reference/admin/formsauthenticationcredentials-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [PassportAuthentication Class](../../reference/admin/passportauthentication-class.md)   
 [WindowsAuthenticationSection Class](../../reference/admin/windowsauthenticationsection-class.md)