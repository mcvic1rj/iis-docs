---
title: "add Element for handlers | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: be08f045-74d7-45cf-b013-a667ad8a4a5b
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# add Element for handlers
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Handlers \<add>](http://www.iis.net/ConfigReference/system.webServer/handlers/add).  
  
 Specifies a handler to be added to the `handlers` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowPathInfo`|Optional `Boolean` attribute.<br /><br /> Specifies whether the handler processes full path information in a URI, such as contoso/marketing/imageGallery.aspx. If the value is `true`, the handler processes the full path, contoso/marketing/imageGallery. If the value is `false`, the handler processes only the last section of the path, /imageGallery.<br /><br /> The default value is `false`.|  
|`modules`|Optional `string` attribute.<br /><br /> Specifies the name of the module or modules to which you want to map the file name or file name with extension. If you specify more than one value, separate the values with a comma (,).<br /><br /> The default value is `ManagedPipelineHandler`.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of the handler mapping.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the file name extension or the file name with extension for which the handler mapping applies.|  
|`preCondition`|Optional `string` attribute.<br /><br /> Specifies conditions under which the handler will run.<br /><br /> The `preCondition` attribute can be one or more of the following possible values. If you specify more than one value, separate the values with a comma (,).<br /><br /> `bitness32`:<br /><br /> - Specify the `bitness32` value when the handler is a 32-bit .dll file, and IIS should load the handler only for worker processes that run in WOW64 mode (32-bit simulation) on a 64-bit operating system.<br /><br /> `bitness64`:<br /><br /> - Specify the `bitness64` value when the handler is a 64-bit .dll file, and IIS should load the handler only for worker processes that run in 64-bit mode.<br /><br /> `integratedMode`:<br /><br /> - Specify the `integratedMode` value when the handler should respond only to requests in application pools that are configured to use the integrated request-processing pipeline.<br /><br /> `ISAPIMode`:<br /><br /> - Specify the `ISAPIMode` value when the handler should respond only to requests in application pools that are configured to use **Classic** mode.<br /><br /> `runtimeVersionv1.1`:<br /><br /> - Specify the `runtimeVersionv1.1` value when the handler should respond only to requests in application pools that are configured to use .NET Framework version 1.1.<br /><br /> `runtimeVersionv2.0`:<br /><br /> - Specify the `runtimeVersionv2.0` value when the handler should respond only to requests in application pools that are configured to use .NET Framework version 2.0.|  
|`requireAccess`|Optional `enum` attribute.<br /><br /> Specifies the type of access that a handler requires to the resource.<br /><br /> The `requireAccess` attribute can be one or more of the following possible values. If you specify more than one value, separate the values with a comma (,). The default value is `Script`.<br /><br /> `Execute`:<br /><br /> - Specifies that the handler requires rights to run executables.<br /><br /> - The numeric value is 4.<br /><br /> `None`:<br /><br /> - Specifies that the handler does not have access requirements.<br /><br /> - The numeric value is 0.<br /><br /> `Read`:<br /><br /> - Specifies that the handler requires read permissions.<br /><br /> - The numeric value is 1.<br /><br /> `Script`:<br /><br /> - Specifies that the handler requires rights to run scripts.<br /><br /> - The numeric value is 3.<br /><br /> `Write`:<br /><br /> - Specifies that the handler requires write permissions.<br /><br /> - The numeric value is 2.|  
|`resourceType`|Optional `string` attribute.<br /><br /> Specifies the type of resource to which the handler mapping applies.<br /><br /> The `resourceType` attribute can be one of the following possible values. The default value is `Unspecified`.<br /><br /> `Directory`:<br /><br /> - Specifies that the handler mapping applies to requests only for physical folders on disk.<br /><br /> - The numeric value is 1.<br /><br /> `Either`:<br /><br /> - Specifies that the handler mapping applies to requests for physical files or folders on disk.<br /><br /> - The numeric value is 2.<br /><br /> `File`:<br /><br /> - Specifies that the handler mapping applies to requests only for physical files on disk.<br /><br /> - The numeric value is 0.<br /><br /> `Unspecified`:<br /><br /> - Specifies that the mapping type is not specified. The handler mapping applies to requests regardless of whether the request maps to a physical file or folder on disk. Use this setting when you map a handler to a file name or file name with extension that does not exist on disk, such as MyHandler.axd.<br /><br /> - The numeric value is 3.|  
|`responseBufferLimit`|Optional `integer` attribute.<br /><br /> Specifies the maximum size, in bytes, of the response buffer for a request handler.<br /><br /> The default value is 4194304 bytes.|  
|`scriptProcessor`|Optional `string` attribute.<br /><br /> Specifies the physical path of the ISAPI extension .dll file or Common Gateway Interface (CGI) .exe file that processes the request.<br /><br /> The `scriptProcessor` attribute is required only for script map handler mappings. When you map a handler to an ISAPI extension, you must specify ISAPIModule for the `modules` attribute. When you map a handler to a CGI file, you must specify CGIModule for the `modules` attribute.|  
|`type`|Optional `string` attribute.<br /><br /> Specifies the namespace path of a managed handler. The `type` attribute is required only for managed handlers.|  
|`verb`|Required `string` attribute.<br /><br /> Specifies the HTTP verbs for which the handler mapping applies.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`handlers`|Specifies handlers to process requests made to sites and applications.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Handlers \<add>](http://www.iis.net/ConfigReference/system.webServer/handlers/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|