---
title: "SystemDiagnosticsSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d7245c41-accd-e0ea-162b-412d8c1cdd33
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# SystemDiagnosticsSection Class
Configures system diagnostics and tracing.  
  
## Syntax  
  
```vbs  
class SystemDiagnosticsSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `SystemDiagnosticsSection` class.  
  
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
 The following table lists the properties exposed by the `SystemDiagnosticsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Assert`|An [AssertSettings](../../reference/admin/assertsettings-class.md) value that specifies the user-interface mode for the [System.Diagnostics.Debug.Assert](http://go.microsoft.com/fwlink/?LinkId=70960) method and the name of a message log file.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`PerformanceCounters`|A [PerformanceCounterSettings](../../reference/admin/performancecountersettings-class.md) value that specifies the size of the global memory shared by performance counters.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`SharedListeners`|A [ListenerSettings](../../reference/admin/listenersettings-class.md) value that contains listeners that any source or trace element can reference.|  
|`Sources`|A [SourceSettings](../../reference/admin/sourcesettings-class.md) value that specifies trace sources that initiate tracing messages.|  
|`Switches`|A [SwitchSettings](../../reference/admin/switchsettings-class.md) value that contains trace switch definitions.|  
|`Trace`|A [TraceSettings](../../reference/admin/tracesettings-class.md) value that contains listeners that collect, store, and route tracing messages.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `SystemDiagnosticsSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AssertSettings Class](../../reference/admin/assertsettings-class.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ListenerSettings Class](../../reference/admin/listenersettings-class.md)   
 [PerformanceCounterSettings Class](../../reference/admin/performancecountersettings-class.md)   
 [SourceSettings Class](../../reference/admin/sourcesettings-class.md)   
 [SwitchSettings Class](../../reference/admin/switchsettings-class.md)   
 [TraceSettings Class](../../reference/admin/tracesettings-class.md)   
 [System.Diagnostics.Debug.Assert Method](http://go.microsoft.com/fwlink/?LinkId=70960)