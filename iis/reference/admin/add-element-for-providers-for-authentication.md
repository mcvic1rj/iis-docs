---
title: "add Element for providers for authentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ebe1947d-bd74-44ad-b011-77c198865ba4
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# add Element for providers for authentication
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authentication Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/providers/add).  
  
 Adds a provider to the collection of authentication providers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the authentication provider.|  
|`type`|Required `string` attribute.<br /><br /> Specifies the managed type of the authentication provider.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authentication`|Configures authentication settings for remote management of the Web server.|  
|`providers`|Configures authentication providers that authenticate [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authentication Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/providers/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|