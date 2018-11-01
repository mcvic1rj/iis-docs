---
title: "virtualDirectoryDefaults Element for application for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 796a37ac-ce3b-4cf8-9ac8-9b9afdbaee65
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# virtualDirectoryDefaults Element for application for site for sites
> [!NOTE]
>  For more information about the `virtualDirectoryDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Virtual Directory Defaults \<virtualDirectoryDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/application/virtualDirectoryDefaults).  
  
 Specifies the default settings for all virtual directories in the parent application. If the same attribute or child element is configured in both the `virtualDirectoryDefaults` section and in the `virtualDirectory` section for a specific virtual directory, the configuration in the `virtualDirectory` section is used for that virtual directory.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowSubDirConfig`|Optional `Boolean` attribute.<br /><br /> Specifies whether IIS looks for Web.config files in content directories lower than the current level (`true`) or does not look for Web.config files in content directories lower than the current level (`false`).<br /><br /> The default value is `true`.|  
|`logonMethod`|Optional `enum` attribute.<br /><br /> Specifies the default logon method for virtual directories in the parent application.<br /><br /> The `logonMethod` attribute can be one of the following possible values. The default is `ClearText`.<br /><br /> `Batch`<br /><br /> - This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.<br /><br /> - The numeric value is 1.<br /><br /> `ClearText`<br /><br /> - This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client.<br /><br /> - The numeric value is 3.<br /><br /> `Interactive`<br /><br /> - This logon type is intended for users who will be interactively using the computer.<br /><br /> - The numeric value is 0.<br /><br /> `Network`<br /><br /> - This logon type is intended for high performance servers to authenticate plaintext passwords. Credentials are not cached for this logon type.<br /><br /> - The numeric value is 2.<br /><br /> For more information about these values, see [LogonUser](http://msdn2.microsoft.com/en-us/library/aa378184.aspx) on the MSDN site.|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the password associated with the user name.<br /><br /> Note:<br /><br /> To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the default virtual path of all virtual directories in the parent application.|  
|`physicalPath`|Optional `string` attribute.<br /><br /> Specifies the default physical path of all virtual directories in the parent application.|  
|`userName`|Optional `string` attribute.<br /><br /> Specifies the default user name of an account that can access configuration files and content for virtual directories in the parent application.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`application`|Specifies configuration settings for an application in the parent site.|  
  
## Remarks  
 For more information about the `virtualDirectoryDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Virtual Directory Defaults \<virtualDirectoryDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/application/virtualDirectoryDefaults).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|