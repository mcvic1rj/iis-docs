---
title: "add Element for manyToOneMappings for iisClientCertificateMappingAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6060dd9b-93f9-42d9-be5b-c28688fd9e99
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# add Element for manyToOneMappings for iisClientCertificateMappingAuthentication
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Many-To-One Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings/add).  
  
 Adds many-to-one client certificate mappings. These mappings allow many clients to use one certificate.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`description`|Optional `string` attribute.<br /><br /> Specifies the description of this one-to-many mapping.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether this one-to-many mapping is enabled or not. `True` enables; `false` disables.<br /><br /> The default value is `true`.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of this one-to-many mapping.|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the password of the account used to authenticate clients that match this rule.<br /><br /> Note:<br /><br /> To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`permissionMode`|Optional `enum` attribute.<br /><br /> The `permissionMode` attribute can be one of the following possible values. The default is Allow.<br /><br /> Allow:<br /><br /> - Specifies that clients with a matching client certificate should be allowed permission to authenticate. The numeric value is 1.<br /><br /> Deny:<br /><br /> - Specifies that clients with a matching client certificate should be denied permission to authenticate. The numeric value is 2.|  
|`username`|Optional `string` attribute.<br /><br /> Specifies the username of the account used to authenticate clients that match this rule.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`rules`|Optional element.<br /><br /> Specifies criteria for mapping client certificates with IIS so that many clients can use one certificate.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`iisClientCertificateMappingAuthentication`|Specifies the settings client certificate mapping authentication using IIS.|  
|`manyToOneMappings`|Maps client certificates containing wildcard criteria to a user account for authentication.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Many-To-One Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/iisClientCertificateMappingAuthentication/manyToOneMappings/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<rules>](../../reference/admin/3c47a4ae-b010-4458-9125-3893cecd0f0a.md)