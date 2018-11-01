---
title: "SettingsSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 437b7c23-a582-c80c-c23d-15610b504be2
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# SettingsSection Class
Contains settings that specify how the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] connects to the network.  
  
## Syntax  
  
```vbs  
class SettingsSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `SettingsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `SettingsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`HttpWebRequest`|An [HttpWebRequestSettings](../../reference/admin/httpwebrequestsettings-class.md) value that customizes Web request parameters.|  
|`Ipv6`|An [Ipv6Settings](../../reference/admin/ipv6settings-class.md) value that specifies whether members of the [System.Net.Dns](http://go.microsoft.com/fwlink/?LinkId=70922) class return Internet Protocol version 6 (IPv6) addresses.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`PerformanceCounters`|A [PerformanceCountersSettings](../../reference/admin/performancecounterssettings-class.md) value that enables or disables network performance counters.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`ServicePointManager`|A [ServicePointManagerSettings](../../reference/admin/servicepointmanagersettings-class.md) value that configures connections to network resources.|  
|`Socket`|A [SocketSettings](../../reference/admin/socketsettings-class.md) value that specifies whether socket operations use completion ports.|  
|`WebProxyScript`|A [WebProxyScriptSettings](../../reference/admin/webproxyscriptsettings-class.md) value that configures the characteristics of the script that is used to discover Web proxies.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `SettingsSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [HttpWebRequestSettings Class](../../reference/admin/httpwebrequestsettings-class.md)   
 [Ipv6Settings Class](../../reference/admin/ipv6settings-class.md)   
 [PerformanceCountersSettings Class](../../reference/admin/performancecounterssettings-class.md)   
 [ServicePointManagerSettings Class](../../reference/admin/servicepointmanagersettings-class.md)   
 [SocketSettings Class](../../reference/admin/socketsettings-class.md)   
 [WebProxyScriptSettings Class](../../reference/admin/webproxyscriptsettings-class.md)   
 [System.Net.Dns Class](http://go.microsoft.com/fwlink/?LinkId=70922)