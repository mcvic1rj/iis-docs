---
title: "staticContent Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3c9cc94d-6577-4518-8e33-988bc00787b0
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# staticContent Element
> [!NOTE]
>  For more information about the `staticContent` element, see the following topic on the Microsoft IIS.net Web site: [Static Content \<staticContent>](http://www.iis.net/ConfigReference/system.webServer/staticContent).  
  
 Configures static file request handler settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultDocFooter`|Optional `string` attribute.<br /><br /> Specifies either the default footer text for every Web page on a site, or the path of a file that contains the default footer text. How this property is read depends on the setting of the `isDocFooterFileName` attribute. **Note:**  The custom footer will only be sent if the `enableDocFooter` attribute is set to `true`.|  
|`enableDocFooter`|Optional `Boolean` attribute.<br /><br /> Specifies whether the text indicated by the `defaultDocFooter` attribute will appear on every static page on a Web site.<br /><br /> The default value is `false`.|  
|`isDocFooterFileName`|Optional `Boolean` attribute.<br /><br /> Specifies whether the string in the `defaultDocFooter` attribute contains a path of a file that contains the default footer text for every static Web page on a site.<br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`clientCache`|Optional element.<br /><br /> Specifies settings for caching static content that is sent to the client.|  
|`mimeMaps`|Optional element.<br /><br /> Specifies a list of the file name extensions for MIME mappings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `staticContent` element, see the following topic on the Microsoft IIS.net Web site: [Static Content \<staticContent>](http://www.iis.net/ConfigReference/system.webServer/staticContent).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<clientCache>](../../reference/admin/clientcache-element-for-staticcontent.md)   
 [\<mimeMap>](../../reference/admin/mimemap-element-for-staticcontent.md)