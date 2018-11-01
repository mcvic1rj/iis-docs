---
title: "application Element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d9f79664-3c50-4db2-9d93-984a53137963
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# application Element for site for sites
> [!NOTE]
>  For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [Application for a Site \<application>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/application).  
  
 Specifies configuration settings for an application in the parent site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`applicationPool`|Optional `string` attribute.<br /><br /> Specifies the application pool to which the application is assigned.|  
|`enabledProtocols`|Optional `string` attribute.<br /><br /> Specifies the protocols through which to communicate with the application.<br /><br /> The default value is `http`. This value enables HTTP and HTTPS protocols for the application.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the virtual path of the application. Must be a unique path within the parent site.|  
|`serviceAutoStartEnabled`|Optional Boolean attribute.`true` if the `autostart` is enabled for this application; otherwise, `false`.The default value is `false`.|  
|`serviceAutoStartProvider`|Optional string attribute.Specifies the name of the `autostart` provider that the Windows Process Activation Service (WAS) will use if `serviceAutoStartEnabled` is set to `true`.There is no default value.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`virtualDirectory`|Optional element.<br /><br /> Specifies configuration settings for a virtual directory in the parent application.|  
|`virtualDirectoryDefaults`|Optional element.<br /><br /> Specifies the default settings for all virtual directories in the parent application.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [Application for a Site \<application>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/application).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
|**IIS 7.5**|The \<application> element was updated to include the serviceAutoStartEnabled and serviceAutoStartProvider attributes.|  
  
## See Also  
 [\<virtualDirectory>](../../reference/admin/virtualdirectory-element-for-application-for-site-for-sites.md)   
 [\<virtualDirectoryDefaults>](../../reference/admin/virtualdirectorydefaults-element-for-application-for-site-for-sites.md)