---
title: "ManyToOneCertificateMappingRuleElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 04fe2a42-1c6f-8e6c-c296-7c03eec6ec42
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# ManyToOneCertificateMappingRuleElement Class
Represents a many-to-one certificate mapping rule.  
  
## Syntax  
  
```vbs  
class ManyToOneCertificateMappingRuleElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ManyToOneCertificateMappingRuleElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`CertificateField`|A required unique read/write `sint32` value that specifies whether the mapping rule applies to the subject or issuer of the certificate. The possible values are listed later in the Remarks section. A key property.|  
|`CertificateSubField`|A required unique read/write `string` value that specifies the certificate subfield against which the `MatchCriteria` property is applied. A key property.|  
|`CompareCaseSensitive`|A required unique read/write `boolean` value. `true` if the comparison performed using the `MatchCriteria` property is case-sensitive; otherwise, `false`. A key property.|  
|`MatchCriteria`|A required unique read/write `string` value that specifies the value that must be present in the certificate subfield in order for the client certificate to be mapped to a token user account. A key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Rules` array property of the `ManyToOneCertificateRuleSettings` class.  
  
 The following table lists the possible values for the `CertificateField` property.  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|1|`Subject`|The rule applies to the subject of the certificate.|  
|2|`Issuer`|The rule applies to the issuer of the certificate.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ManyToOneCertificateMappingRuleElement`  
  
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
 [ManyToOneCertificateRuleSettings Class](../../reference/admin/manytoonecertificaterulesettings-class.md)   
 [OneToOneCertificateMappingElement Class](../../reference/admin/onetoonecertificatemappingelement-class.md)