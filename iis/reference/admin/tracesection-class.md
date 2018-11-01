---
title: "TraceSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c6205ff6-062d-7f7a-98a3-2df6a50bc47b
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# TraceSection Class
Configures the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] code-tracing service.  
  
## Syntax  
  
```vbs  
class TraceSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `TraceSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `TraceSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Enabled`|An optional read/write `boolean` value. `true` if tracing is enabled for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application; otherwise, `false`. The default is `false`.<br /><br /> When tracing is enabled, you can view the logged errors with the Trace.axd viewer at the URL http://*\<servername>*/*\<applicationroot>*/trace.axd. You must set the `Enabled` property to `true` to use the viewer. **Note:**  Trace.axd is added to the `<``httpHandlers``>` section in the Applicationhost.config file by default.|  
|`LocalOnly`|An optional read/write `boolean` value. `true` if the trace viewer (Trace.axd) is available only on the host Web server; `false` if the trace viewer is available from any computer. The default is `true`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`MostRecent`|An optional read/write `boolean` value. `true` if the trace store continues to collect the most recent trace messages and begins to discard older trace messages when the limit specified in `RequestLimit` is reached; `false` if the trace store stops collecting trace messages when the number specified in `RequestLimit` is reached. The default is `false`. **Note:**  This property is new in the [!INCLUDE[dnprdnlong](../../reference/admin/includes/dnprdnlong-md.md)].|  
|`PageOutput`|An optional read/write `boolean` value. `true` if tracing information is added to the bottom of each Web page; `false` if trace output is accessible through the trace utility only. The default is `false`. **Note:**  For more information about the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] trace viewer utility, see [How to: View ASP.NET Trace Information with the Trace Viewer](http://go.microsoft.com/fwlink/?LinkId=73542).|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`RequestLimit`|An optional read/write `sint32` value that specifies the number of trace requests, from 0 through 10000, to store on the server. The default is 10. If the limit is reached and the `MostRecent` property is `false`, tracing stops. **Note:**  Although integer values in the range 0 to 2147483647 are accepted for the `RequestLimit` property, if you specify a value greater than 10000, [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] silently rounds it down to 10000.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`TraceMode`|An optional read/write `sint32` value that specifies the order in which trace information is displayed. The possible values are listed later in the Remarks section.|  
|`WriteToDiagnosticsTrace`|An optional read/write `boolean` value. `true` if [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] trace messages are forwarded to the [System.Diagnostics](http://go.microsoft.com/fwlink/?LinkId=73540) tracing infrastructure for listeners that are registered to display trace messages; otherwise, `false`. The default is `false`. **Note:**  This property is new in the [!INCLUDE[dnprdnlong](../../reference/admin/includes/dnprdnlong-md.md)].|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table lists the possible values for the `TraceMode` property. The default is 1 (`SortByTime`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|1|`SortByTime`|Specifies that trace information is displayed in the order that it is processed.|  
|2|`SortByCategory`|Specifies that trace information is displayed alphabetically by user-defined categories specified in the <xref:System.Web.TraceContext.Warn%2A?displayProperty=fullName> and <xref:System.Web.TraceContext.Write%2A?displayProperty=fullName> method calls in page or server control code.|  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `TraceSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.TraceContext?displayProperty=fullName>   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [trace Element (ASP.NET Settings Schema)](http://go.microsoft.com/fwlink/?LinkId=67200)   
 [How to: Enable Tracing for an ASP.NET Page](http://go.microsoft.com/fwlink/?LinkId=67201)   
 [System.Web.TraceContext Methods](http://go.microsoft.com/fwlink/?LinkId=67202)