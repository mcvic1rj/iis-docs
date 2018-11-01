---
title: "configHistory Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7a651775-d0c5-4a87-ada7-cae1b48f9d0e
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# configHistory Element
> [!NOTE]
>  For more information about the `configHistory` element, see the following topic on the Microsoft IIS.net Web site: [Configuration History \<configHistory>](http://www.iis.net/ConfigReference/system.applicationHost/configHistory).  
  
 Configures settings for returning to a well-known configuration state.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether the configuration history feature is enabled or disabled. If this attribute is `true,` the ApplicationHost Helper Service checks for changes in the ApplicationHost.config file by using the time interval specified by the `period` attribute. If the configuration changes and is still valid, the helper service saves the ApplicationHost.config file in a versioned subdirectory inside the directory specified by the `path` attribute.<br /><br /> The default value is `true`.|  
|`maxHistories`|Optional `int` attribute.<br /><br /> Specifies the maximum number of history directories to store. The history directory with the lowest version number will be deleted if the maximum is reached.<br /><br /> The default value is 10.|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the path of the directory that contains the configuration history subdirectories.. **Note:**  The ApplicationHost Helper Service saves one copy of the ApplicationHost.config file in each configuration history subdirectory. The configuration history subdirectories have the naming format CFGHISTORY_\<serial number>. The serial number is a 10-digit sequential number (zero padded). <br /><br /> The default value is *%SYSTEMDRIVE%\inetpub\history*.|  
|`period`|Optional `timeSpan` attribute.<br /><br /> Specifies the interval at which the ApplicationHost Helper Service checks for changes in the ApplicationHost.config file. If the configuration changes and is still valid, the helper service saves the files in the directory specified by the `path` attribute.<br /><br /> The default value is 00:02:00 (2 minutes).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 The configuration history feature enables you to go back to a former configuration state if you no longer want the current state.  
  
 For more information about the `configHistory` element, see the following topic on the Microsoft IIS.net Web site: [Configuration History \<configHistory>](http://www.iis.net/ConfigReference/system.applicationHost/configHistory).  
  
 The ApplicationHost Helper Service enables the configuration history functionality by saving the ApplicationHost.config file to separate configuration history subdirectories at set intervals specified by the `period` attribute. The subdirectories reside in the directory specified by the `path` attribute.  
  
 If you make a mistake when you modify the ApplicationHost.config file, you can restore an earlier version of the file from a configuration history subdirectory by copying the earlier version into the *%windir%*\system32\inetsrv\config directory.  
  
> [!NOTE]
>  The configuration history files do not require separate access control list (ACL) configuration. They inherit their ACL values from the parent directory, to which only administrators have access.  
  
 The configuration history feature depends on the ApplicationHost Helper Service. The ApplicationHost Helper Service is a runtime-independent service that does not require the Windows Process Activation Service (WAS) or the World Wide Web Publishing Service (WWW service) to operate. It does not depend on any other service and its startup type is `Automatic`.  
  
> [!NOTE]
>  If the ApplicationHost Helper Service is stopped, the configuration history feature will not work.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [ConfigurationHistorySection Class](../../reference/admin/configurationhistorysection-class.md)