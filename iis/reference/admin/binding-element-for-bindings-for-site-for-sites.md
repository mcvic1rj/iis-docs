---
title: "binding Element for bindings for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 97831903-176e-4eca-9d94-0ae778ff1c30
caps.latest.revision: 25
author: "shirhatti"
manager: "wpickett"
---
# binding Element for bindings for site for sites
> [!NOTE]
>  For more information about the `binding` element, see the following topic on the Microsoft IIS.net Web site: [Binding \<binding>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings/binding).  
  
 Configures a binding in the parent site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`bindingInformation`|Required `string` attribute.<br /><br /> Specifies information to communicate with a site. For example, a Web site binding includes the IP address (or unspecified IP addresses), the port number, and an optional host header used to communicate with the site.|  
|`protocol`|Required `string` attribute.<br /><br /> Specifies the protocol for communicating with a site.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`bindings`|Specifies bindings to access the site.|  
  
## Remarks  
 For more information about the `binding` element, see the following topic on the Microsoft IIS.net Web site: [Binding \<binding>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings/binding).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|