---
title: "B - D (IIS 6.0 Metabase Property Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 10269544-43bb-4ec8-917f-0425d193be7f
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# B - D (IIS 6.0 Metabase Property Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letters, B - D.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
|IIS 6.0 Metabase Properties|IIS 6.0 WMI class|IIS 7.0 Schema element/attribute|IIS 7.0 WMI class.property|  
|---------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|BadMailDirectory|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|BannerMessage|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|BINSchemaTimeStamp|IIS_Global|None **Note:**  This property is deprecated,|None|  
|CacheControlCustom|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<staticContent><br /><br /> \<clientCache cacheControlCustom /><br /><br /> \</staticContent>|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.ClientCache.CacheControlCustom|  
|CacheControlMaxAge|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<staticContent><br /><br /> \<clientCache cacheControlMaxAge /><br /><br /> \</staticContent >|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.ClientCache.CacheControlMaxAge|  
|CacheControlNoCache|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebFileSetting|\<staticContent><br /><br /> \<clientCache cacheControlMode /><br /><br /> \</staticContent>|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.ClientCache.CacheControlMode|  
|CacheISAPI|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|None **Note:**  This property is deprecated.|None|  
|CentralBinaryLoggingEnabled|IIsWebServiceSetting|\<log><br /><br /> \<centralBinaryLogFile enabled /><br /><br /> \</log>|ConfigurationSection.LogSection.CentralBinaryLogFile.Enabled|  
|CentralW3CLoggingEnabled|IIsWebServiceSetting|\<log><br /><br /> \<centralW3CLogFile enabled/><br /><br /> \</log>|ConfigurationSection.LogSection.CentraW3CBinaryLogFile.Enabled|  
|CertCheckMode|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None|Object.SSLBinding.CertificateCheckMode|  
|CGIRestrictionList|None|\<isapiCgiRestriction />|ConfigurationSection.ConfigurationSectionWithCollection.IsapiCgiRestrictionSection|  
|CGITimeout|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebFileSetting|\<cgi timeout />|ConfigurationSection.CgiSection.Timeout|  
|ChangeNumber|IIS_Global|None **Note:**  This property is deprecated.|None|  
|ClientPostHardLimit|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|ClientPostSoftLimit|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|ClusterEnabled|IIsFtpServerSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsWebServerSetting|None **Note:**  This property is deprecated.|None|  
|CollectionComment|None|None **Note:**  This property is deprecated.|None|  
|ConnectResponse|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|ConnectionTimeout|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<sites><br /><br /> \<limits connectionTimeout /><br /><br /> \</sites><br /><br /> ...<br /><br /> \<webLimits connectionTimeout />|Object.ConfiguredObject.Site.Limits.ConnectionTimeout<br /><br /> Object.Server.SiteDefaults.Limits.ConnectionTimeout<br /><br /> ConfigurationSection.WebLimitsSection.ConnectionTimeout|  
ContentIndexed|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsNntpVirtualDirSetting|None **Note:**  This property is deprecated.|None|  
|CPUAction|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> \<cpu action /><br /><br /> \</applicationPools>|Object.ApplicationPool.Cpu.Action<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.Action|  
|CPULimit|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> \<cpu limit /><br /><br /> \</applicationPools>|Object.ApplicationPool.Cpu.Limit<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.Limit|  
|CPUResetInterval|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> <cpu resetinterval<br /><br /> \</applicationPools>|Object.ApplicationPool.Cpu.ResetInterval<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.ResetInterval|  
|CreateCGIWithNewConsole|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<cgi createCGIWithNewConsole />|ConfigurationSection.CgiSection.CreateCGIWithNewConsole|  
|CreateProcessAsUser|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<cgi createProcessAsUser />|ConfigurationSection.CgiSection.CreateProcessAsUser|  
|CSideEtrnDomains|IIsSmtpDomainSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|CustomErrorDescriptions|IIsWebInfoSetting|None **Note:**  This property is deprecated.|None|  
|DefaultDoc|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting|\<defaultDocument />|ConfigurationSection.DefaultDocument|  
|DefaultDocFooter|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting|\<staticContent defaultDocFooter />|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.DefaultDocFooter|  
|DefaultDomain|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|DefaultLogonDomain|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<security><br /><br /> \<authentication><br /><br /> \<basicAuthentication defaultLogonDomain /><br /><br /> \<iisClientCertificateMappingAuthentication defaultLogonDomain /><br /><br /> \</authentication><br /><br /> \</security>|ConfigurationSection.BasicAuthenticationSection.DefaultLogonDomain<br /><br /> ConfigurationSection.IisClientCertificateMappingAuthenticationSection.DefaultLogonDomain|  
|DefaultModeratorDomain|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|DemandStartThreshold|IIsWebServiceSetting|\<webLimits demandStartThreshold />|ConfigurationSection.WebLimitsSection.DemandStartThreshold|  
DirBrowseFlags.DirBrowsexxx|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting|\<directoryBrowse showFlags />|ConfigurationSection.DirectoryBrowseSection.ShowFlags|  
|DirBrowseFlags.EnableDefaultDoc|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting|\<defaultDocument enabled />|ConfigurationSection.DefaultDocumentSection.Enabled|  
|DirBrowseFlags.EnableDirBrowse|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<directoryBrowse enabled />|ConfigurationSection.DirectoryBrowse.Enabled|  
|DirectoryLevelsToScan|IIsWebServiceSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|DisableNewNews|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|DisableSocketPooling|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsFTPServerSetting<br /><br /> IIsFTPServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  This property is deprecated.|None|  
|DisableStaticFileCache|IIsWebVirtualDirSetting|None **Note:**  This property is deprecated.|None|  
|DisallowOverlappingRotation|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> \<recycling disallowOverlappingRotation /> \<applicationPools />|Object.ApplicationPool.Recycling.DisallowOverlappingRotation<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.DisallowOverlappingRotation|  
|DisallowRotationOnConfigChange|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> \<recycling disallowRotationOnConfigChange /><br /><br /> \</applicationPools>|Object.ApplicationPool.Recycling.DisallowRotationOnConfigChange<br /><br /> Object.Server.ApplicationPoolDefaults.Recycling.DisallowRotationOnConfigChange|  
|DoDynamicCompression|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<httpCompression doDynamicCompression /><br /><br /> \<UrlCompression doDynamicCompression />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.DoDynamicCompression<br /><br /> ConfigurationSection.UrlCompressionSection.DoDynamicCompression|  
|DontLog|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<httpLogging dontLog />|ConfigurationSection.HttpLoggingSection.DontLog|  
|DoStaticCompression|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting|\<httpCompression><br /><br /> \<doStaticCompression /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.DoStaticCompression<br /><br /> ConfigurationSection.UrlCompressionSection.DoStaticCompression|  
|DownlevelAdminInstance|IIsWebServiceSetting<br /><br /> IIsFTPServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|DropDirectory|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|