---
title: "add Element for scope for authorizationRules for authorization | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d29d4117-3cd2-48fe-8109-b0dd895ebc97
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# add Element for scope for authorizationRules for authorization
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authorization Rules Scope \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules/scope/add).  
  
 Adds an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user or Windows user or Windows group to the collection of users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user, a Windows user, or a Windows group that is authorized to connect to the site or application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`isRole`|Optional `Boolean` attribute.<br /><br /> Specifies whether the entry is a Windows group. When `true`, the entry is a Windows group and any Windows users that belong to that group can connect to the site or application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authorization`|Configures authorization settings for remote management of the Web server.|  
|`authorizationRules`|Configures the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`scope`|Configures the virtual path of the site or application to which [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users are authorized to connect by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authorization Rules Scope \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules/scope/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|