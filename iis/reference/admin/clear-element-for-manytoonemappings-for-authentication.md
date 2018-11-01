---
title: "clear Element for manyToOneMappings for authentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d747bae6-6c82-4851-a8f4-ff69955162e2
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# clear Element for manyToOneMappings for authentication
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Many-To-One Mappings \<manyToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings).  
  
 Clears many-to-one mappings for Client Certificate Mapping authentication at the parent level of the configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`iisClientCertificateMappingAuthentication`|Specifies the settings client certificate mapping authentication that is using IIS.|  
|`manyToOneMappings`|Maps client certificates to a set of wildcard criteria that authenticate the certificates and assign a user account.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Many-To-One Mappings \<manyToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<rules>](../../reference/admin/3c47a4ae-b010-4458-9125-3893cecd0f0a.md)