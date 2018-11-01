---
title: "odbcLogging Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1de03a6b-8e49-48b2-84aa-09db34d2e2ee
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# odbcLogging Element
> [!NOTE]
>  For more information about the `odbcLogging` element, see the following topic on the Microsoft IIS.net Web site: [ODBC Logging \<odbcLogging>](http://www.iis.net/ConfigReference/system.webServer/odbcLogging).  
  
 Configures Open Database Connectivity (ODBC) logging.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`dataSource`|Optional `string` attribute.<br /><br /> Specifies the system DSN (data source name) for the database to which the log is written.<br /><br /> The default value is "InternetDb".|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the ODBC database password that you use when you write information to the database during event logging. By default, this value is encrypted.<br /><br /> The default value is "[enc:AesProvider::enc]".|  
|`tableName`|Optional `string` attribute.<br /><br /> Specifies the name of the ODBC database table where Windows writes information during event logging.<br /><br /> The default value is "InternetLog".|  
|`userName`|Optional `string` attribute.<br /><br /> Specifies the ODBC database user name that is used for writing information to the database during event logging.<br /><br /> The default value is "InternetAdmin".|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `odbcLogging` element, see the following topic on the Microsoft IIS.net Web site: [ODBC Logging \<odbcLogging>](http://www.iis.net/ConfigReference/system.webServer/odbcLogging).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|