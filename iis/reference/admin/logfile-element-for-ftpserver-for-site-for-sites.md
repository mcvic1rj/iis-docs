---
title: "logFile Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d87c6954-8592-4782-81e6-bd08263fdd28
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# logFile Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `logFile` element, see the following topic on the Microsoft IIS.net Web site: [FTP Log Files \<logFile>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/logFile).  
  
 Configures the activity logging options for an FTP site.  
  
## Syntax  
  
## Attributes and Elements  
 Configure the activity logging options for an FTP site.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the logging directory, where the log file and logging-related support files are stored.<br /><br /> The default value is `%SystemDrive%\inetpub\logs\LogFiles`.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> `true` if logging is enabled; otherwise `false`.<br /><br /> The default value is `true`.|  
|`localTimeRollover`|Optional `Boolean` attribute.<br /><br /> `true` if a new log file is created based on local time; otherwise, `false` for Coordinated Universal Time (UTC), which was previously called Greenwich Mean Time (GMT).<br /><br /> Note:<br /><br /> Regardless of the setting, the time stamp for each W3C Extended Logging log record is UTC-based.<br /><br /> The default value is `false`.|  
|`logExtFileFlags`|Optional `flags` attribute.<br /><br /> Specifies the categories of information that are written to either the log file (when you use W3C Extended log file format) or to the ODBC data source during logging events for a site. The `logExtFileFlags` attribute can be one or more of the following values. If you specify more than one value, separate them with a comma (,).<br /><br /> The default values are Date, Time, `ClientIP`, `UserName`, `ServerIP`, `Method`, `UriStem`, `FtpStatus`, `Win32Status`, `FtpSubStatus`, `ServerPort`, `Session`, and `FullPath`.<br /><br /> `BytesRecv`<br /><br /> - Log the number of bytes that the server received.<br /><br /> - The numeric value is 8192.<br /><br /> `BytesSent`<br /><br /> - Log the number of bytes that the server sent.<br /><br /> - The numeric value is 4096.<br /><br /> `ClientIP`<br /><br /> - Log the IP address of the client that made the request.<br /><br /> - The numeric value is 4.<br /><br /> `ClientPort`<br /><br /> - Log the port of the client that made the request.<br /><br /> - The numeric value is 33554432.<br /><br /> `ComputerName`<br /><br /> - Log the name of the server on which the log file entry was generated.<br /><br /> - The numeric value is 32.<br /><br /> `Date`<br /><br /> - Log the date on which the activity occurred.<br /><br /> - The numeric value is 1.<br /><br /> `FtpStatus`<br /><br /> - Log the FTP status code.<br /><br /> - The numeric value is 1024.<br /><br /> `FtpSubStatus`<br /><br /> - Log the sub-status code of the FTP error.<br /><br /> - The numeric value is 2097152.<br /><br /> `FullPath`<br /><br /> - Log the full relative path. Note: This may be different URI that the client requested, which is logged by setting the `UriStem` flag.<br /><br /> - The numeric value is 8388608.<br /><br /> `Host`<br /><br /> - Log the virtual host name, if there is one.<br /><br /> - The numeric value is 1048576.<br /><br /> `Info`<br /><br /> - Log extended debugging information, if there is any.<br /><br /> - The numeric value is 16777216.<br /><br /> `Method`<br /><br /> - Log the requested action. For example, `USER`, `PASS`, etc.<br /><br /> - The numeric value is 128.<br /><br /> `ServerIP`<br /><br /> - Log the IP address of the server on which the log file entry was generated.<br /><br /> - The numeric value is 64.<br /><br /> `ServerPort`<br /><br /> - Log the server port number that is configured for the site.<br /><br /> - The numeric value is 32768.<br /><br /> `Session`<br /><br /> - Log the unique identifier for the FTP session. This is useful for analyzing session activity in your logs.<br /><br /> - The numeric value is 4194304.<br /><br /> `SiteName`<br /><br /> - Log the Internet service name and instance number for the site.<br /><br /> - The numeric value is 16.<br /><br /> `Time`<br /><br /> - Log the time in Coordinated Universal Time (UTC), at which the activity occurred.<br /><br /> - The numeric value is 2.<br /><br /> `TimeTaken`<br /><br /> - Log the length of time taken for a request to be completed. The time taken is recorded in milliseconds.<br /><br /> - The numeric value is 16384.<br /><br /> `UriStem`<br /><br /> - Log the Universal Resource Identifier (URI) stem information, which is the target of the action. Note: This shows the URI steam exactly as the client requested, which may not be the full relative path. For the full relative path, use the `FullPath` flag.The numeric value is 256.<br /><br /> `UserName`<br /><br /> - Log the name of the authenticated user who accessed your server. Anonymous users are indicated by a hyphen.<br /><br /> - The numeric value is 8.<br /><br /> `Win32Status`<br /><br /> - Log the Windows status code.<br /><br /> - The numeric value is 2048.|  
|`period`|Optional `enum` attribute.<br /><br /> Specifies how often the FTP service creates a new log file. The period attribute can be one of the following possible values.<br /><br /> The default value is `Daily`.<br /><br /> `Daily`<br /><br /> - Create a new log file daily.<br /><br /> - The numeric value is 1.<br /><br /> `Hourly`<br /><br /> - Create a new log file hourly.<br /><br /> - The numeric value is 4.<br /><br /> `MaxSize`<br /><br /> - Create a new log file when a maximum size is reached. The maximum size is specified in the `truncateSize` attribute.<br /><br /> - The numeric value is 0.<br /><br /> `Monthly`<br /><br /> - Create a new log file monthly.<br /><br /> - The numeric value is 3.<br /><br /> `Weekly`<br /><br /> - Create a new log file weekly.<br /><br /> - The numeric value is 2.|  
|`selectiveLogging`|Optional `flags` attribute.<br /><br /> Specifies the verbosity for FTP logging.<br /><br /> The default value is `LogSuccessful`, `LogError`, `LogInfrastructure`.<br /><br /> `LogError`<br /><br /> - Specifies that errors will be logged. The amount of data actually logged also depends on the setting of the `LogInfrastructure` flag.<br /><br /> - The numeric value is 2.<br /><br /> `LogInfrastructure`<br /><br /> - Specifies that all FTP commands and low-level data channel activity will be logged. For example, the logs will contain entries for `DataChannelOpened`, `DataChannelClosed`, `PORT`/`EPRT`, `PASV`/`EPSV`, if the `LogInfrastructure` flag is set.<br /><br /> - The numeric value is 4.<br /><br /> `LogSuccessful`<br /><br /> - Specifies that successful activity will be logged. The amount of data actually logged also depends on the setting of `LogInfrastructure` flag.<br /><br /> - The numeric value is 1.|  
|`truncateSize`|Optional `int64` attribute.<br /><br /> Specifies the maximum size of the log file (in bytes) after which to create a new log file. This value is only applicable when `MaxSize` is chosen for the `period` attribute. The minimum file size is 1,048,576 bytes. If this attribute is set to a value less than 1,048,576 bytes, the default value is implicitly assumed as 1,048,576 bytes.<br /><br /> The default value is 20971520.|  
  
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
 For more information about the `logFile` element, see the following topic on the Microsoft IIS.net Web site: [FTP Log Files \<logFile>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/logFile).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)