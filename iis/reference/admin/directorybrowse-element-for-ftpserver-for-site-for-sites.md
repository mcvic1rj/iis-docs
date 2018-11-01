---
title: "directoryBrowse Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 839d73b1-bf4c-45f1-ad8b-86e8a50408bc
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# directoryBrowse Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `directoryBrowse` element, see the following topic on the Microsoft IIS.net Web site: [FTP Directory Browse \<directoryBrowse>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/directoryBrowse).  
  
 Specifies the content settings for directory browsing on an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`showFlags`|Optional `flags` attribute.<br /><br /> Specifies the options for directory listings.<br /><br /> -   `LongDate:`<br />     - Specifies whether to show long dates or short dates.<br />     - The numeric value is 2.<br /><br /> -   `StyleUnix:`<br />     - Specifies whether to display UNIX-style directory listings; otherwise, displays MSDOS-style listings.<br />     - The numeric value is 4.<br /><br /> -   `DisplayAvailableBytes:`<br />     - Specifies whether to display the available bytes in directory listings.<br />     - The numeric value is 16.<br /><br /> -   `DisplayVirtualDirectories:`<br />     - Specifies whether to display virtual directories if set; otherwise, virtual directories are hidden.<br />     - The numeric value is 32.<br /><br /> -   `UseGmtTime:`<br />     - Specifies whether to display dates and times in GMT.<br />     - The numeric value is 64.<br /><br /> There is no default value.|  
|`virtualDirectoryTimeout`|Optional `int` attribute.<br /><br /> Specifies the maximum amount of time the FTP service will use to retrieve the timestamp information for virtual directories. If threshold is reached, or `virtualDirectoryTimeout` is set to 0, then the current date will be used instead.<br /><br /> The default value is 5.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level FTP server settings.|  
  
## Remarks  
 For more information about the `directoryBrowse` element, see the following topic on the Microsoft IIS.net Web site: [FTP Directory Browse \<directoryBrowse>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/directoryBrowse).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)