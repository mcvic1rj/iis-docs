---
title: "error Element for httpErrors | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2f7d8339-1ead-43eb-9aa1-12ec56e4bae6
caps.latest.revision: 25
author: "shirhatti"
manager: "wpickett"
---
# error Element for httpErrors
> [!NOTE]
>  For more information about the `error` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Errors \<error>](http://www.iis.net/ConfigReference/system.webServer/httpErrors/error).  
  
 Adds an HTTP error to the collection of HTTP errors.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`path`|Required `string` attribute.<br /><br /> Specifies the file path or URL that is served in response to the HTTP error specified by the `statusCode` and `subStatusCode` attributes. If you choose the **File** response mode**,** you specify the path of the custom error page. If you choose the **ExecuteURL** response mode, the path has to be a server relative URL (for example, /404.htm). If you choose the **Redirect** response mode, you have to enter an absolute URL (for example, www.contoso.com/404.htm).|  
|`prefixLanguageFilePath`|Optional `string` attribute.<br /><br /> Specifies the initial path segment when generating the path for a custom error. This segment appears before the language-specific portion of the custom error path. For example, in the path c:\inetpub\custerr\en-us\404.htm, "c:\inetpub\custerr" is the `prefixLanguageFilePath`.|  
|`responseMode`|Optional `enum` attribute.<br /><br /> Specifies how custom error content is returned.<br /><br /> The `responseMode` attribute can be one of the following possible values. The default is **File**.<br /><br /> `File`: Serves static content, for example, a .html file for the custom error. If `responseMode` is set to `File`, the `path` attribute value has to be a file path. The numeric value is 0.<br /><br /> `ExecuteURL`: Serves dynamic content (for example, an .asp file) specified in the `path` attribute for the custom error. If `responseMode` is set to `ExecuteURL`, the path value has to be a server relative URL. The numeric value is 1.<br /><br /> `Redirect`: Redirects client browsers to a the URL specified in the `path` attribute that contains the custom error file. If `responseMode` is set to `Redirect`, the path value has to be an absolute URL. The numeric value is 2.|  
|`statusCode`|Required `integer` attribute.<br /><br /> Specifies the number of the HTTP status code for which you want to create a custom error message. Acceptable values are from 400 through 999.|  
|`subStatusCode`|Optional `integer` attribute.<br /><br /> Specifies the number of the HTTP substatus code for which you want to create a custom error message. Acceptable values are from -1 through 999.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpErrors`|Configures HTTP error messages for a Web server.|  
  
## Remarks  
 For more information about the `error` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Errors \<error>](http://www.iis.net/ConfigReference/system.webServer/httpErrors/error).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-httperrors.md)   
 [\<clear>](../../reference/admin/clear-element-for-httperrors.md)