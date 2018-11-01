---
title: "log Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e58875a8-96a8-4b58-ba5f-16d0db370e6c
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# log Element for system.ftpServer
> [!NOTE]
>  For more information about the `log` element, see the following topic on the Microsoft IIS.net Web site: [FTP Logging Options \<log>](http://www.iis.net/ConfigReference/system.ftpServer/log).  
  
 Specifies log settings for an FTP server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`centralLogFileMode`|Optional `enum` attribute.<br /><br /> Specifies the central logging mode for the FTP server.<br /><br /> The `centralLogFileMode` attribute can be one of the following possible values.<br /><br /> The default value is `Site`.<br /><br /> `Site`:<br /><br /> - Specifies that each site will write to individual log files on the FTP server.<br /><br /> - The numeric value is 0.<br /><br /> `Central`:<br /><br /> - Specifies that a single log file will be maintained for all the sites on the FTP server.<br /><br /> - The numeric value is 1.|  
|`logInUTF8`|Optional `Boolean` attribute.<br /><br /> Specifies whether IIS should log all strings for the FTP server in UCS Transformation Format 8 (UTF-8). This setting applies to text-mode logging for all of the sites on the FTP server.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`centralLogFile`|Optional element.<br /><br /> Specifies the settings for the central log file.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
  
## Remarks  
 For more information about the `log` element, see the following topic on the Microsoft IIS.net Web site: [FTP Logging Options \<log>](http://www.iis.net/ConfigReference/system.ftpServer/log).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<centralLogFile>](../../reference/admin/centrallogfile-element-for-log-for-system-ftpserver.md)