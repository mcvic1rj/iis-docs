---
title: "asp Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2a9b9077-9d51-40dc-9591-facba938b1f0
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# asp Element
> [!NOTE]
>  For more information about the `asp` element, see the following topic on the Microsoft IIS.net Web site: [ASP \<asp>](http://www.iis.net/ConfigReference/system.webServer/asp).  
  
 Configures settings for Active Server Pages (ASP) applications.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`appAllowClientDebug`|Optional `Boolean` attribute.<br /><br /> Specifies whether client-side debugging is enabled.<br /><br /> The default value is `false`.|  
|`appAllowDebugging`|Optional `Boolean` attribute.<br /><br /> Specifies whether server-side debugging is enabled.<br /><br /> The default value is `false`.|  
|`bufferingOn`|Optional `Boolean` attribute.<br /><br /> Specifies whether buffering of ASP application output is enabled.<br /><br /> The default value is `true`.|  
|`calcLineNumber`|Optional `Boolean` attribute.<br /><br /> Specifies whether ASP calculates and stores the line number of each executed line of code in order to provide the number in an error report.<br /><br /> The default value is `true`.|  
|`codePage`|Optional `integer` attribute.<br /><br /> Specifies the default character set for an ASP application. This value is an integer in the range from 0 to 2147483647. For example, the value 1252 sets the default character set to a Latin character set used in American English and many European alphabets.<br /><br /> The default value is 0.|  
|`enableApplicationRestart`|Optional `Boolean` attribute.<br /><br /> Specifies whether ASP applications are automatically restarted whenever a configuration setting is changed.<br /><br /> The default value is `true`.|  
|`enableAspHtmlFallback`|Optional `Boolean` attribute.<br /><br /> Specifies whether a .htm file with the same name as the requested .asp file, if it exists, will be sent to the client instead of the .asp file. This will occur in the event that the request is rejected due to a full request queue.<br /><br /> The default value is `true`.|  
|`enableChunkedEncoding`|Optional `Boolean` attribute.<br /><br /> Specifies whether HTTP 1.1 chunked transfer encoding is enabled.<br /><br /> The default value is `true`.|  
|`enableParentPaths`|Optional `Boolean` attribute.<br /><br /> Specifies whether ASP pages allow paths relative to the current directory or above the current directory.<br /><br /> The default value is `false`.|  
|`errorsToNTLog`|Optional `Boolean` attribute.<br /><br /> Specifies whether logging of ASP errors to the Windows Event Log is enabled.<br /><br /> The default value is `false`.|  
|`exceptionCatchEnable`|Optional `Boolean` attribute.<br /><br /> Specifies whether COM component exception trapping is enabled. If set to `false`, the Microsoft Script Debugger tool does not catch exceptions sent by the component that you are debugging.<br /><br /> The default value is `true`.|  
|`lcid`|Optional `integer` attribute.<br /><br /> Specifies the default locale identifier for an ASP application. This value is an integer in the range from 0 to 2147483647.<br /><br /> The default value is 0.|  
|`logErrorRequests`|Optional `Boolean` attribute.<br /><br /> Specifies whether ASP errors are written to the client browser and the IIS logs by default.<br /><br /> The default value is `true`.|  
|`runOnEndAnonymously`|Optional `Boolean` attribute.<br /><br /> Specifies whether `SessionOnEnd` and `ApplicationOnEnd` global ASP functions are run as the anonymous user.<br /><br /> The default value is `true`.|  
|`scriptErrorMessage`|Optional `string` attribute.<br /><br /> Specifies the error message that will be sent to the browser when specific debugging errors are not sent to the client.<br /><br /> The default value is "An error occurred on the server when processing the URL. Please contact the system administrator".|  
|`scriptErrorSentToBrowser`|Optional `Boolean` attribute.<br /><br /> Specifies whether the writing of debugging specifics to the client browser is enabled.<br /><br /> The default value is `false`.|  
|`scriptLanguage`|Optional `string` attribute.<br /><br /> Specifies the default script language for all ASP applications running on the Web server.<br /><br /> The default value is `VBScript`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`comPlus`|Optional element.<br /><br /> Specifies COM+ settings.|  
|`cache`|Optional element.<br /><br /> Specifies ASP cache settings.|  
|`limits`|Optional element.<br /><br /> Specifies limits for various ASP properties.|  
|`session`|Optional element.<br /><br /> Specifies ASP session state settings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `asp` element, see the following topic on the Microsoft IIS.net Web site: [ASP \<asp>](http://www.iis.net/ConfigReference/system.webServer/asp).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<comPlus>](../../reference/admin/complus-element-for-asp.md)   
 [\<cache>](../../reference/admin/cache-element-for-asp.md)   
 [\<limits>](../../reference/admin/limits-element-for-asp.md)   
 [\<session>](../../reference/admin/session-element-for-asp.md)