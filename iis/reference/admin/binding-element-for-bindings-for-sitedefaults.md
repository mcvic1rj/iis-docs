---
title: "binding Element for bindings for siteDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a28f48f4-96a5-4b07-b536-4667f269a1fd
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# binding Element for bindings for siteDefaults
> [!NOTE]
>  For more information about the `binding` element, see the following topic on the Microsoft IIS.net Web site: [Adding a Default Binding \<binding>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/bindings/binding).  
  
 Configures a default binding for all sites on the server.  
  
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
|`siteDefaults`|Specifies default settings for all sites on the server.|  
|`bindings`|Specifies the default bindings to access all sites on the server.|  
  
## Remarks  
 For more information about the `binding` element, see the following topic on the Microsoft IIS.net Web site: [Adding a Default Binding \<binding>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/bindings/binding).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|