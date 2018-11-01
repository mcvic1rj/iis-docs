---
title: "basicAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4ecba9ca-c35c-4a2e-bcfc-d1591e43e53c
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# basicAuthentication Element
> [!NOTE]
>  For more information about the `basicAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Basic Authentication \<basicAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/basicAuthentication).  
  
 Specifies Basic authentication configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultLogonDomain`|Optional `String` attribute.<br /><br /> Specifies the default logon domain for Basic authentication.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether Basic authentication is enabled.<br /><br /> The default value is `False`.|  
|`logonMethod`|Optional `enum` attribute.<br /><br /> The `logonMethod` attribute can be one of the following possible values. The default is ClearText.<br /><br /> For more information about these values, see [LogonUser](http://msdn2.microsoft.com/en-us/library/aa378184.aspx) on the MSDN site.<br /><br /> Batch:<br /><br /> - This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention. The numeric value is 1.<br /><br /> ClearText:<br /><br /> - This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client. The numeric value is 3.<br /><br /> Interactive:<br /><br /> - This logon type is intended for users who will be interactively using the computer. The numeric value is 0.<br /><br /> Network:<br /><br /> - This logon type is intended for high performance servers to authenticate plaintext passwords. Credentials are not cached for this logon type. The numeric value is 2.|  
|`realm`|Optional `String` attribute.<br /><br /> Specifies the realm for Basic authentication.|  
  
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
 For more information about the `basicAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Basic Authentication \<basicAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/basicAuthentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|