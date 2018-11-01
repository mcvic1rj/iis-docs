---
title: "configurationRedirection Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 18780bf9-144d-4c04-8457-4fb00a239611
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# configurationRedirection Element
> [!NOTE]
>  For more information about the `configurationRedirection` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Redirection \<configurationRedirection>](http://www.iis.net/ConfigReference/configurationRedirection).  
  
 Shares IIS configuration files and encryption keys between one or more IIS servers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether configuration redirection is enabled or disabled on the Web server.<br /><br /> The default value is `false`.|  
|`enableUncPolling`|Optional Boolean attribute.true if UNC polling should be used to check if the configuration files have been updated; otherwise, false if change notifications should be used. Note: The time interval between checks is configured by the pollingPeriod attribute.Note: This attribute was added in IIS 7.5.The default value is false.|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the password that you need to authenticate the user name to access the location for configuration file storage. This is a case sensitive string. **Note:**  To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the location from which to read configuration files and encryption keys. This can be a network path or a folder on the local computer.|  
|`pollingPeriod`|Optional timeSpan attribute.Specifies the time interval between checks that IIS will use to check if the configuration files have been updated. Note: This only applies when the enableUncPolling attribute is set to true.Note: This attribute was added in IIS 7.5.The default value is 00:03:00 (three minutes.)|  
|`userName`|Optional `string` attribute.<br /><br /> Specifies the user name to access the location for configuration file storage.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `configurationRedirection` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Redirection \<configurationRedirection>](http://www.iis.net/ConfigReference/configurationRedirection).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Redirection.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
||The enableUncPolling and pollingPeriod attributes were added in IIS 7.5.|