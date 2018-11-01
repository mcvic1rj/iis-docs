---
title: "messages Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 628a5589-3eda-464e-8386-ab134d8c2c24
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# messages Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `messages` element, see the following topic on the Microsoft IIS.net Web site: [FTP Messages \<messages>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/messages).  
  
 Specify the message that the FTP service will display to FTP clients.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowLocalDetailedErrors`|Optional `Boolean` attribute.<br /><br /> `true` if detailed error messages should be displayed locally; otherwise, `false`. **Note:**  Detailed error messages cannot be displayed remotely. <br /><br /> The default value is `true`.|  
|`bannerMessage`|Optional `string` attribute.<br /><br /> Specifies the message that is displayed when a client connects to the FTP server.<br /><br /> There is no default value.|  
|`exitMessage`|Optional `string` attribute.<br /><br /> Specifies the message that is displayed when a client is closing a connection to the FTP server.<br /><br /> There is no default value.|  
|`expandVariables`|Optional `Boolean` attribute.<br /><br /> `true` if user variables should be expanded; otherwise, `false`.<br /><br /> The default value is `false`.|  
|`greetingMessage`|Optional `string` attribute.<br /><br /> Specifies the message that is displayed after a client has logged in to the FTP server.<br /><br /> There is no default value.|  
|`maxClientsMessage`|Optional `string` attribute.<br /><br /> Specifies the message that is displayed when a client tries to log in and the maximum number of clients has already been reached on the FTP server.<br /><br /> There is no default value.|  
|`suppressDefaultBanner`|Optional `Boolean` attribute.<br /><br /> `true` if the FTP service should suppress the default "Microsoft FTP Service" banner; otherwise, false.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features on FTP sites.|  
  
## Remarks  
 For more information about the `messages` element, see the following topic on the Microsoft IIS.net Web site: [FTP Messages \<messages>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/messages).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)