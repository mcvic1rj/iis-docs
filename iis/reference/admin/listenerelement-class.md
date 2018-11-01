---
title: "ListenerElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1d144054-260c-f615-00c8-76b5a51166bd
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# ListenerElement Class
Contains a listener that monitors and formats trace output.  
  
## Syntax  
  
```vbs  
class ListenerElement : TypedElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ListenerElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Filter`|A [TypedElement](../../reference/admin/typedelement-class.md) value that filters the trace output.|  
|`InitializeData`|(Inherited from `TypedElement`.)|  
|`Name`|A required unique read/write `string` value that contains the name of the listener. The key property.|  
|`TraceOutputOptions`|A read/write `sint32` value that specifies the kind of trace event data that is returned from a thread and a process. The possible values are listed later in the Remarks section.|  
|`Type`|(Inherited from `TypedElement`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `SharedListeners` array property of the [ListenerSettings](../../reference/admin/listenersettings-class.md) class and in the `Listeners` array property of the [SourceListenerSettings](../../reference/admin/sourcelistenersettings-class.md) class.  
  
 The following table lists the possible values for the `TraceOutputOptions` property. The default is 0 (`None`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`None`|No trace data is returned.|  
|1|`LogicalOperationStack`|Returns stack data that correlates thread-bound logical operation identities with their trace events.|  
|2|`DateTime`|Returns the date and time at which the event trace occurred.|  
|4|`Timestamp`|Returns the current number of ticks in the timer mechanism.|  
|8|`ProcessId`|Returns the unique identifier of the current process.|  
|16|`ThreadId`|Returns a unique identifier for the current managed thread.|  
|32|`Callstack`|Returns a string that contains trace information that lists the method calls on the stack. The most recent call is listed first.|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 [TypedElement](../../reference/admin/typedelement-class.md)  
  
 `ListenerElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [ListenerSettings Class](../../reference/admin/listenersettings-class.md)   
 [SourceListenerSettings Class](../../reference/admin/sourcelistenersettings-class.md)   
 [TypedElement Class](../../reference/admin/typedelement-class.md)   
 [System.Diagnostics.TraceEventCache Properties](http://go.microsoft.com/fwlink/?LinkId=71875)