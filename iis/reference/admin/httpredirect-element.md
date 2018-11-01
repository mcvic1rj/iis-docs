---
title: "httpRedirect Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f8503f11-6932-4da0-86f1-ad4cd3a7d924
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# httpRedirect Element
> [!NOTE]
>  For more information about the `httpRedirect` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Redirects \<httpRedirect>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect).  
  
 Configures settings for redirecting client requests to a new location.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`childOnly`|Optional `Boolean` attribute.<br /><br /> Specifies whether the `destination` value should be added to the beginning of the file name that contains the request to be redirected. For example, if `childOnly` were set to `true` and the destination value were configured to be http://marking.contoso.com/, a request for http://contoso.com/default.htm would be redirected to http://marketing.contoso.com/default.htm.<br /><br /> The default value is `false`.|  
|`destination`|Optional `string` attribute.<br /><br /> Specifies a URL or virtual path to which to redirect the client.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether redirection is enabled (`true`) or disabled (`false`).<br /><br /> The default value is `false`.|  
|`exactDestination`|Optional `Boolean` attribute.<br /><br /> Specifies that the `destination` value should be considered an absolute target location, not a relative location.<br /><br /> The default value is `false`.|  
|`httpResponseStatus`|Optional `enum` attribute.<br /><br /> Specifies type of redirection.<br /><br /> The `httpResponseStatus` attribute can be one of the following possible values. The default is `Found`.<br /><br /> `Found`:<br /><br /> - Returns a 302 status code, which tells the client to issue a new request to the location specified in the `destination` attribute.<br /><br /> - The numeric value is 302.<br /><br /> `Permanent`:<br /><br /> - Returns a 301 status code, which informs the client that the location for the requested resource has permanently changed.<br /><br /> - The numeric value is 301.<br /><br /> `Temporary`:<br /><br /> - Returns a 307 status code, which prevents the client from losing data when the browser issues an HTTP POST request.<br /><br /> - The numeric value is 307.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a wildcard redirection rule to the collection of redirection rules.|  
|`clear`|Optional element.<br /><br /> Removes all references to wildcard redirection rules from the collection of redirection rules.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a wildcard redirection rule from the collection of redirection rules.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpRedirect` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Redirects \<httpRedirect>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-httpredirect.md)   
 [\<remove>](../../reference/admin/remove-element-for-httpredirect.md)   
 [\<clear>](../../reference/admin/clear-element-for-httpredirect.md)