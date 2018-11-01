---
title: "HealthMonitoringSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8fd30064-d022-b1a0-6011-75b020d101dd
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# HealthMonitoringSection Class
Configures an application for health monitoring.  
  
## Syntax  
  
```vbs  
class HealthMonitoringSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `HealthMonitoringSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|(Inherited from [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md).)|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `HealthMonitoringSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`BufferModes`|A [BufferModeSettings](../../reference/admin/buffermodesettings-class.md) value that configures the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] event-buffering settings for event providers.|  
|`Enabled`|A read/write `boolean` value. `true` if health monitoring is enabled for the Web application; otherwise, `false`. The default is `true`.|  
|`EventMappings`|A [EventMappingSettings](../../reference/admin/eventmappingsettings-class.md) value that maps friendly event names to related event types.|  
|`HeartbeatInterval`|A read/write `datetime` value that specifies the interval between <xref:System.Web.Management.WebHeartbeatEvent> events. The default is 0, which indicates that no `WebHeartbeatEvent` event is raised.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Profiles`|A [ProfileSettings](../../reference/admin/profilesettings-class.md) value that specifies event profiles that determine how events are collected by [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and raised to providers.|  
|`Providers`|A [ProviderSettings](../../reference/admin/providersettings-class.md) value that specifies the names and types of health monitoring providers that process events.|  
|`Rules`|A [RuleSettings](../../reference/admin/rulesettings-class.md) value that maps events to health monitoring providers.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `HealthMonitoringSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Management.WebHeartbeatEvent>   
 [BufferModeSettings Class](../../reference/admin/buffermodesettings-class.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [EventMappingSettings Class](../../reference/admin/eventmappingsettings-class.md)   
 [ProfileSettings Class](../../reference/admin/profilesettings-class.md)   
 [ProviderSettings Class](../../reference/admin/providersettings-class.md)   
 [RuleSettings Class](../../reference/admin/rulesettings-class.md)   
 [ASP.NET Health Monitoring Overview](http://go.microsoft.com/fwlink/?LinkId=69306)   
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)