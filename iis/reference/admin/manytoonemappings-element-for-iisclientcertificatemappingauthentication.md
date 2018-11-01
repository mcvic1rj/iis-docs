---
title: "manyToOneMappings Element for iisClientCertificateMappingAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8e220e92-3781-460b-acff-89d62dfe5ae8
caps.latest.revision: 28
author: "shirhatti"
manager: "wpickett"
---
# manyToOneMappings Element for iisClientCertificateMappingAuthentication
> [!NOTE]
>  For more information about the `manyToOneMappings` element, see the following topic on the Microsoft IIS.net Web site: [Many-To-One Mappings \<manyToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings).  
  
 Maps client certificates containing wildcard criteria to a user account for authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a mapping to the collection of manyToOneMappings.|  
|`clear`|Optional element.<br /><br /> Removes all references to mappings from the manyToOneMappings collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`iisClientCertificateMappingAuthentication`|Specifies the settings client certificate mapping authentication using IIS.|  
  
## Remarks  
 For more information about the `manyToOneMappings` element, see the following topic on the Microsoft IIS.net Web site: [Many-To-One Mappings \<manyToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-manytoonemappings-for-iisclientcertificatemappingauthentication.md)   
 [\<clear>](../../reference/admin/clear-element-for-manytoonemappings-for-authentication.md)