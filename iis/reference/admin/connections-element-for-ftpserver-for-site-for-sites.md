---
title: "connections Element for ftpServer for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 01ce9335-5bc0-4d9f-ae6a-9f2e31598933
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# connections Element for ftpServer for site for sites
> [!NOTE]
>  For more information about the `connections` element, see the following topic on the Microsoft IIS.net Web site: [FTP Connections \<connections>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/connections).  
  
 Specifies the connection-related settings for FTP sites.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`controlChannelTimeout`|Optional `int` attribute.<br /><br /> Specifies the timeout, in seconds, when a connection will be timed out because of inactivity on the control channel. **Note:**  The FTP service will disconnect the session when this timeout is reached. <br /><br /> The default value is 120.|  
|`dataChannelTimeout`|Optional `int` attribute.<br /><br /> Specifies the timeout, in seconds, when a connection will be timed out because of inactivity on the data channel. **Note:**  The FTP service will only disconnect the data channel when this timeout is reached. <br /><br /> The default value is 30.|  
|`disableSocketPooling`|Optional `Boolean` attribute.<br /><br /> `true` if socket pooling is disabled; otherwise, `false`.<br /><br /> The `disableSocketPooling` attribute specifies whether socket pooling is used for sites that are distinguished by IP address rather than port number or host name. If `disableSocketPooling` is set to `false`, then socket pooling is enabled and sockets are shared between sites that use the same socket number but different IP addresses. In this situation, the FTP service becomes the exclusive owner of the port on each address that is bound to the server. For example, if socket pooling is enabled on a server that has two IP addresses, 10.0.0.1 and 10.0.0.2, and an FTP site is bound to address 10.0.0.1 on port 21, the FTP service will also own port 21 on the 10.0.0.2 address. If `disableSocketPooling` is set to `true`, then there is no socket sharing for sites based on IP address.<br /><br /> The default value is `false`.|  
|`maxBandwidth`|Unused uint attribute. **Note:**  This attribute is not implemented for FTP 7.|  
|`maxConnections`|Optional `unit` attribute.<br /><br /> Specifies the maximum number of simultaneous connections for an FTP site. **Note:**  Use the `maxClientsMessage` attribute of the messages element to specify a message that the FTP service will return to clients when the maximum number of simultaneous connections has been exceeded. <br /><br /> The default value is `4294967295` (unlimited.)|  
|`minBytesPerSecond`|Optional `int` attribute.<br /><br /> Specifies the minimum bandwidth requirements for data transfers. **Note:**  The FTP service will disconnect the data channel when the minimum bandwidth is not met. <br /><br /> The default value is `240`.|  
|`resetOnMaxConnections`|Optional `Boolean` attribute.<br /><br /> `true` if the FTP service should quickly disconnect an FTP session instead of sending a maximum connections response; otherwise `false`. **Note:**  The `resetOnMaxConnections` attribute optimizes the overhead when processing connections that are not allowed to connect because `maxConnection` limit was reached. <br /><br /> The default value is `false`.|  
|`serverListenBacklog`|Optional `int` attribute.<br /><br /> Specifies the number of outstanding sockets that can be queued.<br /><br /> The default value is `60`.|  
|`unauthenticatedTimeout`|Optional `int` attribute.<br /><br /> Specifies the idle time-out, in seconds, between when a new connection is made and authentication succeeds. If the client does not successfully authenticate within the specified time period, the FTP service will disconnect the session.<br /><br /> The default value is `30`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Defines all sites on the server, and all applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
|`ftpServer`|Specifies the site-level settings for FTP features for FTP sites.|  
  
## Remarks  
 For more information about the `connections` element, see the following topic on the Microsoft IIS.net Web site: [FTP Connections \<connections>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/ftpServer/connections).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<ftpServer>](../../reference/admin/ftpserver-element-for-site-for-sites.md)