---
title: "OneToOneSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 87c2bd23-5ce9-4a1a-9413-f159f54436a1
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# OneToOneSettings Class
Contains one-to-one client certificate mappings.  
  
## Syntax  
  
```vbs  
class OneToOneSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `OneToOneSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`OneToOneMappings`|An array of [OneToOneCertificateMappingElement](../../reference/admin/onetoonecertificatemappingelement-class.md) values that specify one-to-one client certificate mappings.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `OneToOneMappings` array property of the [IisClientCertificateMappingAuthenticationSection](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `OneToOneSettings`  
  
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
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [ManyToOneCertificateMappingElement Class](../../reference/admin/manytoonecertificatemappingelement-class.md)   
 [ManyToOneCertificateMappingRuleElement Class](../../reference/admin/manytoonecertificatemappingruleelement-class.md)   
 [ManyToOneSettings Class](../../reference/admin/manytoonesettings-class.md)   
 [OneToOneCertificateMappingElement Class](../../reference/admin/onetoonecertificatemappingelement-class.md)