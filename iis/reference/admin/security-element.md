---
title: "security Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5363e220-8705-484b-b3ab-4808eac24e51
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# security Element
> [!NOTE]
>  For more information about the `security` element, see the following topic on the Microsoft IIS.net Web site: [Security \<security>](http://www.iis.net/ConfigReference/system.webServer/security).  
  
 Specifies the section group that contains security-related sections.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`access`|Optional element.<br /><br /> Specifies configuration settings for Secure Sockets Layer (SSL) such as whether to use client certificates for authentication and crypto strength.|  
|`applicationDependencies`|Optional element.<br /><br /> Specifies an application that has dependencies to one or more CGI or ISAPI extension restrictions.|  
|`authentication`|Optional element.<br /><br /> Specifies authentication-related settings|  
|`authorization`|Optional element.<br /><br /> Specifies authorization-related settings.|  
|`ipSecurity`|Optional element.<br /><br /> Specifies access restrictions based on the IP version 4 address or DNS domain name.|  
|`isapiCgiRestriction`|Optional element.<br /><br /> Specifies settings that restrict which CGI and ISAPI programs are allowed to run on the server.|  
|`requestFiltering`|Optional element.<br /><br /> Specifies configuration settings for request filtering.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `security` element, see the following topic on the Microsoft IIS.net Web site: [Security \<security>](http://www.iis.net/ConfigReference/system.webServer/security).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<access>](../../reference/admin/access-element-for-security.md)   
 [\<applicationDependencies>](../../reference/admin/applicationdependencies-element-for-security-element.md)   
 [\<authentication>](../../reference/admin/authentication-element.md)   
 [\<authorization>](../../reference/admin/authorization-element-for-security.md)   
 [\<ipSecurity>](../../reference/admin/ipsecurity-element.md)   
 [\<isapiCgiRestriction>](../../reference/admin/isapicgirestriction-element.md)   
 [\<requestFiltering>](../../reference/admin/requestfiltering-element-for-security.md)