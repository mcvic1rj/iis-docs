---
title: "anonymousAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 24a3973e-c91e-4aa9-bb8d-1a3ea96574e2
caps.latest.revision: 36
author: "shirhatti"
manager: "wpickett"
---
# anonymousAuthentication Element
> [!NOTE]
>  For more information about the `anonymousAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Anonymous Authentication \<anonymousAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/anonymousAuthentication).  
  
 Specifies Anonymous authentication configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether Anonymous authentication is enabled.<br /><br /> The default value is `True`.|  
|`logonMethod`|Optional `enum` attribute.<br /><br /> The `logonMethod` attribute can be one of the following possible values. The default is ClearText.<br /><br /> For more information on these values, see [LogonUser](http://msdn2.microsoft.com/en-us/library/aa378184.aspx) on the MSDN site.<br /><br /> Batch:<br /><br /> - This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention. The numeric value is 1.<br /><br /> ClearText:<br /><br /> - This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client. The numeric value is 3.<br /><br /> Interactive:<br /><br /> - This logon type is intended for users who will be using the computer interactively. The numeric value is 0.<br /><br /> Network:<br /><br /> - This logon type is intended for high performance servers to authenticate plaintext passwords. Credentials are not cached for this logon type. The numeric value is 2.|  
|`password`|Optional `String` attribute.<br /><br /> Specifies the password for Anonymous authentication.<br /><br /> To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`username`|Optional `String` attribute.<br /><br /> Specifies the username for Anonymous authentication. If you leave this value blank (i.e., username=""), Anonymous authentication uses the application pool identity to authenticate anonymous users.<br /><br /> The default value is IUSR.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
  
## Remarks  
 For more information about the `anonymousAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Anonymous Authentication \<anonymousAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/anonymousAuthentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|