---
title: "N - R (IIS 6.0 Metabase Properties Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 30710cee-4256-4db5-a2df-e8701de5b656
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# N - R (IIS 6.0 Metabase Properties Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letters, N - R.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
|Metabase Property|IIS 6.0 WMI Class|IIS 7.0 Schema Element|IIS 7.0 WMI Class|  
|-----------------------|-----------------------|----------------------------|-----------------------|  
|NameResolutionType|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NewsCrawlerTime|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NewsDropDirectory|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NewsFailedPickupDirectory|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NewsPickupDirectory|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NntpClearTextProvider|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NntpCommandLogMask|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NntpOrganization|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NntpServiceVersion|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NntpUucpName|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|NotDeletable|IIsNntpServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|NTAuthenticationProviders|None|\<windowsAuthentication><br /><br /> \<providers /><br /><br /> \</windowsAuthentication>|ConfigurationSection.ConfigurationSectionWithCollection.WindowsAuthenticationSection.Providers.Providers|  
|OrphanActionExe|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<applicationPools><br /><br /> \<failure orphanActionExe /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.OrphanActionExe<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.OrphanActionExe|  
|OrphanActionParams|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure orphanActionParams /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.OrphanActionParams<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.OrphanActionParams|  
|OrphanWorkerProcess|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure orphanWorkerProcess /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.OrphanWorkerProcess<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.OrphanWorkerProcess|  
|PassivePortRange|IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|PassportRequiredADMapping|IIsFtpServiceSetting|None **Note:**  This metabase property is deprecated.|None|  
|Path|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<sites><br /><br /> \<site><br /><br /> \<application><br /><br /> \<virtualDirectory physicalPath /><br /><br /> \</application><br /><br /> \<site><br /><br /> \</sites>|Object.ConfiguredObject.VirtualDirectory.PhysicalPath<br /><br /> Object.Server.VirtualDirectoryDefaults.PhysicalPath<br /><br /> Object.ConfiguredObject.Site. VirtualDirectoryDefaults.PhysicalPath<br /><br /> Object.ConfiguredObject.Application. VirtualDirectoryDefaults.PhysicalPath|  
|PeriodicRestartMemory|IIsWevVirtualDirSetting|\<applicationPools><br /><br /> \<recycling><br /><br /> \<periodicRestart memory/><br /><br /> \</recycling><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.PeriodicRestart.Memory<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.PeriodicRestart.Memory|  
|PeriodicRestartPrivateMemory|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<recycling><br /><br /> \<periodicRestart privateMemory /><br /><br /> \</recycling><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.PrivateMemory<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.PeriodicRestart.PrivateMemory|  
|PeriodicRestartRequests|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<recycling requests /><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.PeriodicRestart.Requests<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.PeriodicRestart.Requests|  
|PeriodicRestartSchedule|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<periodicRestart><br /><br /> \<schedule value /><br /><br /> \</periodicRestart><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.PeriodicRestart.Schedule.Value<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.PeriodicRestart.Schedule.Value|  
|PeriodicRestartTime|IisApplicationPoolSetting<br /><br /> IisApplicationPoolsSetting|\<applicationPools><br /><br /> \<periodicRestart time /><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.PeriodicRestart.Time<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.PeriodicRestart.Time|  
|PickupDirectory|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|\<mailSettings><br /><br /> \<smtp><br /><br /> \<specifiedPickupDirectory pickupDirectoryLocation /><br /><br /> \</smtp><br /><br /> \</mailSettings>|ConfigurationSection.SmtpMailSettingsSection.SpecifiedPickupDirectory.PickupDirectoryLocation|  
|PingingEnabled|IsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|\<applicationPools><br /><br /> \<processModel pingingEnabled /><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.PingingEnabled<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.PingingEnabled|  
|PingInterval|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> processModel pingInterval /><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.PingInterval<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.PingInterval|  
|PingResponseTime|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<processModel pingResponseTime /><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.PingResponseTime<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.PingResponseTime|  
|PoolIdcTimeout|IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolsSetting|None **Note:**  This metabase property is deprecated.|None|  
|Pop3properties|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebDirectorySetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|PostmasterEmail|None|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|PostmasterName|IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|PrettyNamesFile|IIsSmtpServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|ProcessTCRIfLoggedOn|IIsNntpServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|QueueDirectory|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None|None|  
|RapidFailProtection|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure rapidFailProtection /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.RapidFailProtection<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.RapidFailProtection|  
|RapidFailProtectionInterval|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure rapidFailProtectionInterval /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.RapidFailProtectionInterval<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.RapidFailProtectionInterval|  
|RapidFailProtectionMaxCrashes|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure rapidFailProtectionMaxCrashes /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.RapidFailProtectionMaxCrashes<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.RapidFailProtectionMaxCrashes|  
|Realm|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<authentication><br /><br /> \<basicAuthentication realm /><br /><br /> \<digestAuthentication  realm /><br /><br /> \</authentication>|ConfigurationSection.BasicAuthenticationSection.Realm<br /><br /> ConfigurationSection.DigestAuthenticationSection.Realm|  
|RedirectHeaders|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebDirectorySetting|\<httpProtocol><br /><br /> \<redirectHeaders><br /><br /> \</httpProtocol>|ConfigurationSection.ConfigurationSectionWithCollection.HttpProtocolSection.RedirectHeaders.RedirectHeaders|  
|RelayForAuth|IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RelayIpList|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RemoteRetryAttempts|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RemoteRetryInterval|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RemoteSmtpPort|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RemoteSmtpSecurePort|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RemoteTimeout|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RsestrictionListCustomDesc|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  This metabase property is deprecated.|None|  
|RevocationFreshnessTime|None|None<br /><br /> See HTTP_SERVICE_CONFIG_SSL_PARAM|None|  
|RevocationURLRetrievalTimeout|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None<br /><br /> See HTTP_SERVICE_CONFIG_SSL_PARAM|None|  
|RouteAction|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None<br /><br /> You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RouteActionString|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RoutePassword|IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RouteUserName|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|RoutingDll|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpDomainSetting|None **Note:**  This metabase property is deprecated.|None|  
|RoutingSources|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  This metabase property is deprecated.|None|