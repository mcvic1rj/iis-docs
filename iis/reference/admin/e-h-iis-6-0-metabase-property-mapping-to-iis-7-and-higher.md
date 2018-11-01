---
title: "E - H (IIS 6.0 Metabase Property Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2075b171-6887-45c9-91c7-a09968016ea6
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# E - H (IIS 6.0 Metabase Property Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letters E - H.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
## E - F - G - H  
  
|IIS 6.0 Metabase Property|IIS 6.0 WMI class|IIS 7.0 Schema element/attribute|IIS 7.0 WMI class.property|  
|-------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|Enable32BitAppOnWin64|IIsWebServiceSetting|\<applicationPools enable32BitAppOn64 />|Object.ApplicationPool.Enable32BitAppOnWin64<br /><br /> Object.Server.ApplicationPoolDefaults.Enable32BitAppOnWin64|  
|EnableDocFooter|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<staticContent><br /><br /> \<enableDocFooter><br /><br /> \</staticContent>|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.EnableDocFooter|  
|EnableEditWhileRunning|IIsComputerSetting|None **Note:**  This property is deprecated.|None|  
|EnableHistory|IIsComputerSetting|None **Note:**  This property is deprecated.|None|  
|EnableReverseDns|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<ipSecurity><br /><br /> \<enableReverseDns><br /><br /> \</ipSecurity>|ConfigurationSection.ConfigurationSectionWithCollection.IPSecuritySection.EnableReverseDns|  
|EnableReverseDnsLookup|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  This property is deprecated.|None|  
|EtrnDays|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|EtrnSubdomains|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExitMessage|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExMdbGuid|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExpireNewsgroups|IIsNntpExpireSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExpirePolicyName|IIsNntpExpireSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExpireSpace|IIsNntpExpireSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|ExpireTime|IIsNntpExpireSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|Feed.`properties`|IIsNntpFeedSetting<br /><br /> IIsNntpFeedsSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|FilterDescription|IIsFilterSetting|None **Note:**  See RSCA_ISAPI_FILTER_INFO Structure|None|  
|FilterEnableCache|IIsFilterSetting|\<isapiFilters><br /><br /> \<enableCache><br /><br /> \</isapiFilters>|ConfigurationSection.ConfigurationSectionWithCollection.IsapiFiltersSection.IsapiFilters.EnableCache|  
|FilterEnabled|IIsFilterSetting|\<isapiFilters><br /><br /> \<filter enabled /><br /><br /> \</isapiFilters>|ConfigurationSection.ConfigurationSectionWithCollection.IsapiFiltersSection.IsapiFilters.Enabled|  
|FilterFlags|IIsFilterSetting|None **Note:**  See the notificationBitmask member of the RSCA_ISAPI_FILTER_INFO structure|None|  
|FilterLoadOrder|IIsFilterSetting|None **Note:**  This property is deprecated.|None|  
|FilterPath|IIsFiltersSetting|\<isapiFilters><br /><br /> \< filter path><br /><br /> \</isapiFilters>|ConfigurationSection.ConfigurationSectionWithCollection.IsapiFiltersSection.IsapiFilters.Path|  
|FilterSate|IIsFilterSetting|None **Note:**  See the RSCA_OBJECT_STATE_ENUM structure.|None|  
|FrontPageWeb|IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebDirectorySetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|FsPropertyPath|IISNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|FtpDirBrowseShowLongDate|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting<br /><br /> IIsFtpVirtualDirSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|FtpLogInUtf8|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|FullyQualifiedDomainName|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|GreetingsMessage|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|GroupHelpFile|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|GroupListFile|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|GroupvarListFile|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
  
## H  
  
|IIS 6.0 Metabase Property|IIS 6.0 WMI class|IIS 7.0 Schema element/attribute|IIS 7.0 WMI class.property|  
|-------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|HcCacheControlHeader|IIsCompressionSchemesSetting|\<httpCompression cacheControlHeader />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.CacheControlHeader|  
|HcCompressionBufferSize|IIsCompressionSchemesSetting|None **Note:**  You can configure this metabase property using the Management Compatibility feature.|None|  
|HcCompressionDirectory|IIsCompressionSchemesSetting|\<httpCompression directory />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.Directory|  
|HcCompressionDll|IIsCompressionSchemeSetting|\<httpCompression><br /><br /> \<scheme dll /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.Dll|  
|HcCreateFlags|IIsCompressionSchemeSetting|\<httpCompression><br /><br /> \<scheme name /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.Name|  
|HcDoDiskSpaceLimiting|IIsCompressionSchemesSetting|\<httpCompression doDiskSpaceLimiting />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.DoDiskSpaceLimiting|  
|HcDoDynamicCompression|IIsCompressionSchemeSetting<br /><br /> IIsCompressionSchemesSetting|\<httpCompression><br /><br /> \<scheme doDynamicCompression /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.DoDynamicCompression|  
|HcDoOnDemandCompression|IIsCompressionSchemeSetting<br /><br /> IIsCompressionSchemesSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HcDoStaticCompression|IIsCompressionSchemeSetting<br /><br /> IIsCompressionSchemesSetting|\<httpCompression><br /><br /> \<scheme doStaticCompression /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.DoStaticCompression|  
|HcDynamicCompressionLevel|IIsCompressionSchemeSetting|\<httpCompression><br /><br /> \<scheme dynamicCompressionLevel /><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.DynamicCompressionLevel|  
|HcExpiresHeader|IIsCompressionSchemesSetting|\<httpCompression expiresHeader />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.ExpiresHeader|  
HcFileExtensions|IIsCompressionSchemeSetting|None **Note:**  Configure this metabase property using the Management Compatibility feature.|None|  
|HcFilesDeletedPerDiskFree|IIsCompressionSchemeSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HcIoBufferSize|IIsCompressionSchemesSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HcMaxDiskSpaceUsage|IIsCompressionSchemesSetting|\<httpCompression maxDiskSpaceUsage />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.MaxDiskSpaceUsage|  
|HcMaxQueueLength|IIsCompressionSchemesSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HcMinFileSizeForComp|IIsCompressionSchemesSetting|\<httpCompression minFileSizeForComp />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.MinFileSizeForComp|  
|HcNoCompressionForHttp10|IIsCompressionSchemesSetting|\<httpCompression noCompressionForHttp10 />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.NoCompressionForHttp10|  
|HcNoCompressionForProxies|IIsCompressionSchemesSetting|\<httpCompression noCompressionForProxies />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.NoCompressionForProxies|  
|HcNoCompressionForRange|IIsCompressionSchemesSetting|\<httpCompression noCompressionForRange />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.NoCompressionForRange|  
|HcOnDemandCompLevel|IIsCompressionSchemesSetting|\<httpCompression><br /><br /> \<scheme name="gzip" staticCompressionLevel="7"><br /><br /> \</httpCompression>|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.HttpCompression.StaticCompressionLevel|  
|HcOnDemandCompression|IIsCompressionSchemesSetting|None<br /><br /> **Note** This metabase property is deprecated.|None.|  
|HcPriority|IIsCompressionSchemeSetting|None|None|  
|HcScriptFileExtension|IIsCompressionSchemeSetting|None|None|  
|HcSendCacheHeaders|IIsCompressionSchemesSetting|\<httpCompression sendCacheHeaders />|ConfigurationSection.ConfigurationSectionWithCollection.HttpCompressionSection.SendCacheHeaders|  
|HeaderWaitTimeout|IIsWebServiceSetting|\<webLimits headerWaitTimeout />|ConfigurationSection.WebLimitsSection.HeaderWaitTimeout|  
|HistoryExpiration|IIsNntpServiceSetting<br /><br /> IIsNntpSeverSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HistoryMajorVersionNumber|IIS_Global|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HistoryTableFile|IIsNntpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HonorClientMsgIds|IIsNntpServiceSetting<br /><br /> IIsNntpSeverSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HopCount|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  Configure this metabase property using the IIS Management Compatibility feature.|None|  
|HttpCustomHeaders|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<httpProtocol><br /><br /> \<customHeaders><br /><br /> \</httpProtocol>|ConfigurationSection.HttpProtocolSection.CustomHeaders|  
|HttpErrors|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebdirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<httpErrors>|ConfigurationSection.ConfigurationSectionWithCollection.HttpErrorsSection.HttpErrors|  
|HttpErrors: Path|IIsWebServerSetting|\<httpErrors><br /><br /> \<error path /><br /><br /> \</httpErrors>|ConfigurationSection.ConfigurationSectionWithCollection.HttpErrorsSection. HttpErrors.Path|  
|HttpErrots: Status Codes|IIsWebServiceSetting|\<httpErrors><br /><br /> \<error statusCodes /><br /><br /> \</httpErrors>|ConfigurationSection.ConfigurationSectionWithCollection.HttpErrorsSection.HttpErrors.StatusCode|  
HttpErrors: Substatus Codes|IIsWebFileSetting|\<httpErrors><br /><br /> \<error subStatusCodes /><br /><br /> \</httpErrors>|ConfigurationSection.ConfigurationSectionWithCollection.HttpErrorsSection.HttpErrors.SubStatusCode|  
|HttpErrors: ResponseMode|IIsWebDirectorySetting|\<httpErrors><br /><br /> \<error responseModel /><br /><br /> \</httpErrors>|ConfigurationSection.ConfigurationSectionWithCollection.HttpErrorsSection.HttpErrors.ResponseMode|  
|HttpExpires|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<clientCache><br /><br /> \<staticContent httpExpires /><br /><br /> \</clientCache>|ConfigurationSection.ConfigurationSectionWithCollection.StaticContentSection.ClientCache.HttpExpires|  
|HttpPics|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|None **Note:**  This metabase property is deprecated.|None|  
|HttpRedirect|IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<httpProtocol><br /><br /> \<redirectHeaders><br /><br /> \</httpProtocol>|ConfigurationSection.HttpProtocolSection.RedirectHeaders|