---
title: "iisClientCertificateMappingAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: df5cd1d1-ddde-4604-869a-64e65472395b
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# iisClientCertificateMappingAuthentication Element
> [!NOTE]
>  For more information about the `iisClientCertificateMappingAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [IIS Client Certificate Mapping Authentication \<iisClientCertificateMappingAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication).  
  
 Specifies the settings Client Certificate Mapping authentication using IIS.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultLogonDomain`|Optional `String` attribute.<br /><br /> Specifies the default domain that the server uses to authenticate users.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether Client Certificate Mapping authentication using IIS is enabled.<br /><br /> The default is `False`.|  
|`logonMethod`|Optional `enum` attribute.<br /><br /> The `logonMethod` attribute can be one of the following possible values. The default is ClearText.<br /><br /> For more information on these values, see [LogonUser](http://msdn2.microsoft.com/en-us/library/aa378184.aspx) on the MSDN site.<br /><br /> Batch:<br /><br /> - This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention. The numeric value is 1.<br /><br /> ClearText:<br /><br /> - This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client. The numeric value is 3.<br /><br /> Interactive:<br /><br /> - This logon type is intended for users who will be using the computer interactively. The numeric value is 0.<br /><br /> Network:<br /><br /> - This logon type is intended for high performance servers to authenticate plaintext passwords. Credentials are not cached for this logon type. The numeric value is 2.|  
|`manyToOneCertificateMappingsEnabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether many-to-one mapping is enabled<br /><br /> The default value is `True`.|  
|`oneToOneCertificateMappingsEnabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether one-to-one mapping is enabled<br /><br /> The default value is `True`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`manyToOneMappings`|Optional element.<br /><br /> Maps client certificates to a set of wildcard criteria that authenticate the certificates and assign a user account.|  
|`oneToOneMappings`|Optional element.<br /><br /> Specifies one-to-one client certificate mappings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
  
## Remarks  
 For more information about the `iisClientCertificateMappingAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [IIS Client Certificate Mapping Authentication \<iisClientCertificateMappingAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<manyToOneMappings>](../../reference/admin/manytoonemappings-element-for-iisclientcertificatemappingauthentication.md)   
 [\<oneToOneMappings>](../../reference/admin/onetoonemappings-element-for-security.md)