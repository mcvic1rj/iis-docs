---
title: "handlers Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 29e0dc39-40dc-4db9-868e-0b31a4841513
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# handlers Element
> [!NOTE]
>  For more information about the `handlers` element, see the following topic on the Microsoft IIS.net Web site: [Handlers \<handlers>](http://www.iis.net/ConfigReference/system.webServer/handlers).  
  
 Specifies handlers to process requests made to sites and applications.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`accessPolicy`|Optional `flags` attribute.<br /><br /> Specifies the allowed access types for the entire handlers collection.<br /><br /> The `accessPolicy` attribute can be one of the following possible values. The default is `Read`.<br /><br /> `Execute`: Enables handlers in the handlers collection that require execute rights in directories and files.<br /><br /> `None`: Disables all handlers in the handlers collection that require access to directories or files.<br /><br /> `NoRemoteExecute`: Prevents handlers in the handlers collection from running executables when a handler receives a remote request.<br /><br /> `NoRemoteRead`: Prevents handlers in the handlers collection from reading files when a handler receives a remote request.<br /><br /> `NoRemoteScript`: Prevents handlers in the handlers collection from running scripts when a handler receives a remote request.<br /><br /> `NoRemoteWrite`: Prevents handlers in the handlers collection from creating or changing files when a handler receives a remote request.<br /><br /> `Read`: Enables handlers in the handlers collection that require read access to directories and files.<br /><br /> `Script`: Enables handlers in the handlers collection that require script rights to directories or files.<br /><br /> `Source`: Enables handlers in the handlers collection that require read access to source code (together with the `Read` flag) or write access to source code (together with the `Write` flag).<br /><br /> `Write`: Enables handlers in the handlers collection that require write access to directories and files.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a handler to the collection of handlers.|  
|`clear`|Optional element.<br /><br /> Removes all references to handlers from the handlers collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a handler from the handlers collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `handlers` element, see the following topic on the Microsoft IIS.net Web site: [Handlers \<handlers>](http://www.iis.net/ConfigReference/system.webServer/handlers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-handlers.md)   
 [\<remove>](../../reference/admin/remove-element-for-handlers.md)   
 [\<clear>](../../reference/admin/clear-element-for-handlers.md)