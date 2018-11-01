---
title: "providers Element for authentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8595e0e6-7209-4a6e-8fdb-7606d8b970fd
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# providers Element for authentication
> [!NOTE]
>  For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/providers).  
  
 Configures authentication providers that authenticate [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. The default authentication provider, ConfigurationAuthenticationProvider, uses IIS configuration to store [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user credentials.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a provider to the collection of authentication providers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authentication`|Configures authentication settings for remote management of the Web server.|  
  
## Remarks  
 For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/providers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-providers-for-authentication.md)