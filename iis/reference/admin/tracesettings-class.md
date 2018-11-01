---
title: "TraceSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 306c9960-18bb-2003-fda6-2b9a04206f6a
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# TraceSettings Class
Configures the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] trace functionality and controls how trace results are gathered, stored, and displayed.  
  
## Syntax  
  
```vbs  
class TraceSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `TraceSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AutoFlush`|A read/write `boolean` value. `true` if the trace listeners automatically flush the output buffer after every write operation; otherwise, `false`. The default is `false`. **Note:**  When the `AutoFlush` property is set to `true`, the trace listener writes to the file regardless of whether the [System.Diagnostics.Trace.Flush](http://go.microsoft.com/fwlink/?LinkId=71872) method is called.|  
|`IndentSize`|A read/write `sint32` value that specifies the number of spaces to indent when the [System.Diagnostics.Trace.Indent](http://go.microsoft.com/fwlink/?LinkId=71871) method is called. The default is 4. **Note:**  A [System.Diagnostics.TextWriterTraceListener](http://go.microsoft.com/fwlink/?LinkId=26061) interprets this number as spaces. An [EventLogTraceListener](http://go.microsoft.com/fwlink/?LinkId=71873) ignores this value. This property is stored on per-thread, per-request basis.|  
|`Listeners`|A [TraceListenerSettings](../../reference/admin/tracelistenersettings-class.md) value that contains listeners that monitor and format trace output.|  
|`UseGlobalLock`|A read/write `boolean` value. `true` if the global lock will be used; otherwise, `false`. The default is `true`. **Note:**  The global lock is always used if the trace listener is not thread safe, regardless of the value of `UseGlobalLock`. The [System.Diagnostics.TraceListener.IsThreadSafe](http://go.microsoft.com/fwlink/?LinkId=74329) property determines whether the listener is thread safe. The global lock is not used only if the value of `UseGlobalLock` is `false` and the value of `IsThreadSafe` is `true`. The default behavior is to use the global lock.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Trace` property of the [SystemDiagnosticsSection](../../reference/admin/systemdiagnosticssection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `TraceSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [SystemDiagnosticsSection Class](../../reference/admin/systemdiagnosticssection-class.md)   
 [TraceListenerSettings Class](../../reference/admin/tracelistenersettings-class.md)   
 [System.Diagnostics.Trace.Indent Method](http://go.microsoft.com/fwlink/?LinkId=71871)   
 [System.Diagnostics.Trace.Flush Method](http://go.microsoft.com/fwlink/?LinkId=71872)   
 [System.Diagnostics.TextWriterTraceListener Class](http://go.microsoft.com/fwlink/?LinkId=26061)   
 [System.Diagnostics.EventLogTraceListener Class](http://go.microsoft.com/fwlink/?LinkId=71873)   
 [System.Diagnostics.TraceListener.IsThreadSafe Property](http://go.microsoft.com/fwlink/?LinkId=74329)