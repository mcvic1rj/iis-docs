---
title: "authentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 98bef86a-90c2-4e0e-9e4f-56e05fb9900b
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# authentication Element
> [!NOTE]
>  For more information about the `authentication` element, see the following topic on the Microsoft IIS.net Web site: [Security Authentication \<authentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication).  
  
 Specifies the section group that contains authentication sections.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`anonymousAuthentication`|Optional element.<br /><br /> Specifies the settings for Anonymous authentication.|  
|`basicAuthentication`|Optional element.<br /><br /> Specifies the settings for Basic authentication.|  
|`clientCertificateMappingAuthentication`|Optional element.<br /><br /> Specifies the settings Client Certificate Mapping authentication using Active Directory.|  
|`digestAuthentication`|Optional element.<br /><br /> Specifies the settings for Digest authentication.|  
|`iisClientCertificateMappingAuthentication`|Optional element.<br /><br /> Specifies the settings Client Certificate Mapping authentication using IIS.|  
|`windowsAuthentication`|Optional element.<br /><br /> Specifies the settings for Windows authentication.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `authentication` element, see the following topic on the Microsoft IIS.net Web site: [Security Authentication \<authentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<anonymousAuthentication>](../../reference/admin/anonymousauthentication-element.md)   
 [\<basicAuthentication>](../../reference/admin/basicauthentication-element.md)   
 [\<clientCertificateMappingAuthentication>](../../reference/admin/clientcertificatemappingauthentication-element.md)   
 [\<digestAuthentication>](../../reference/admin/digestauthentication-element.md)   
 [\<iisClientCertificateMappingAuthentication>](../../reference/admin/iisclientcertificatemappingauthentication-element.md)   
 [\<windowsAuthentication>](../../reference/admin/windowsauthentication-element.md)