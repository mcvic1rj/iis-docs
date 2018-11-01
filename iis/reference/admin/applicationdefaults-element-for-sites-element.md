---
title: "applicationDefaults Element for sites Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a6915a8a-b0a6-4e24-bcf2-a840cc3a9c04
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# applicationDefaults Element for sites Element
> [!NOTE]
>  For more information about the `applicationDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Defaults \<applicationDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/applicationDefaults).  
  
 Specifies default settings for all applications in the sites on the server. If the same attribute or child element is configured in both the `applicationDefaults` section and in the application section for a specific application, the configuration in the application section is used for that application.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`applicationPool`|Optional `string` attribute.<br /><br /> Specifies the default application pool to which all applications on the server are assigned.|  
|`enabledProtocols`|Optional `string` attribute.<br /><br /> Specifies the default protocols through which to communicate with all applications on the server.<br /><br /> The default value is `http`. This value enables HTTP and HTTPS protocols an application.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the default virtual path of all applications on the server.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
  
## Remarks  
 For more information about the `applicationDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Defaults \<applicationDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/applicationDefaults).  
  
 For more information, see http://www.iis.net/ConfigReference/system.applicationHost/sites/applicationDefaults  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|