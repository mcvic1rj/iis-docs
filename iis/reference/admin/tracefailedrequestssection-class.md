---
title: "TraceFailedRequestsSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6730e6f8-fff8-8e3b-b50c-42e67b9cec62
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# TraceFailedRequestsSection Class
Represents a failed-request tracing configuration section.  
  
## Syntax  
  
```vbs  
class TraceFailedRequestsSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `TraceFailedRequestsSection` class.  
  
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
 The following table lists the properties exposed by the `TraceFailedRequestsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`TraceFailedRequests`|A read/write array of [TraceUrl](../../reference/admin/traceurl-class.md) values that configure the tracing for specific request types (for example, *.aspx).|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class corresponds to the `<traceFailedRequests>` section in ApplicationHost.config.  
  
## Example  
 The following example lists the `Location`, `Path`, and `TraceFailedRequest` properties for the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Place the TraceFailedRequestsSection object into a variable by  
' using the GetSection method on the Site object.  
oSite.GetSection "TraceFailedRequestsSection", oTFRSection  
  
' Echo the path and location information.  
WScript.Echo "Path: " & oTFRSection.Path  
WScript.Echo "Location: " & oTFRSection.Location  
WScript.Echo vbCRLF  
  
' Retrieve and display the values for the TraceFailedRequests property.  
For Each oTFR In oTFRSection.TraceFailedRequests  
    WScript.Echo "Trace URL path: " & oTFR.Path  
    WScript.Echo String(16 + Len(oTFR.Path), "=")  
  
    Set oFD = oTFR.FailureDefinitions  
    WScript.Echo "Failure Definition Status Codes: " & oFD.StatusCodes  
    WScript.Echo "Failure Definition TimeTaken: " & oFD.TimeTaken  
    WScript.Echo "Failure Definition Verbosity Level: " & _  
            GetVerbosityText(oFD.Verbosity)  
    WScript.Echo   
  
    For Each oTA In oTFR.TraceAreas.TraceAreas  
        WScript.Echo "Trace Provider: " & oTA.Provider  
        WScript.Echo "Trace Verbosity Level: " & _  
            GetVerbosityText(oTA.Verbosity)  
        If Not (oTA.Provider = "ASP" Or _  
                oTA.Provider = "ISAPI Extension") Then  
            WScript.Echo "Trace Areas: " & oTA.Areas  
        End If  
        WScript.Echo   
    Next  
    WScript.Echo  
Next  
  
' Provide text for the verbosity enumeration values.  
Function GetVerbosityText(sint32Value)  
    Select Case sint32Value  
        Case 0  
            GetVerbosityText="General"  
        Case 1  
            GetVerbosityText="Critical Error"  
        Case 2  
            GetVerbosityText="Error"  
        Case 3  
            GetVerbosityText="Warning"  
        Case 4  
            GetVerbosityText="Information"  
        Case 5  
            GetVerbosityText="Verbose"  
        Case Else  
            GetVerbosityText ="Undefined Verbosity Level"  
    End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `TraceFailedRequestsSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [HttpTracingSection Class](../../reference/admin/httptracingsection-class.md)   
 [TraceAreaElement Class](../../reference/admin/traceareaelement-class.md)   
 [TraceAreaDefinition Class](../../reference/admin/traceareadefinition-class.md)   
 [TraceProviderDefinition Class](../../reference/admin/traceproviderdefinition-class.md)   
 [TraceProviderDefinitionsSection Class](../../reference/admin/traceproviderdefinitionssection-class.md)   
 [TraceUrl Class](../../reference/admin/traceurl-class.md)   
 [TraceUrlAreaSettings Class](../../reference/admin/traceurlareasettings-class.md)   
 [Create a Tracing Rule for Failed Requests](http://go.microsoft.com/fwlink/?LinkId=64723)