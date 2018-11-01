---
title: "activeDirectory Element for userIsolation for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9d9b93c1-817f-4c5f-942f-85448c90745f
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# activeDirectory Element for userIsolation for ftpServer for site for sites
> [!NOTE]
>  For more information about the `activeDirectory` element, see the following topic on the Microsoft IIS.net Web site: FTP [Active Directory User Isolation \<activeDirectory>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/userIsolation/activeDirectory).  
  
 Specifies the credentials and connection time-out for communicating with an Active Directory server for FTP user isolation.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`adCacheRefresh`|Optional `timeSpan` attribute.<br /><br /> Specifies the time span to cache active directory information.<br /><br /> The default value is 00:01:00.|  
|`adPassword`|Optional encrypted `string` attribute.<br /><br /> Specifies the user password for the connection to the active directory server.<br /><br /> There is no default value.|  
|`adUserName`|Optional `string` attribute.<br /><br /> Specifies the user name for the connection to the active directory server.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|This element is used to start or restrict FTP clients in specific sections of an FTP site.|  
|`userIsolation`|This element is used to start or restrict FTP clients in specific sections of an FTP site.|  
  
## Remarks  
 For more information about the `activeDirectory` element, see the following topic on the Microsoft IIS.net Web site: FTP [Active Directory User Isolation \<activeDirectory>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/userIsolation/activeDirectory).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<userIsolation>](../../reference/admin/userisolation-element-for-ftpserver-for-site-for-sites.md)