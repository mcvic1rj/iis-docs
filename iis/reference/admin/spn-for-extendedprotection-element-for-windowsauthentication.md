---
title: "spn for extendedProtection Element for windowsAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 675385b2-080e-4674-ad71-6f29c56a0607
caps.latest.revision: 5
author: "shirhatti"
manager: "wpickett"
---
# spn for extendedProtection Element for windowsAuthentication
> [!NOTE]
>  For more information about the `spn` element, see the following topic on the Microsoft IIS.net Web site: [Service Principle Name \<spn>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection/spn).  
  
 Adds a Service Principle Name (SPN) to the collection of SPNs. Each SPN specifies a unique endpoint for client activity using the extended protection features for Windows authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Optional `string` attribute.<br /><br /> Specifies a unique SPN.<br /><br /> There is no efault value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`windowsAuthentication`|Specifies the settings for Windows authentication.|  
|`extendedProtection`|Specifies extended protection options for Windows authentication.|  
  
## Remarks  
 For more information about the `spn` element, see the following topic on the Microsoft IIS.net Web site: [Service Principle Name \<spn>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection/spn).  
  
## Element Information  
  
|||  
|-|-|  
|`Configuration locations`|ApplicationHost.config|  
|`Requirements`|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<extendedProtection>](../../reference/admin/extendedprotection-element-for-windowsauthentication.md)