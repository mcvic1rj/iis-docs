---
title: "authentication Element for management | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8cfedf91-431f-450d-bf3a-7d87d93c15f7
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# authentication Element for management
> [!NOTE]
>  For more information about the `authentication` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication \<authentication>](http://www.iis.net/ConfigReference/system.webServer/management/authentication).  
  
 Configures authentication settings for remote management of the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultProvider`|Optional `string` attribute.<br /><br /> Specifies the default provider that provides authentication for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users on the Web server.<br /><br /> If you change the default provider, you must restart the Management Service (WMSVC) for changes to take effect. If you have [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] open, you must also reopen [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`credentials`|Optional element.<br /><br /> Configures [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user credentials for users to connect to sites and applications on the server by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`providers`|Optional element.<br /><br /> Configures authentication providers that authenticate [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `authentication` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication \<authentication>](http://www.iis.net/ConfigReference/system.webServer/management/authentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<credentials>](../../reference/admin/credentials-element-for-authentication.md)   
 [\<providers>](../../reference/admin/providers-element-for-authentication.md)