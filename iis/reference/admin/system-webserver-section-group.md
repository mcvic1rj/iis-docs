---
title: "system.webServer Section Group | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0afddb04-cb47-4981-859c-9846d826a473
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# system.webServer Section Group
> [!NOTE]
>  For more information about the `system.webServer` element, see the following topic on the Microsoft IIS.net Web site: [\<system.webServer>](http://www.iis.net/ConfigReference/system.webServer).  
  
 Specifies the root element for the [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] configuration section and contains configuration elements that configure settings used by the Web server engine and modules.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`asp`|Optional element.<br /><br /> Configures settings for Active Server Pages (ASP) applications.|  
|`caching`|Optional element.<br /><br /> Configures output cache settings.|  
|`cgi`|Optional element.<br /><br /> Configures default settings for Common Gateway Interface (CGI) applications.|  
|`defaultDocument`|Optional element.<br /><br /> Configures settings for returning a default document to a client browser when the client does not specify a file name in a request.|  
|`directoryBrowse`|Optional element.<br /><br /> Configures whether directory browsing is enabled or disabled on the Web server, and specifies the information to include in a directory listing.|  
|`fastCgi`|Optional element.<br /><br /> Contains a collection of fastCgi application pool definitions.|  
|`globalModules`|Optional element.<br /><br /> Specifies configuration settings for global modules on a Web server.|  
|`handlers`|Optional element.<br /><br /> Specifies handlers to process requests made to sites and applications.|  
|`httpCompression`|Optional element.<br /><br /> Configures HTTP compression settings for a Web server.|  
|`httpErrors`|Optional element.<br /><br /> Configures HTTP error messages for a Web server.|  
|`httpLogging`|Optional element.<br /><br /> Specifies configuration settings for HTTP.sys logging.|  
|`httpProtocol`|Optional element.<br /><br /> Configures custom and redirect response headers to be sent from the server to the client.|  
|`httpRedirect`|Optional element.<br /><br /> Configures settings for redirecting client requests to a new location.|  
|`httpTracing`|Optional element.<br /><br /> Specifies configuration settings for HTTP.sys tracing.|  
|`isapiFilters`|Optional element.<br /><br /> Specifies configuration settings for ISAPI filters on a Web server.|  
|`management`|Optional element.<br /><br /> Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`modules`|Optional element.<br /><br /> Specifies configuration settings for modules on a Web server.|  
|`odbcLogging`|Optional element.<br /><br /> Configures Open Database Connectivity (ODBC) logging.|  
|`security`|Optional element.<br /><br /> Specifies the section group that contains security-related sections.|  
|`serverRuntime`|Optional element.<br /><br /> Configures request limits for applications on a Web server.|  
|`serverSideIncludes`|Optional element.<br /><br /> Specifies whether server-side includes (SSI) `#exec` directives are disabled.|  
|`staticContent`|Optional element.<br /><br /> Configures static file request handler settings.|  
|`tracing`|Optional element.<br /><br /> Configures request trace settings.|  
|`urlCompression`|Optional element.<br /><br /> Configures compression of static and dynamic content.|  
|`validation`|Optional element.<br /><br /> Configures IIS 7.0 to detect whether an ASP.NET application that is set up to run in ISAPI mode needs any migration in order to function correctly in Integrated mode.|  
|`webdav`|Optional Element.<br /><br /> Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `system.webServer` element, see the following topic on the Microsoft IIS.net Web site: [\<system.webServer>](http://www.iis.net/ConfigReference/system.webServer).  
  
## See Also  
 [\<asp>](../../reference/admin/asp-element.md)   
 [\<caching>](../../reference/admin/caching-element.md)   
 [\<cgi>](../../reference/admin/cgi-element.md)   
 [\<defaultDocument>](../../reference/admin/defaultdocument-element.md)   
 [IIS 7.0: directoryBrowse Element for ftpServer for siteDefaults for sites (IIS Settings Schema)](http://msdn.microsoft.com/en-us/d711798f-995f-4785-8767-1ceec301f0ab)   
 [\<fastCgi>](../../reference/admin/fastcgi-element.md)   
 [\<globalModules>](../../reference/admin/globalmodules-element.md)   
 [\<handlers>](../../reference/admin/handlers-element.md)   
 [\<httpCompression>](../../reference/admin/httpcompression-element.md)   
 [\<httpErrors>](../../reference/admin/httperrors-element.md)   
 [\<httpLogging>](../../reference/admin/httplogging-element.md)   
 [\<httpProtocol>](../../reference/admin/httpprotocol-element.md)   
 [\<httpRedirect>](../../reference/admin/httpredirect-element.md)   
 [\<httpTracing>](../../reference/admin/httptracing-element.md)   
 [\<isapiFilters>](../../reference/admin/isapifilters-element.md)   
 [\<management>](../../reference/admin/management-element.md)   
 [\<modules>](../../reference/admin/modules-element.md)   
 [\<odbcLogging>](../../reference/admin/odbclogging-element.md)   
 [IIS 7.0: security Element for ftpServer for siteDefaults for sites (IIS Settings Schema)](http://msdn.microsoft.com/en-us/e9c14c98-fa0f-4533-a1a5-86b0294f31f6)   
 [\<serverRuntime>](../../reference/admin/serverruntime-element.md)   
 [\<serverSideInclude>](../../reference/admin/serversideinclude-element.md)   
 [\<staticContent>](../../reference/admin/staticcontent-element.md)   
 [\<tracing>](../../reference/admin/tracing-element.md)   
 [\<urlCompression>](../../reference/admin/urlcompression-element.md)   
 [\<validation>](../../reference/admin/validation-element.md)   
 [\<webdav>](../../reference/admin/webdav-element.md)