---
title: "TraceAreaDefinition Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2e7a5f92-c545-bddf-e717-433ae9baa574
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# TraceAreaDefinition Class
Specifies trace area names and their corresponding enumeration values for a trace provider.  
  
## Syntax  
  
```vbs  
class TraceAreaDefinition : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `TraceAreaDefinition` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Name`|A required unique read/write `string` value that specifies the name of the trace area. The key property.|  
|`Value`|A read/write `uint32` value that maps to a trace area or areas. You can define one or more trace areas by specifying the flag number. The possible values are listed later in the Remarks section.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Areas` array property of the [TraceAreaSettings](../../reference/admin/traceareasettings-class.md) class.  
  
 The failed-request tracing feature of [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] uses the `TraceAreaDefinition` class. The property values of this class map to the same values for the areas used by the Event Tracing for Windows (ETW) providers. Trace areas are defined by default for the "WWW Server" and "ASPNET" trace providers in the ApplicationHost.config file.  
  
 The following table lists the possible values for the `Value` property.  
  
|Value|Keyword|  
|-----------|-------------|  
|2|`Authentication`|  
|4|`Security`|  
|8|`Filter`|  
|16|`StaticFile`|  
|32|`CGI`|  
|64|`Compression`|  
|128|`Cache`|  
|256|`RequestNotifications`|  
|512|`Module`|  
  
> [!NOTE]
>  There is no `UrlFilter` area as there is in ETW for Windows Server 2003 SP1.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `TraceAreaDefinition`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [Create a Tracing Rule for Failed Requests](http://go.microsoft.com/fwlink/?LinkId=64723)   
 [FailureDefinition Class](../../reference/admin/failuredefinition-class.md)   
 [HttpTracingSection Class](../../reference/admin/httptracingsection-class.md)   
 [TraceAreaElement Class](../../reference/admin/traceareaelement-class.md)   
 [TraceAreaSettings Class](../../reference/admin/traceareasettings-class.md)   
 [TraceFailedRequestsSection Class](../../reference/admin/tracefailedrequestssection-class.md)   
 [TraceProviderDefinition Class](../../reference/admin/traceproviderdefinition-class.md)   
 [TraceProviderDefinitionsSection Class](../../reference/admin/traceproviderdefinitionssection-class.md)   
 [TraceUrl Class](../../reference/admin/traceurl-class.md)