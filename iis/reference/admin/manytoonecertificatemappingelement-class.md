---
title: "ManyToOneCertificateMappingElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 416cb05f-c711-e9a7-a16d-ced7aff9121f
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# ManyToOneCertificateMappingElement Class
Maps one or more certificates to a single user account.  
  
## Syntax  
  
```vbs  
class ManyToOneCertificateMappingElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ManyToOneCertificateMappingElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Description`|A read/write `string` value that contains a description of the mapping.|  
|`Enabled`|A read/write `boolean` value. `true` if the mapping is enabled; otherwise, `false`. The default is `true`.|  
|`Name`|A required read-only `string` value that specifies the name of the mapping. The key property.|  
|`Password`|A read/write `string` value that specifies the password for the Windows user account to which the certificate is mapped.|  
|`PermissionMode`|A read/write `sint32` value that specifies the behavior of the `Rules` property. The possible values are listed later in the Remarks section.|  
|`Rules`|A [ManyToOneCertificateRuleSettings](../../reference/admin/manytoonecertificaterulesettings-class.md) value that contains many-to-one certificate mapping rules.|  
|`UserName`|A read/write `string` value that specifies the user name for the Windows user account to which the certificate is mapped.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class form members of the `ManyToOneMappings` property of the [IisClientCertificateMappingAuthenticationSection](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md) class.  
  
 Many-to-one mapping uses wildcard matching rules that verify whether a client certificate contains specific information, such as the issuer or subject. This mapping does not compare the actual client certificate, but rather accepts all the client certificates that fulfill the specific criteria. If a client gets another certificate that contains all the same user information, the existing mapping will work.  
  
 The following table lists the possible values for the `PermissionMode` property. The default is 1 (`Allow`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|1|`Allow`|The mapping is allowed based on the criteria specified by the `Rules` property.|  
|2|`Deny`|The mapping is denied based on the criteria specified by the `Rules` property.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ManyToOneCertificateMappingElement`  
  
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
 [ManyToOneCertificateMappingRuleElement Class](../../reference/admin/manytoonecertificatemappingruleelement-class.md)   
 [ManyToOneCertificateRuleSettings Class](../../reference/admin/manytoonecertificaterulesettings-class.md)