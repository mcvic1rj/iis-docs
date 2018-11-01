---
title: "userIsolation Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 744b142e-469d-4c08-ad9e-0a3d345255f5
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# userIsolation Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the                  `userIsolation` element, see the following topic on the Microsoft IIS.net Web site:                  [FTP User Isolation \<userIsolation>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/userIsolation).  
  
 This element is used to start or restrict FTP clients in specific sections of an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`mode`|Optional                                  `enum` attribute.<br /><br /> Specifies the user isolation mode.<br /><br /> `StartInUsersDirectory`:<br /><br /> - Specifies that user isolation should not be used, but start a session in user's directory if it exists.<br /><br /> - The numeric value is 0.<br /><br /> `IsolateRootDirectoryOnly`:<br /><br /> - Specifies that user isolation should isolate only the root directory. Users' home directories must be physical directories, and global virtual directories can still be used.<br /><br /> - The numeric value is 1.<br /><br /> `ActiveDirectory`:<br /><br /> - Isolates users based on Active Directory settings.<br /><br /> - The numeric value is 2.<br /><br /> `IsolateAllDirectories`:<br /><br /> - Specifies that user isolation should isolate all directories. User's home directories can be either physical directories or virtual directories, but global virtual directories are ignored; all virtual directories must be explicitly created under each user’s home path.<br /><br /> - The numeric value is 3.<br /><br /> `None`:<br /><br /> - Specifies that no user isolation should not be used.<br /><br /> - The numeric value is 4.<br /><br /> `Custom`:<br /><br /> - Specifies that a custom FTP provider will implement the user isolation.<br /><br /> - The numeric value is 5.<br /><br /> When using either the                                  `IsolateRootDirectoryOnly` or                                  `IsolateAllDirectories` modes for user isolation, the physical or virtual directory paths must use the following hierarchy:<br /><br /> Anonymous users:<br /><br /> - `%FtpRoot%\LocalUser\Public`<br /><br /> Local Windows user accounts (Requires Basic authentication):<br /><br /> -                                                  `%FtpRoot%\LocalUser\%UserName%`<br /><br /> Windows domain accounts (Requires Basic authentication):<br /><br /> -                                                  `%FtpRoot%\%UserDomain%\%UserName%`<br /><br /> IIS Manager or ASP.NET custom authentication user accounts:<br /><br /> -                                                 `%FtpRoot%\LocalUser\%UserName%`<br /><br /> The default value is None|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`activeDirectory`|Optional element.<br /><br /> Specifies the connection credentials and time-out for communicating with an Active Directory server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by                                  [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
  
## Remarks  
 For more information about the                  `userIsolation` element, see the following topic on the Microsoft IIS.net Web site:                  [FTP User Isolation \<userIsolation>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/userIsolation).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)