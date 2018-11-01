---
title: "RoleManagerSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4215b69c-7f4b-0364-eaf8-3c63d39a936f
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# RoleManagerSection Class
Defines configuration settings that are used to support the role management infrastructure of Web applications.  
  
## Syntax  
  
```vbs  
class RoleManagerSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `RoleManagerSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|(Inherited from [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md).)|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `RoleManagerSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`CacheRolesInCookie`|A read/write `boolean` value. `true` if the current user's roles are cached in a cookie; otherwise, `false`. The default is `false`.|  
|`CookieName`|A read/write `string` value that specifies the name of the cookie that is used to cache role names. The default is ".ASPXROLES".|  
|`CookiePath`|A read/write `string` value that specifies the virtual path of the cookie that is used to cache role names. The default is "/".|  
|`CookieProtection`|A read/write `sint32` enumeration that specifies the cookie protection scheme. The possible values are listed later in the Remarks section.|  
|`CookieRequireSSL`|A read/write `boolean` value. `true` if the cookie that is used to cache role names requires a Secure Sockets Layer (SSL) connection in order to be returned to the server; otherwise, `false`. The default is `false`.|  
|`CookieSlidingExpiration`|A read/write `boolean` value. `true` if the cookie that is used to cache role names will be reset periodically; otherwise, `false`. The default is `true`.|  
|`CookieTimeout`|A read/write `datetime` value that specifies the amount of time, in minutes, before the cookie that is used to cache role names expires. The default is 30 minutes.|  
|`CreatePersistentCookie`|A read/write `boolean` value. `true` if role names are made cookie-persistent across browser sessions; otherwise, `false`. The default is false.<br /><br /> The `CreatePersistentCookie` property indicates whether the cookie that is used to cache role names should be a persistent cookie, which means that the cookie is available across browser sessions, or a session-based cookie, which means that the cookie is lost when the browser is closed. The default is `false`, which indicates that a session-based cookie is used to cache role names.|  
|`DefaultProvider`|A read/write `string` value that specifies the name of the default provider that is used to manage roles. The default is "AspNetSqlRoleProvider". This property must match a named value specified in the `Providers` property. An empty string ("") is not a valid value.|  
|`Domain`|A read/write `string` value that specifies the name of the domain that is associated with the cookie that is used to cache role names. The default is an empty string (""). If no value is specified, the `Domain` property returns `null`.|  
|`Enabled`|A read/write `boolean` value. `true` if the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] role management feature is enabled (that is, it can be accessed at run time); otherwise, `false`. The default is `false`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`MaxCachedResults`|A read/write `sint32` value that specifies the maximum number of roles that [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] caches in the role cookie. The default is 25.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Providers`|A [ProvidersSettings](../../reference/admin/providerssettings-class.md) value that specifies role management providers. **Note:**  Role management providers are components that provide access to the types of roles for a site.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table lists the possible values for the `CookieProtection` property. The default is 3 (`All`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`None`|Specifies that the cookie information is not protected. Information in the cookie is stored in clear text and is not validated when the information is sent back to the server.|  
|1|`Validation`|Ensures that the information in the cookie has not been changed before the information is sent back to the server.|  
|2|`Encryption`|Encrypts the information in the cookie.|  
|3|`All`|Specifies that both the `Validation` and `Encryption` values are used to protect the information in the cookie.|  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `RoleManagerSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [NameTypeElement Class](../../reference/admin/nametypeelement-class.md)   
 [ProvidersSettings Class](../../reference/admin/providerssettings-class.md)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)