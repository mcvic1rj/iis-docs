---
title: "AspSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ec1156b1-7d9c-443f-2f75-f9a96f33ea5a
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# AspSection Class1
Exposes Active Server Pages (ASP) configuration settings for ASP applications.  
  
## Syntax  
  
```vbs  
class AspSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `AspSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `AspSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AppAllowClientDebug`|A read/write `boolean` value. `true` if ASP client-side debugging is `enabled`; otherwise, `false`. The default is `false`.|  
|`AppAllowDebugging`|A read/write `boolean` value. `true` if ASP debugging is enabled on the server; otherwise, `false`. The default is `false`.|  
|`BufferingOn`|A read/write `boolean` value. `true` if the output from an ASP application will be buffered; otherwise, `false`. The default is `true`.|  
|`Cache`|A read/write [AspCache](../../reference/admin/aspcache-class.md) value that configures ASP caching.|  
|`CalcLineNumber`|A read/write `boolean` value. `true` if ASP should calculate and store the line number of each executed line of code in order to provide the number in an error report; otherwise, `false`. The default is `true`.|  
|`CodePage`|A read/write `uint32` value that specifies the code page for the application. The default is 0.|  
|`ComPlus`|A read/write [AspComPlus](../../reference/admin/aspcomplus-class.md) value that configures properties related to COM+.|  
|`EnableApplicationRestart`|A read/write `boolean` value. `true` if the ASP application can automatically be restarted; otherwise, `false`. The default is `true`.|  
|`EnableAspHtmlFallback`|A read/write `boolean` value. `true` if an .htm file with a similar name as the requested .asp file is sent in response to a new request when the request queue is already full; otherwise, `false`. The default is `true`. The naming convention for the .htm file is the name of the .asp file with "_asp" appended. For example, if the .asp file is "hello.asp", the .htm file should be "hello_asp.htm."|  
|`EnableChunkedEncoding`|A read/write `boolean` value. `true` if HTTP 1.1 chunked transfer encoding is enabled for the World Wide Web Publishing Service (WWW service); otherwise, `false`. The default is `true`.|  
|`EnableParentPaths`|A read/write `boolean` value. `true` if an ASP page allows paths above the current directory; `false` if only paths relative to the current directory are allowed. The default is `false`.|  
|`ErrorsToNTLog`|A read/write `boolean` value. `true` if ASP errors are written to the Windows event log; otherwise, `false`. The default is `false`. **Note:**  By default, ASP errors are written to the client browser and to the IIS log files.|  
|`ExceptionCatchEnable`|A read/write `boolean` value. `true` if ASP pages catch component exceptions that can be caught by the Microsoft Script Debugger tool; otherwise, `false`. The default is `true`.|  
|`Lcid`|A read/write `uint32` value that specifies the default locale identifier for an application. The default is 0.|  
|`Limits`|A read/write [AspLimits](../../reference/admin/asplimits-class.md) value that configures properties related to ASP limits.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`LogErrorRequests`|A read/write `boolean` value. `true` if the Web server writes ASP errors to the application section of the Windows event log; otherwise, `false`. The default is `true`.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`RunOnEndAnonymously`|A read/write `boolean` value. `true` if the `SessionOnEnd` and `ApplicationOnEnd` global ASP functions should be run as the anonymous user; otherwise, `false`. The default is `true`.|  
|`ScriptErrorMessage`|A read/write `string` value that contains the error message sent to the browser if specific debugging errors are not sent to the client. The default is "An error occurred on the server when processing the URL. Please contact the system administrator."|  
|`ScriptErrorSentToBrowser`|A read/write `boolean` value. `true` if the Web server writes debugging specifics (file name, error, line number, description) to the client browser in addition to logging them to the Windows event log; otherwise, `false`. The default is `false`.|  
|`ScriptLanguage`|A read/write `string` value that specifies the default script language for all ASP applications running on the Web server. The default is "VBScript".|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`Session`|A read/write [AspSession](../../reference/admin/aspsession-class.md) value that configures properties related to ASP sessions.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `AspSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AspCache Class](../../reference/admin/aspcache-class.md)   
 [AspComPlus Class](../../reference/admin/aspcomplus-class.md)   
 [AspLimits Class](../../reference/admin/asplimits-class.md)   
 [AspSession Class](../../reference/admin/aspsession-class.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)