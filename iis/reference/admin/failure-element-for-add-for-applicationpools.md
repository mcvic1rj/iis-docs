---
title: "failure Element for add for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 49fe6b49-f2d0-4e4a-8440-60bad7ee53c7
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# failure Element for add for applicationPools
> [!NOTE]
>  For more information about the `failure` element, see the following topic on the Microsoft IIS.net Web site: [Failure Settings for an Application Pool \<failure>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/failure).  
  
 Defines the actions to take when an application pool fails.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`autoShutdownExe`|Optional `string` attribute.<br /><br /> Specifies an executable to run when the WWW service shuts down an application pool. You can use the `autoShutdownParams` attribute to send parameters to the executable.|  
|`autoShutdownParams`|Optional `string` attribute.<br /><br /> Specifies command-line parameters for the executable that is specified in the `autoShutdownExe` attribute.|  
|`loadBalancerCapabilities`|Optional `enum` attribute.<br /><br /> Specifies behavior when a worker process cannot be started, such as when the request queue is full or an application pool is in rapid-fail protection. The `loadBalancerCapabilities` attribute can be one of the following possible values. The default value is `HttpLevel`.<br /><br /> -   `HttpLevel:`<br />     - Specifies that a 503 error code has been returned. Load balancers that are not HTTP aware will not switch to a different node because the 503 response tells the load balancer that the computer is healthy.                       The numeric value is 2.<br /><br /> -   `TcpLevel:`<br />     -              Specifies that the TCP connection will terminate. This is useful when you use a load balancer that is not HTTP aware.                       The numeric value is 1.|  
|`orphanActionExe`|Optional `string` attribute.<br /><br /> Specifies an executable to run when the WWW service orphans a worker process (if the `orphanWorkerProcess` attribute is set to `true`). You can use the `orphanActionParams` attribute to send parameters to the executable.|  
|`orphanActionParams`|Optional `string` attribute.<br /><br /> Indicates command-line parameters for the executable named by the `orphanActionExe` attribute. To specify the process ID of the orphaned process, use %1%.|  
|`orphanWorkerProcess`|Optional `Boolean` attribute.<br /><br /> Specifies whether to assign a worker process to an orphan state instead of terminating it when an application pool fails.<br /><br /> The default value is `false`.|  
|`rapidFailProtection`|Optional `Boolean` attribute.<br /><br /> Setting to `true` instructs the WWW service to remove from service all applications that are in an application pool when:<br /><br /> The number of worker process crashes has reached the maximum specified in the `rapidFailProtectionMaxCrashes` attribute.<br /><br /> The crashes occur within the number of minutes specified in the `rapidFailProtectionInterva`l attribute.<br /><br /> The default value is `true`.|  
|`rapidFailProtectionInterval`|Optional `timeSpan` attribute.<br /><br /> Specifies the number of minutes before the failure count for a process is reset.<br /><br /> The default value is `00:05:00` (five minutes).|  
|`rapidFailProtectionMaxCrashes`|Optional `uint` attribute.<br /><br /> Specifies the maximum number of failures allowed within the number of minutes specified by the `rapidFailProtectionInterval` attribute.<br /><br /> The default value is 5.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Contains default configuration settings for all application pools on the server and defines configuration settings for specific application pools.|  
|`add`|Configures an application pool in the server configuration.|  
  
## Remarks  
 For more information about the `failure` element, see the following topic on the Microsoft IIS.net Web site: [Failure Settings for an Application Pool \<failure>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/failure).  
  
 This element can be declared in ApplicationHost.config only. Any attempt to declare it in a configuration file at a different level in the hierarchy causes an error and a resultant error message.  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|