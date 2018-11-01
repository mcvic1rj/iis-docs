---
title: "windowsAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d2381dbe-93c3-4ebd-9278-3491cf25d2be
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# windowsAuthentication Element
> [!NOTE]
>  For more information about the `windowsAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication \<windowsAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection/spn).  
  
 Specifies Windows authentication configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`AuthPersistNonNTLM`|Optional `boolean` attribute.<br /><br /> Specifies whether IIS automatically re-authenticates every non-NTLM (for example, Kerberos) request, even those on the same connection. `False` enables multiple authentications for the same connections.<br /><br /> The default is `True`. **Note:**  A setting of `True` means that the client will be authenticated only once on the same connection. IIS will cache a token or ticket on the server for a TCP session that stays established.|  
|`authPersistSingleRequest`|Optional `Boolean` attribute.<br /><br /> Setting this flag to `True` specifies that authentication persists only for a single request on a connection. IIS resets the authentication at the end of each request, and forces re-authentication on the next request of the session.<br /><br /> The default value is `False`.|  
|`enabled`|Required `Boolean` attribute.<br /><br /> Specifies whether Windows authentication is enabled.<br /><br /> The default value is `False`.|  
|`useKernelMode`|Optional `Boolean` attribute.<br /><br /> Specifies whether Windows authentication is done in kernel mode. `True` specifies that Windows authentication uses kernel mode.<br /><br /> Kernel-mode authentication may improve authentication performance and prevent authentication problems with application pools configured to use a custom identity.<br /><br /> As a best practice, do not disable this setting if you use Kerberos authentication and have a custom identity on the application pool.<br /><br /> The default is `True`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`extendedProtection`|Optional element.<br /><br /> Specifies extended protection options for Windows authentication. **Note:**  This element was added in IIS 7.5.|  
|`providers`|Optional element.<br /><br /> Specifies security support providers used for Windows authentication.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
  
## Remarks  
 For more information about the `windowsAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication \<windowsAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection/spn).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<extendedProtection>](../../reference/admin/extendedprotection-element-for-windowsauthentication.md)   
 [\<providers>](../../reference/admin/providers-element-for-windowsauthentication.md)