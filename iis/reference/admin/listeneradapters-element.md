---
title: "listenerAdapters Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5b8e6af0-5c2b-479f-ac39-7c4d96cbde92
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# listenerAdapters Element
> [!NOTE]
>  For more information about the `listenerAdapters` element, see the following topic on the Microsoft IIS.net Web site: [Listener Adapters \<listenerAdapters>](http://www.iis.net/ConfigReference/system.applicationHost/listenerAdapters).  
  
 Specifies configuration settings for *listener adapters*, which are components that establish communication between non-HTTP protocol listeners and the Windows Process Activation Service (WAS).  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Specifies the configuration for a listener adapter.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `listenerAdapters` element, see the following topic on the Microsoft IIS.net Web site: [Listener Adapters \<listenerAdapters>](http://www.iis.net/ConfigReference/system.applicationHost/listenerAdapters).  
  
 Changes to the `listenerAdapters` element take effect only when a listener adapter connects with WAS. In most cases, this connection requires that the server be restarted.  
  
 The W3SVC service, which contains HTTP-specific functionality, does not use `listenerAdapter` configuration settings.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-listeneradapters.md)