---
title: "processModel Element for add for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1ceb31f5-a5d9-4013-b676-bd14890acfb8
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# processModel Element for add for applicationPools
> [!NOTE]
>  For more information about the `processModel` element, see the following topic on the Microsoft IIS.net Web site: [Process Model Settings for an Application Pool \<processModel>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/processModel).  
  
 Configures the process model settings for an application pool.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`identityType`|Optional `enum` attribute.<br /><br /> Specifies the account identity under which the application pool runs.<br /><br /> The `identityType` attribute can be one of the following possible values. The default is `NetworkService`.<br /><br /> -   `ApplicationPoolIdentity:`<br />     - Specifies that the application pool runs under the dynamically-created application pool identity account. Starting in IIS 7.5, ApplicationPoolIdentity is the default identity under which to run application pools. (In IIS 7.0 the default identity was NetworkService.)When an application pool runs under the ApplicationPoolIdentity account, the application pool accesses resources as the "IIS AppPool\\<AppPool\>" identity. For example, for the "DefaultAppPool", the identity is "IIS AppPool\DefaultAppPool". This identity allows administrators to specify permissions that pertain only to the identity under which the application pool is running, thereby increasing server security.<br />     - The numeric value is 4.<br /><br /> -   `LocalService:`<br />     - Specifies that the application pool runs under the built-in `LocalService` account, which has the same user rights as `NetworkService`.<br />     - When an application pool runs under the `LocalService` account, the application pool presents anonymous credentials on the network.<br />     - The numeric value is 1.<br /><br /> -   `LocalSystem:`<br />     - Running an application pool under an account that has high-level user rights is a serious security risk.<br />     - The numeric value is 0.<br /><br /> -   `NetworkService:`<br />     - Specifies that the application pool runs under the built-in `NetworkService` account. This is the default built-in account under which to run application pools.<br />     - When an application pool runs under the `NetworkService` account, the application pool accesses network resources as the computer account.<br />     - The numeric value is 2.<br /><br /> -   `SpecificUser:`<br />     - Specifies that the application pool runs under a custom identity, which is configured by using the `userName` and `password` attributes.<br />     - To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.<br />     - The numeric value is 3.|  
|`idleTimeout`|Optional `timeSpan` attribute.<br /><br /> Specifies how long (in minutes) a worker process should run idle if no new requests are received and the worker process is not processing requests. After the allocated time passes, the worker process should request that it be shut down by the WWW service.<br /><br /> The default value is `00:20:00`.|  
|`loadUserProfile`|Optional `Boolean` attribute.<br /><br /> Specifies whether IIS loads the user profile for the application pool identity. Setting this value to `false` causes IIS to revert to IIS 6.0 behavior. IIS 6.0 does not load the user profile for an application pool identity.<br /><br /> The default value is `true`.|  
|`logonType`|Optional enum attribute.Specifies the logon type for the process identity. (For additional information about logon types, see the [LogonUser Function](http://msdn.microsoft.com/en-us/library/aa378184\(VS.85\).aspx) topic on the Microsoft MSDN Web site.)<br /><br /> This attribute was introduced in IIS 7.5.<br /><br /> The `logonType` attribute can be one of the following possible values; the default is `LogonBatch`.<br /><br /> -   `LogonBatch:`<br />     - Specifies that the application pool identity should logon as a batch user.The numeric value is 0.<br /><br /> -   `LogonService:`<br />     - Specifies that the application pool identity should logon as a service.The numeric value is 1.|  
|`manualGroupMembership`|Optional `Boolean` attribute.<br /><br /> Specifies whether the IIS_IUSRS group Security Identifier (SID) is added to the worker process token. When `false`, IIS automatically uses an application pool identity as though it were a member of the built-in IIS_IUSRS group, which has access to necessary file and system resources. When `true`, an application pool identity must be explicitly added to all resources that a worker process requires at runtime.<br /><br /> The default value is `false`.|  
|`maxProcesses`|Optional `uint` attribute.<br /><br /> Specifies the number of worker processes associated with the application pool. A value other than `1` indicates a Web garden.<br /><br /> The default value is `1`.|  
|`password`|Optional `string` attribute.<br /><br /> Specifies the password associated with the `userName` attribute. This attribute is only necessary when the value of `identityType` is `SpecificUser`.<br /><br /> To avoid storing unencrypted password strings in configuration files, always use Appcmd.exe or [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords.|  
|`pingingEnabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether pinging is enabled for the worker process.<br /><br /> The default value is `true`.|  
|`pingInterval`|Optional `timeSpan` attribute.<br /><br /> Specifies the time between health-monitoring pings that the WWW service sends to a worker process.<br /><br /> The default value is `00:00:30` (30 seconds).|  
|`pingResponseTime`|Optional `timeSpan` attribute.<br /><br /> Specifies the time that a worker process is given to respond to a health-monitoring ping. After the time limit is exceeded, the WWW service terminates the worker process.<br /><br /> The default value is `00:01:30` (1 minute 30 seconds).|  
|`shutdownTimeLimit`|Optional `timeSpan` attribute.<br /><br /> Specifies the time that the W3SVC service waits after it initiated a recycle. If the worker process does not shut down within the `shutdownTimeLimit`, it will be terminated by the W3SVC service.<br /><br /> The default value is `00:01:30` (1 minute 30 seconds).|  
|`startupTimeLimit`|Optional `timeSpan` attribute.<br /><br /> Specifies the time that IIS waits for an application pool to start. If the application pool does not startup within the `startupTimeLimit`, the worker process is terminated and the rapid-fail protection count is incremented.<br /><br /> The default value is `00:01:30` (1 minute 30 seconds).|  
|`userName`|Optional `string` attribute.<br /><br /> Specifies the identity under which the application pool runs when the `identityType` is `SpecificUser`.|  
  
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
 For more information about the `processModel` element, see the following topic on the Microsoft IIS.net Web site: [Process Model Settings for an Application Pool \<processModel>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add/processModel).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
|**IIS 7.5**|The \<processModel> element of the \<add> element was updated in IIS 7.5 to include settings that allow you run applications using the new ApplicationPoolIdentity and to specify the login type for the process identity.|