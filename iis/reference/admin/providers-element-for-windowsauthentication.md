---
title: "providers Element for windowsAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a571113f-2e9d-4fae-b42e-1ea1ab8fd512
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# providers Element for windowsAuthentication
> [!NOTE]
>  For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers).  
  
 Specifies security support providers used for Windows authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a security provider to the collection of providers. Windows authentication requires at least one provider.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a security provider from the providers collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to providers from the provider collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`windowsAuthentication`|Specifies Windows authentication configuration.|  
  
## Remarks  
 For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-providers-for-windowsauthentication.md)   
 [\<remove>](../../reference/admin/remove-element-for-providers-for-windowsauthentication.md)   
 [\<clear>](../../reference/admin/clear-element-for-providers-for-windowsauthentication.md)