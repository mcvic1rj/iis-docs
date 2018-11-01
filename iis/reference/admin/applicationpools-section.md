---
title: "applicationPools Section | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 369a9c46-bd76-40f7-8ef8-b5efed412117
caps.latest.revision: 35
author: "shirhatti"
manager: "wpickett"
---
# applicationPools Section
> [!NOTE]
>  For more information about the `applicationPools` element, see the following topic on the Microsoft IIS.net Web site: [Application Pools \<applicationPools>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools).  
  
 Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Adds an application pool to the `applicationPools` section.|  
|`applicationPoolDefaults`|Required `string` attribute.<br /><br /> Configures the default settings for all application pools in an `applicationPools` section.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `applicationPools` element, see the following topic on the Microsoft IIS.net Web site: [Application Pools \<applicationPools>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-applicationpools.md)   
 [\<applicationPoolDefaults>](../../reference/admin/applicationpooldefaults-element-for-applicationpools.md)