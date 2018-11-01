---
title: "directoryBrowse Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a3fc2dd9-1874-4015-ac36-a1bba6409714
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# directoryBrowse Element
> [!NOTE]
>  For more information about the `directoryBrowse` element, see the following topic on the Microsoft IIS.net Web site: [Directory Browse \<directoryBrowse>](http://www.iis.net/ConfigReference/system.webServer/directoryBrowse).  
  
 Configures whether directory browsing is enabled or disabled on the Web server, and specifies the information to include in a directory listing.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether directory browsing is enabled (`true`) or disabled (`false`) on the Web server.<br /><br /> The default value is `false`.|  
|`showFlags`|Optional `flags` attribute.<br /><br /> The `showFlags` attribute can have one or more of the following possible values. If you specify more than one value, separate the values with a comma (,). The default values are `Date, Time, Size, Extension`.<br /><br /> `Date`:<br /><br /> - Includes the last modified date for a file or directory in a directory listing.<br /><br /> `Extension`:<br /><br /> - Includes a file name extension for a file in a directory listing.<br /><br /> `LongDate`:<br /><br /> - Includes the last modified date in extended format for a file in a directory listing.<br /><br /> `None`:<br /><br /> - Specifies that only the file or directory names are returned in a directory listing.<br /><br /> `Size`:<br /><br /> - Includes the file size for a file in a directory listing.<br /><br /> `Time`:<br /><br /> - Includes the last modified time for a file or directory in a directory listing.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
  
## Remarks  
 For more information about the `directoryBrowse` element, see the following topic on the Microsoft IIS.net Web site: [Directory Browse \<directoryBrowse>](http://www.iis.net/ConfigReference/system.webServer/directoryBrowse).  
  
## Default Configuration  
 The following default `<directoryBrowse>` element is configured in the root ApplicationHost.config file in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] when the Directory Browsing role service is installed.  
  
```  
<directoryBrowse enabled="false" />  
```  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|