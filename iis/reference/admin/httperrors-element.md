---
title: "httpErrors Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 62391f4e-acfe-4429-9c89-fd7991daf80a
caps.latest.revision: 37
author: "shirhatti"
manager: "wpickett"
---
# httpErrors Element
> [!NOTE]
>  For more information about the `httpErrors` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
 Configures HTTP error messages for a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultPath`|Optional `string` attribute.<br /><br /> Specifies the default path of the custom error page. The type of path is determined by the `defaultResponseMode` attribute. If you choose `File`, the file path is returned**.** If you choose either the `ExecuteURL` or `Redirect` path type, the URL of the custom error page is returned.|  
|`defaultResponseMode`|Optional `enum` attribute.<br /><br /> Specifies how custom error content is returned.<br /><br /> The `defaultResponseMode` attribute can be one of the following possible values. The default is `File`.<br /><br /> `File`:<br /><br /> - Serves static content, for example, a .html file for the custom error. If `responseMode` is set to `File`, the path value has to be a file path. The numeric value is 0.<br /><br /> `ExecuteURL`:<br /><br /> - Serves dynamic content, for example, a .asp file for the custom error. If `responseMode` is set to `ExecuteURL`, the path value has to be a server relative URL. The numeric value is 1.<br /><br /> `Redirect`:<br /><br /> - Redirects client browsers to a different URL that contains the custom error file. If `responseMode` is set to `Redirect`, the path value has to be an absolute URL. The numeric value is 2.|  
|`detailedMoreInformationLink`|Optional `string` attribute.<br /><br /> Specifies a link, shown at the bottom of the page, to a page with more detailed information about a particular error. You can use this property to point end users to a custom location for error information. The status, sub-status, hresult and message ID are sent as part of the query string.<br /><br /> The default value is "http://go.microsoft.com/fwlink/?LinkID=62293".|  
|`errorMode`|Optional `enum` attribute.<br /><br /> Specifies whether HTTP errors are enabled.<br /><br /> The `errorMode` attribute can be one of the following values. The default is `DetailedLocalOnly`.<br /><br /> `DetailedLocalOnly`:<br /><br /> - Returns detailed error information if the request is from the local computer, and returns a custom error message if the request is from an external computer. The numeric value is 0.<br /><br /> `Custom`:<br /><br /> - Replaces the error that the module or server generates with a custom page that you specify. This mode is useful in providing friendlier error messages to end users. The numeric value is 1.<br /><br /> - Note: This setting turns off detailed errors, even for local requests.<br /><br /> `Detailed`:<br /><br /> - Sends detailed error information back to the client. This mode is useful for testing and debugging Web sites and applications. The numeric value is 2.|  
|`existingResponse`|Optional `enum` attribute.<br /><br /> Specifies what happens to an existing response when the HTTP status code is an error, i.e. response codes >= 400.<br /><br /> `Auto`:<br /><br /> - Leaves the response untouched only if the `SetStatus` flag is set. The numeric value is 0.<br /><br /> `Replace`:<br /><br /> - Replaces the existing response even if the `SetStatus` flag is set. The numeric value is 1.<br /><br /> `PassThrough`:<br /><br /> - Leaves the response untouched if an existing response exists. The numeric value is 2.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`error`|Optional element.<br /><br /> Adds an HTTP error to the collection of HTTP errors.|  
|`remove`|Optional element.<br /><br /> Removes a reference to an HTTP error from the HTTP error collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to HTTP errors from the HTTP error collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpErrors` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<error>](../../reference/admin/error-element-for-httperrors.md)