---
title: "oneToOneMappings Element for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5e6e8827-820a-4fbb-9ca9-d51b5e6f64d4
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# oneToOneMappings Element for security
> [!NOTE]
>  For more information about the `oneToOneMappings` element, see the following topic on the Microsoft IIS.net Web site: [One-To-One Mappings \<oneToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/oneToOneMappings).  
  
 Maps client certificates to a user account for authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a one-to-one mapping to the collection of one-to-one mappings.|  
|`clear`|Optional element.<br /><br /> Removes all references to one-to-one mappings from the one-to-one mappings collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`iisClientCertificateMappingAuthentication`|Specifies the settings client certificate mapping authentication using IIS.|  
  
## Remarks  
 For more information about the `oneToOneMappings` element, see the following topic on the Microsoft IIS.net Web site: [One-To-One Mappings \<oneToOneMappings>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/oneToOneMappings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-onetoonemappings-for-iisclientcertificatemappingauthentication.md)   
 [\<clear>](../../reference/admin/clear-element-for-onetoonemappings.md)