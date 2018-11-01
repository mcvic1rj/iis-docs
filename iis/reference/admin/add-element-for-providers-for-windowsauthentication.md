---
title: "add Element for providers for windowsAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 644899ca-e6cd-495c-b3e7-8249de0f9231
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# add Element for providers for windowsAuthentication
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Windows Authentication Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers/add).  
  
 Adds a security provider for Windows authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Optional `String` attribute.<br /><br /> Specifies the name of the security provider.<br /><br /> By default, there are two providers: Negotiate and NTLM.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`windowsAuthentication`|Specifies Windows authentication configuration.|  
|`providers`|Specifies security support providers used for Windows authentication.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Windows Authentication Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers/add).  
  
 Windows authentication includes the Kerberos v5 and NTLM security providers. Negotiate is a wrapper for Kerberos v5 and NTLM. When you use Negotiate, the client Web browser selects the most appropriate security support provider for authentication.  
  
 If you want to force NTLM, remove the Negotiate provider from the list of providers.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|