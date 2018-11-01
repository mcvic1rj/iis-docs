---
title: "add Element for oneToOneMappings for iisClientCertificateMappingAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9aa52bb8-6314-4386-8bdf-be01152aa18a
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# add Element for oneToOneMappings for iisClientCertificateMappingAuthentication
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding One-To-One Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/oneToOneMappings/add).  
  
 Adds a one-to-one mapping for Client Certificate Mapping authentication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`certificate`|Required `string` attribute.<br /><br /> Specifies that the server should compare its own certificate with the copy of the certificate sent over the wire as a base64-encoded string by the browser.<br /><br /> The two data strings must be identical for the mapping to proceed. If a client gets another certificate, it will not match the original, even if the copy contains all the same user information as the original.<br /><br /> If there are line breaks in the base64-encoded string of the client certificate in this attribute, you must remove them. Line breaks can interfere with the server's ability to compare the server's certificate with the certificate sent by the browser.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether one-to-one mapping is enabled or not. `True` enables; `false` disables.<br /><br /> The default value is `true`.|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the password of the account used to authenticate clients. **Note:**  To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`username`|Optional `string` attribute.<br /><br /> Specifies the user name of the account used to authenticate clients.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`Configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`Security`|Specifies the section group that contains security-related sections.|  
|`Authentication`|Specifies the section group that contains authentication sections.|  
|`iisClientCertificateMappingAuthentication`|Specifies the settings client certificate mapping authentication using IIS.|  
|`oneToOneMappings`|Maps client certificates to a user account for authentication.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding One-To-One Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/oneToOneMappings/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|