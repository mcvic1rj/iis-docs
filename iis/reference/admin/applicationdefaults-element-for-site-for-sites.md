---
title: "applicationDefaults Element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2266a299-f671-40b2-80ac-fcf5c5149139
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# applicationDefaults Element for site for sites
> [!NOTE]
>  For more information about the `applicationDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Defaults \<applicationDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/applicationDefaults).  
  
 Specifies default settings for all applications in the parent site. If the same attribute or child element is configured in both the applicationDefaults section and in the application section for a specific application, the configuration in the application section is used for that application.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`applicationPool`|Optional `string` attribute.<br /><br /> Specifies the default application pool to which all applications in the parent site are assigned.|  
|`enabledProtocols`|Optional `string` attribute.<br /><br /> Specifies the protocols through which to communicate with all applications in the parent site.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the default virtual path of all applications in the parent site.|  
|`serviceAutoStartEnabled`|Optional Boolean attribute.`true` if the autostart is enabled for this application; otherwise, `false`.The default value is `false`.|  
|`serviceAutoStartProvider`|Optional string attribute.Specifies the name of the autostart provider that the Windows Process Activation Service (WAS) will use if `serviceAutoStartEnabled` is set to `true`.There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `applicationDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Defaults \<applicationDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/applicationDefaults).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
|**IIS 7.5**|The \<application> element was updated to include the serviceAutoStartEnabled and serviceAutoStartProvider attributes.|