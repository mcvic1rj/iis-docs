---
title: "OneToOneCertificateMappingElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0bacbe93-6725-b59a-6776-9f74e8de1484
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# OneToOneCertificateMappingElement Class
Represents a one-to-one mapping of a Secure Sockets Layer (SSL) certificate to a user account.  
  
## Syntax  
  
```vbs  
class OneToOneCertificateMappingElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `OneToOneCertificateMappingElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Certificate`|A read-only `string` value that specifies an SSL certificate. The key property.|  
|`Enabled`|A read/write `boolean` value. `true` if one-to-one certificate mapping is enabled for the certificate specified in the `Certificate` property; otherwise, `false`. The default is `true`.|  
|`Password`|A read/write `string` value that specifies the password for the Windows user account to which the certificate is mapped.|  
|`UserName`|A read/write `string` value that specifies the user name of the user account to which the SSL certificate is mapped.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `OneToOneMappings` array property of the [OneToOneSettings](../../reference/admin/onetoonesettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `OneToOneCertificateMappingElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AccessSection Class](../../reference/admin/accesssection-class.md)   
 [ClientCertificateMappingAuthenticationSection Class](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [ManyToOneCertificateMappingElement Class](../../reference/admin/manytoonecertificatemappingelement-class.md)   
 [ManyToOneCertificateMappingRuleElement Class](../../reference/admin/manytoonecertificatemappingruleelement-class.md)   
 [OneToOneSettings Class](../../reference/admin/onetoonesettings-class.md)   
 [SSLBinding Class](../../reference/admin/sslbinding-class.md)