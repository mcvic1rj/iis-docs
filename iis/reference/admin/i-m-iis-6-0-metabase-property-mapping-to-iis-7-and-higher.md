---
title: "I - M (IIS 6.0 Metabase Property Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0e9c2167-603b-4e33-ab78-4c71d1c36ed5
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# I - M (IIS 6.0 Metabase Property Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letters, I - M.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
|IIS 6.0 Metabase Property|IIS 6.0 WMI Class|IIS 7.0 Schema Element/Attribute|IIS 7.0 WMI Class.Property|  
|-------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|IdleTimeout|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<processModel idleTimeout /><br /><br /> \<applicationPools>|Object.ApplicationPool.ProcessModel<br /><br /> ConfigurationSection.ProcessModelSection.IdleTimeout|  
|IIS5IsolationModeEnabled|IIsWebServiceSetting|None **Note:**  This metabase property is deprecated.|None|  
|InProcessIsapiApps|IIsWebServiceSetting|None **Note:**  This metabase property is deprecated.|None|  
|IsapiRestrictionList|None|None **Note:**  This metabase property is deprecated.|None<br /><br /> See ConfigurationSection.ConfigurationSectionWithCollection.IsapiCgiRestionSection|  
|IPSecurity|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebdirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<security><br /><br /> \<ipSecurity allowUnlisted /><br /><br /> \</security>|ConfigurationSection.ConfigurationSectionWithCollection.IPSecuritySection.AllowUnlisted|  
|KeyType|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsComputerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsFilterSetting<br /><br /> IIsFiltersSetting<br /><br /> IIsCompressionSchemeSetting<br /><br /> IIsCompressionSchemesSetting<br /><br /> IIsCertMapperSetting<br /><br /> IIsMimeMapSetting<br /><br /> IIsLogModulesSetting<br /><br /> IIsLogModuleSetting<br /><br /> IIsCustomLogModuleSetting<br /><br /> IIsWebInfoSetting<br /><br /> IIS_ROOT<br /><br /> IIS_Global<br /><br /> IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|None **Note:**  This metabase property is deprecated.|None|  
|LoadBalancerCapabilities|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<failure loadBalancerCapabilities /><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.LoadBalancerCapabilities<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.LoadBalancerCapabilities|  
|LocalDomains|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|LocalRetryAttempts|IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|LocalRetryInterval|IIsSmtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|LogAnonymous|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|LogCustomPropertyproperties|IIsCustomLogModuleSetting|None **Note:**  This metabase property is deprecated.|None|  
|LogEventOnRecycle|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<recycling logEventOnRecycle /><br /><br /> \<applicationPools>|Object.ApplicationPool.Recycling.LogEventOnRecycle<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.LogEventOnRecycle|  
|LogExtFileFlags|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<log logExtFileFlags /><br /><br /> \<centralW3CLogFile logExtFileFlags /><br /><br /> \</log>|Object.ConfiguredObject.Site.LogFile.LogExtFileFlags<br /><br /> ConfigurationSection.LogSection.CentralW3CLogFile.LogExtFileFlags|  
|LogFileDirectory|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<log><br /><br /> \<centralBinaryLogFile directory /><br /><br /> \<centralW3CLogFile directory /><br /><br /> \</log>|ConfigurationSection.LogSection.CentralW3CLogFile.Directory<br /><br /> ConfigurationSection.LogSection.CentralBinaryLogFile.Directory<br /><br /> Object.ConfiguredObject.Site.LogFile.Directory|  
LogFileLocalTimeRollover|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<log><br /><br /> \<centralBinaryLogFile localTimeRollover /><br /><br /> \<centralW3CLogFile localTimeRollover /><br /><br /> \</log>|ConfigurationSection.LogSection.CentralW3CLogFile.LocalTimeRollover<br /><br /> ConfigurationSection.LogSection.CentralBinaryLogFile.LocalTimeRollover<br /><br /> Object.ConfiguredObject.Site.LogFile.LocalTimeRollover|  
|LogFilePeriod|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<log><br /><br /> \<centralBinaryLogFile period />     \<centralW3CLogFile period /><br /><br /> \</log>|ConfigurationSection.LogSection.CentralW3CLogFile.Period<br /><br /> ConfigurationSection.LogSection.CentralBinaryLogFile.Period<br /><br /> Object.ConfiguredObject.Site.LogFile.Period|  
|LogFileTruncateSize|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<log><br /><br /> \<centralBinaryLogFile truncateSize /><br /><br /> \<centralW3CLogFile truncateSize /><br /><br /> \</log>|ConfigurationSection.LogSection.CentralW3ClogFile.TruncateSize<br /><br /> ConfigurationSection.LogSection.CentralBinaryLogFile.TruncateSize<br /><br /> Object.ConfiguredObject.Site.LogFile.TruncateSize|  
|LoginUTF8|IIsWebServiceSetting|\<log logInUTF8 />|ConfigurationSection.LogSection.LogInUTF8|  
|LogModuleID|IIsLogModuleSetting|None **Note:**  This metabase property is deprecated.|None|  
|LogModuleUiId|IIsLogModuleSetting|None **Note:**  This metabase property is deprecated.|None|  
|LogModuleList|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|None|None|  
|LogNonAnonymous|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|LogOdbcproperties|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|LogPluginClsid|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<sites><br /><br /> \<logFile customLogPluginClsid /><br /><br /> \</sites>|Object.ConfiguredObject.Site.LogFile.CustomLogPluginClsid|  
|LogType|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|None **Note:**  This metabase property is deprecated.|None<br /><br /> See: Object.ConfiguredObject.Site.LogFile.Enabled|  
|MajorIIsVersionNumber|IIsWebInfoSetting|None **Note:**  This metabase property is deprecated.|None|  
|MasqueradeDomain|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxBandwidth|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsComputerSetting|\<sites><br /><br /> \<limits maxBandwidth /><br /><br /> \</sites>|Object.ConfiguredObject.Site.Limits.MaxBandwidth<br /><br /> Object.Server.SiteDefaults.Limits.MaxBandwidth|  
MaxBandwidthBlocked|IIsWebServerSetting<br /><br /> IIsComputerSetting|None **Note:**  This metabase property is deprecated.|None|  
|MaxBatchedMessages|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|MaxClientsMessages|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxConnections|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<sites><br /><br /> \<limits maxConnections /><br /><br /> \</sites>|Object.ConfiguredObject.Site.Limits.MaxConnections<br /><br /> Object.Server.SiteDefaults.Limits.MaxConnections|  
|MaxDirChangeIOSize|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  This metabase property is deprecated.|None|  
|MaxEndPointConnections|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None|None|  
|MaxErrorFiles|IIsComputerSetting|None **Note:**  You canconfigure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxGlobalBandwidth|IIsWebServiceSetting|\<webLimits maxGlobalBandwidth />|ConfigurationSection.WeblimitsSection.MaxGlobalBandwidth|  
|MaxHistoryFiles|IIsComputerSetting|None **Note:**  This metabase property is deprecated.|None|  
|MaxMailObjects|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxMessageSize|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxOutConnections|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxOutConnectionsPerDomain|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxProcesses|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<processModel maxProcesses /><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.MaxProcesses<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.MaxProcesses|  
|MaxRecipients|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxRequestEntityAllowed|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebdirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<asp><br /><br /> \<limits maxRequestEntityAllowed /><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.MaxRequestEntityAllowed|  
|MaxSearchResults|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxSessionSize|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxSmtpErrors|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MaxSmtpLogonErrors|None|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MD_properties|IIsComputerSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebInfoSetting|None **Note:**  This metabase property is deprecated.|None|  
|MimeMap|IIsMimeMapSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebdirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<staticContent><br /><br /> \<mimeMap /><br /><br /> \</staticContent>|ConfigurationSection.ConfigurationSectionWithCollection.StaticContent|  
|MinFileBytesPerSec|IIsWebServiceSetting|\<webLimits minBytesPerSecond />|ConfigurationSection.WeblimitsSection.MinBytesPerSecond|  
|MinorIIsVersionNumber|IIsWebInfoSetting|None **Note:**  This metabase property is deprecated.|None|  
|ModeratorFile|IIsNntpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|MSDOSDirOutput|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|