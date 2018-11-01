---
title: "add Element for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f4dafa20-eecb-447e-9961-cf53017f1b6c
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# add Element for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Failed Requests \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add).  
  
 Adds a path to the collection of path definitions for failure tracing.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`customActionExe`|Optional `string` attribute.<br /><br /> Specifies an executable file to run when a failure condition is reached (for example, to run a VBScript file, specify "cscript.exe"). All command-line variables will be expanded. For example, "%windir%" will be expanded to the path of the Windows directory.|  
|`customActionParams`|Optional `string` attribute.<br /><br /> Contains parameters to pass to the executable file specified in the `customActionExe` attribute. Command-line variables such as "%windir%" will be expanded. You may also use parameter variables such as "%1" and "%2" in the string that you specify (for example, "MyScript.vbs %1 %2").|  
|`customActionTriggerLimit`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of times the program specified by the `customActionExe` attribute will execute during the lifetime of the worker process for the failed-request definition. This value resets every time that the worker process recycles. Permissible values are from 0 through 10000. The default is 1. This feature can be used, for example, to create a memory dump after the next failure but not after subsequent failures. **Note:**  If the `CustomActionTriggerLimit` value that you specify is reached during the run time of the worker process, subsequent failed requests will be logged, but the program specified in CustomActionExe will not run. The entries in the failed-requests log will indicate that the CustomActionTriggerLimit value has been reached.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the path for which you want to log trace events. The path is relative to the URL (virtual directory/directory). Sub paths cannot be used. In addition, the path must be local to the directory where the definition is set. Wildcard values can be used, for example, "*.aspx". For tracing the default document, use "/" as the path value.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`traceAreas`|Required element.<br /><br /> Configures what to trace for a given path.|  
|`failureDefinitions`|Required element.<br /><br /> Defines the conditions in which to save traces for a request.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceFailedRequests`|Contains settings for tracing failed requests on the Web server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Failed Requests \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-tracefailedrequests-for-tracing.md)   
 [\<traceAreas>](../../reference/admin/traceareas-element-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<failureDefinitions>](../../reference/admin/failuredefinitions-element-for-add-for-tracefailedrequests-for-tracing.md)