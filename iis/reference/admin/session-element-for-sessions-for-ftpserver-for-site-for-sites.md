---
title: "session Element for sessions for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c8ce8283-6d88-4f36-97a3-425c7a5bd614
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# session Element for sessions for ftpServer for site for sites
> [!NOTE]
>  For more information about the `session` element, see the following topic on the Microsoft IIS.net Web site: [FTP Session \<session>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/sessions/session).  
  
 A collection of elements which are dynamically created by the FTP service as clients connect to your FTP server. The data within these elements can be queried but not modified. Each `session` element contains a terminate method, which allows you to disconnect the client session.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`bytesReceived`|`int64` attribute.<br /><br /> Specifies the cumulative number of bytes that have been received for the session.|  
|`bytesSent`|`int64` attribute.<br /><br /> Specifies the cumulative number of bytes that have been sent for the session.|  
|`clientIp`|`int string` attribute.<br /><br /> Specifies the client's IP address.|  
|`commandStartTime`|`int string` attribute.<br /><br /> Specifies the time that the last command was started.|  
|`currentCommand`|`int string` attribute.<br /><br /> Specifies the currently executing command.|  
|`lastErrorStatus`|`uint` attribute.<br /><br /> Specifies the last FTP reply code.|  
|`previousCommand`|`int string` attribute.<br /><br /> Specifies the previously executed command.|  
|`sessionId`|`int string` attribute.<br /><br /> Specifies the unique identifier for the session.|  
|`sessionStartTime`|`int string` attribute.<br /><br /> Specifies the time that the session was started.|  
|`userName`|`int string` attribute.<br /><br /> Specifies the user name for the session, or `Anonymous` if the session is anonymous.|  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|A collection of elements which are dynamically created by the FTP service as clients connect to your FTP server.|  
|`sessions`|[Use the introduction sentence from this topic.]|  
  
## Remarks  
 For more information about the `session` element, see the following topic on the Microsoft IIS.net Web site: [FTP Session \<session>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/sessions/session).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<sessions>](../../reference/admin/sessions-element-for-ftpserver-for-site-for-sites.md)