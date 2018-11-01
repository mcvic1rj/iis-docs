---
title: "centralLogFile Element for log for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 76580ef8-38df-4b06-a984-df91d0002e60
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# centralLogFile Element for log for system.ftpServer
> [!NOTE]
>  For more information about the `centralLogFile` element, see the following topic on the Microsoft IIS.net Web site: [FTP Central Logging Options \<centralLogFile>](http://www.iis.net/ConfigReference/system.ftpServer/log/centralLogFile).  
  
 Specifies settings for the central log file when the FTP server is configured to use a single log file for all FTP sites.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`directory`|Optional `string` attribute.Specifies the logging directory, where the log file and logging-related support files are stored.<br /><br /> The default value is %SystemDrive%\inetpub\logs\LogFiles.|  
|`enabled`|Optional `Boolean` attribute.`true` if logging is enabled; otherwise `false`.The default value is `true`.|  
|`localTimeRollover`|Optional `Boolean` attribute.<br /><br /> `true` if a new log file is created based on local time; otherwise, `false` for Coordinated Universal Time (UTC), which was previously called Greenwich Mean Time (GMT).<br /><br /> Regardless of the setting, the time stamp for each W3C Extended Logging log record is UTC-based.<br /><br /> The default value is `false`.|  
|`logExtFileFlags`|Optional `flags` attribute.<br /><br /> Specifies the categories of information that are written to either the log file (when you use W3C Extended log file format) or to the ODBC data source during logging events for a site. The `logExtFileFlags` attribute can be one or more of the following values. If you specify more than one value, separate them with a comma (,).<br /><br /> The default values are Date, Time, ClientIP, UserName, ServerIP, Method, UriStem, FtpStatus, Win32Status, FtpSubStatus, ServerPort, Session, and FullPath.<br /><br /> -   `BytesRecv:`<br />     - Log the number of bytes that the server received.The numeric value is 8192.<br /><br /> -   `BytesSent:`<br />     - Log the number of bytes that the server sent.The numeric value is 4096.<br /><br /> -   `ClientIP:`<br />     - Log the IP address of the client that made the request.The numeric value is 4.<br /><br /> -   `ClientPort:`<br />     - Log the port of the client that made the request.The numeric value is 33554432.<br /><br /> -   `ComputerName:`<br />     - Log the name of the server on which the log file entry was generated.The numeric value is 32.<br /><br /> -   `Date:`<br />     - Log the date on which the activity occurred.The numeric value is 1.<br /><br /> -   `FtpStatus:`<br />     - Log the FTP status code.The numeric value is 1024.<br /><br /> -   `FtpSubStatus:`<br />     - Log the sub-status code of the FTP error.The numeric value is 2097152.<br /><br /> -   `FullPath:`<br />     - Log the full relative path. Note: This may be different from the URI that the client requested, which is logged by setting the `UriStem` flag.The numeric value is 8388608.<br /><br /> -   `Host:`<br />     - Log the virtual host name, if there is one.The numeric value is 1048576.<br /><br /> -   `Info:`<br />     - Log extended debugging information, if there is any.The numeric value is 16777216.<br /><br /> -   `Method:`<br />     - Log the requested action. For example, `USER`, `PASS`, etc.The numeric value is 128.<br /><br /> -   `ServerIP:`<br />     - Log the IP address of the server on which the log file entry was generated.The numeric value is 64.<br /><br /> -   `ServerPort:`<br />     - Log the server port number that is configured for the site.The numeric value is 32768.<br /><br /> -   `Session:`<br />     - Log the unique identifier for the FTP session. This is useful for analyzing session activity in your logs.The numeric value is 4194304.<br /><br /> -   `SiteName:`<br />     - Log the Internet service name and instance number for the site.The numeric value is 16.<br /><br /> -   `Time:`<br />     - Log the time in Coordinated Universal Time (UTC), at which the activity occurred.The numeric value is 2.<br /><br /> -   `TimeTaken:`<br />     - Log the length of time taken for a request to be completed. The time taken is recorded in milliseconds.The numeric value is 16384.<br /><br /> -   `UriStem:`<br />     - Log the Universal Resource Identifier (URI) stem information, which is the target of the action. Note: This shows the URI stem exactly as the client requested, which may not be the full relative path. For the full relative path, use the `FullPath` flag.The numeric value is 256.<br /><br /> -   `UserName:`<br />     - Log the name of the authenticated user who accessed your server. Anonymous users are indicated by a hyphen.The numeric value is 8.<br /><br /> -   `Win32Status:`<br />     - Log the Windows status code.The numeric value is 2048.|  
|`Period`|Optional `enum` attribute.Specifies how often the FTP service creates a new log file. The period attribute can be one of the following possible values.The default value is Daily.<br /><br /> -   `Daily:`<br />     - Create a new log file daily.The numeric value is 1.<br /><br /> -   `Hourly:`<br />     - Create a new log file hourly.The numeric value is 4.<br /><br /> -   `MaxSize:`<br />     - Create a new log file when a maximum size is reached. The maximum size is specified in the `truncateSize` attribute.The numeric value is 0.<br /><br /> -   `Monthly:`<br />     - Create a new log file monthly.The numeric value is 3.<br /><br /> -   `Weekly:`<br />     - Create a new log file weekly.The numeric value is 2.|  
|`selectiveLogging`|Optional `flags` attribute.<br /><br /> Specifies the verbosity for FTP logging.<br /><br /> The default value is `LogSuccessful`, `LogError`, `LogInfrastructure`.<br /><br /> -   `LogError:`<br />     - Specifies that errors will be logged. The amount of data actually logged also depends on the setting of `LogInfrastructure` flag.The numeric value is 2.<br /><br /> -   `LogInfrastructure:`<br />     - Specifies that all FTP commands and low-level data channel activity will be logged. For example, if the `LogInfrastructure` flag is set then the logs will contain entries for `DataChannelOpened`, `DataChannelClosed`, `PORT/EPRT`, and `PASV/EPSV`.The numeric value is 4.<br /><br /> -   `LogSuccessful:`<br />     - Specifies that successful activity will be logged. The amount of data actually logged also depends on the setting of `LogInfrastructure` flag.The numeric value is 1.|  
|`TruncateSize`|Optional `int64` attribute.<br /><br /> Specifies the maximum size of the log file (in bytes) after which to create a new log file. This value is only applicable when `MaxSize` is chosen for the period attribute. The minimum file size is 1,048,576 bytes. If this attribute is set to a value less than 1,048,576 bytes, the default value is implicitly assumed as 1,048,576 bytes.<br /><br /> The default value is 20971520.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
|`log`|Specifies the root element for configuring FTP log settings.|  
  
## Remarks  
 For more information about the `centralLogFile` element, see the following topic on the Microsoft IIS.net Web site: [FTP Central Logging Options \<centralLogFile>](http://www.iis.net/ConfigReference/system.ftpServer/log/centralLogFile).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<log>](../../reference/admin/log-element-for-system-ftpserver.md)