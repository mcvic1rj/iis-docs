---
title: "defaultDocument Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4a2c5b13-6f70-494b-8e99-4634d58e562b
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# defaultDocument Element
> [!NOTE]
>  For more information about the `defaultDocument` element, see the following topic on the Microsoft IIS.net Web site: [Default Document \<defaultDocument>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument).  
  
 Configures settings for returning a default document to a client browser when the client does not specify a file name in a request.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies that default documents are enabled.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`files`|Optional element.<br /><br /> Specifies a list of file names that can be returned as default documents.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
  
## Remarks  
 For more information about the `defaultDocument` element, see the following topic on the Microsoft IIS.net Web site: [Default Document \<defaultDocument>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument).  
  
## Default Configuration  
 The following default `<defaultDocuments>` element is configured in the root ApplicationHost.config file in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] when the Default Document role service is installed. This configuration section inherits the default configuration settings unless you use the `<clear>` element.  
  
```  
<defaultDocument enabled="true">  
   <files>  
      <add value="Default.htm" />  
      <add value="Default.asp" />  
      <add value="index.htm" />  
      <add value="index.html" />  
      <add value="iisstart.htm" />  
      <add value="default.aspx" />  
   </files>  
</defaultDocument>  
```  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<files>](../../reference/admin/files-element-for-defaultdocument.md)