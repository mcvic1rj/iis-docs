---
title: "extendedProtection Element for windowsAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6469990f-5484-43f1-9592-b39481da6545
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# extendedProtection Element for windowsAuthentication
> [!NOTE]
>  For more information about the extendedProtection element, see the following topic on the Microsoft IIS.net Web site: [Windows Extended Protection \<extendedProtection>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection).  
  
 Specifies the settings that configure the extended protection for Windows authentication in IIS 7.5. Extended protection enhances the existing Windows authentication functionality in order to mitigate authentication relay or "man in the middle" attacks.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`flags`|Optional `flags` attribute.<br /><br /> Specifies the additional behavior settings for extended protection.<br /><br /> The flags attribute can be a combination of the following values; the default value is `None`.<br /><br /> `None`<br /><br /> - This flag specifies that no additional behavior is enabled for extended protection. (For example, no proxy server is being used and SPN checking is enabled and requires FQDNs.)<br /><br /> - The numerical value is 0.<br /><br /> `Proxy`<br /><br /> - This flag specifies that part of the communication path will be through a proxy, or that the client is connecting directly to the destination server over HTTP.<br /><br /> - The numerical value is 1.<br /><br /> `NoServiceNameCheck`<br /><br /> - This flag specifies that SPN checking is disabled; this flag should not be used in scenarios where only SPNs are being checked.<br /><br /> - The numerical value is 2.<br /><br /> `AllowDotlessSpn`<br /><br /> - This flag specifies that SPNs are not required to be FQDNs. Setting this flag allows NetBIOS-based SPNs.<br /><br /> Note:<br /><br /> Setting this flag is not a secure scenario; non-FQDN-based names are vulnerable to name resolution poisoning attacks.<br /><br /> - The numerical value is 4.<br /><br /> `ProxyCohosting`<br /><br /> - This flag specifies that the entire client-to-server communication path will use HTTP only; no part of the communication path will use SSL, and SPN checking will be used. Note: When you specify this flag, you must also specify the `Proxy` flag.<br /><br /> - The numerical value is 32.|  
|`tokenChecking`|Optional `enum` attribute.<br /><br /> Specifies the behavior for checking channel-binding information.<br /><br /> The `tokenChecking` attribute can be one of the following values; the default value is `None`.<br /><br /> `None`<br /><br /> - This value specifies that IIS will not perform channel-binding token checking. This setting emulates the behavior that existed before extended protection.<br /><br /> - The numerical value is 0.<br /><br /> `Allow`<br /><br /> - This value specifies that channel-binding token checking is enabled, but not required. This setting allows secure communication with clients that support extended protection, but still supports clients that are not capable of using extended protection.<br /><br /> - The numerical value is 1.<br /><br /> `Require`<br /><br /> - This value specifies that channel-binding token checking is required. This setting does not provide support for clients that do not support extended protection.<br /><br /> - The numerical value is 2.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`spn`|Adds a SPN to the collection.|  
|`clearSpns`|Clears the collection of SPNs.|  
|`removeSpn`|Removes a SPN from the collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`windowsAuthentication`|Specifies the settings for Windows authentication.|  
  
## Remarks  
 For more information about the extendedProtection element, see the following topic on the Microsoft IIS.net Web site: [Windows Extended Protection \<extendedProtection>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/extendedProtection).  
  
## Element Information  
  
|||  
|-|-|  
|`Configuration locations`|ApplicationHost.config|  
|`Requirements`|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<spn>](../../reference/admin/spn-for-extendedprotection-element-for-windowsauthentication.md)