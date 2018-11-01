---
title: "add Element for serviceAutoStartProviders for system.applicationHost | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5fca32b8-72f5-4820-b8e5-99b66464c37b
caps.latest.revision: 4
author: "shirhatti"
manager: "wpickett"
---
# add Element for serviceAutoStartProviders for system.applicationHost
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Service Autostart Providers \<add>](http://www.iis.net/ConfigReference/system.applicationHost/serviceAutoStartProviders/add).  
  
 Adds a provider to the collection of autostart providers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a provider to the collection of autostart providers.|  
|`clear`|Optional element.<br /><br /> Clears the collection of autostart providers.|  
|`remove`|Optional element.<br /><br /> Removes a provider from the collection of autostart providers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`serviceAutoStartProviders`|Specifies a collection of managed assemblies that will be loaded when the `AlwaysRunning` is specifed for an application pool's `startMode`.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Service Autostart Providers \<add>](http://www.iis.net/ConfigReference/system.applicationHost/serviceAutoStartProviders/add).  
  
## Element Information  
  
|||  
|-|-|  
|Namespace|ApplicationHost.config|  
|Schema Name|[!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)]|  
  
## See Also  
 [\<serviceAutoStartProviders>](../../reference/admin/serviceautostartproviders-element-for-system-applicationhost.md)