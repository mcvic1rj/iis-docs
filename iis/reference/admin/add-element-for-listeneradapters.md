---
title: "add Element for listenerAdapters | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9cf795da-8fb6-46d4-b2e3-16e96d859cf9
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# add Element for listenerAdapters
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Listener Adapters \<add>](http://www.iis.net/ConfigReference/system.applicationHost/listenerAdapters/add).  
  
 Specifies configuration settings for a non-HTTP listener adapter that can be used by Windows Process Activation Service (WAS) to communicate with a listener service.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`identity`|Optional `string` attribute.<br /><br /> Specifies a local account name, a domain account, or a built-in account. The identity is used to help secure the WAS communication channel between the listener service and the listener adapter.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of the listener adapter to which WAS connects the listener service.|  
|`protocolManagerDll`|Optional `string` attribute.<br /><br /> Specifies the fully qualified path or short name of the DLL that contains the listener adapter's code. The DLL must be found on disk (by using standard search procedures that depend on DLL type) in order for the function specified in `protocolManagerDllInitFunction` to be called.|  
|`protocolManagerDllInitFunction`|Optional `string` attribute.<br /><br /> Specifies the name of the function to call in the custom listener adapter code. The DLL specified in the `protocolManagerDll` attribute must contain the function specified in the `protocolManagerDllInitFunction` attribute.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`listenerAdapters`|Specifies configuration settings for listener adapters.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Listener Adapters \<add>](http://www.iis.net/ConfigReference/system.applicationHost/listenerAdapters/add).  
  
 Changes to the `listenerAdapters` element take effect only when a listener adapter connects with WAS. You must restart WAS for changes to take effect.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|