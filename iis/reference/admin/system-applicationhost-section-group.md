---
title: "system.applicationHost Section Group | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 63e3f622-760c-4fce-9827-63b0f0b48b7a
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# system.applicationHost Section Group
> [!NOTE]
>  For more information about the `applicationHost` element, see the following topic on the Microsoft IIS.net Web site: [\<system.ApplicationHost>](http://www.iis.net/ConfigReference/system.applicationHost).  
  
 Contains global configuration settings that are used by Windows Process Activation Service (WAS) in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`applicationPools`|Optional element.<br /><br /> Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`configHistory Optional`|Specifies the configuration history settings for a server.|  
|`customMetadata`|Optional element.<br /><br /> Contains settings that are used internally by the Admin Base Object (ABO) mapper component of [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`listenerAdapters`|Optional element.<br /><br /> Specifies configuration settings for *listener adapters*, which are components that establish communication between non-HTTP protocol listeners and WAS.|  
|`log`|Optional element.<br /><br /> Specifies the logging mode for a server.|  
|`serviceAutoStartProviders`|Specifies a collection of managed assemblies that will be loaded when the AlwaysRunning is specifed for an applocation pool's startMode.<br /><br /> Note: This element was added in IIS 7.5.|  
|`sites`|Optional element.<br /><br /> Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`webLimits`|Optional element.<br /><br /> Configures TCP/IP connection and bandwidth limits.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `applicationHost` element, see the following topic on the Microsoft IIS.net Web site: [\<system.ApplicationHost>](http://www.iis.net/ConfigReference/system.applicationHost).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
|**IIS 7.5**|The `serviceAutoStartProviders` element was added in IIS 7.5.|  
  
## See Also  
 [\<applicationPools>](../../reference/admin/applicationpools-section.md)   
 [\<customMetadata>](../../reference/admin/custommetadata-element.md)   
 [\<listenerAdapters>](../../reference/admin/listeneradapters-element.md)   
 [\<log>](../../reference/admin/log-element-for-system-applicationhost.md)   
 [\<serviceAutoStartProviders>](../../reference/admin/serviceautostartproviders-element-for-system-applicationhost.md)   
 [\<sites>](../../reference/admin/sites-element.md)   
 [\<webLimits>](../../reference/admin/weblimits-element.md)