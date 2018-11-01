---
title: "serviceAutoStartProviders Element for system.applicationHost | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9c3094d2-8dfa-4cde-9a41-4cbb5f14d413
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# serviceAutoStartProviders Element for system.applicationHost
> [!NOTE]
>  For more information about the `serviceAutoStartProviders` element, see the following topic on the Microsoft IIS.net Web site: [Service Autostart Providers \<serviceAutoStartProviders>](http://www.iis.net/ConfigReference/system.applicationHost/serviceAutoStartProviders).  
  
 Specifies a collection of managed assemblies that Windows Process Activation Service (WAS) will load automatically when the `startMode` attribute of an application pool is set to `AlwaysRunning`. This collection allows developers to specify assemblies that perform initialization tasks before any HTTP requests are serviced.  
  
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
  
## Remarks  
 For more information about the `serviceAutoStartProviders` element, see the following topic on the Microsoft IIS.net Web site: [Service Autostart Providers \<serviceAutoStartProviders>](http://www.iis.net/ConfigReference/system.applicationHost/serviceAutoStartProviders).  
  
## Element Information  
  
|||  
|-|-|  
|Namespace|ApplicationHost.config|  
|Schema Name|[!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)]|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-serviceautostartproviders-for-system-applicationhost.md)