---
title: "A (IIS 6.0 Metabase Property Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 27e44b5b-175a-4533-ae40-be18faa09e4d
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# A (IIS 6.0 Metabase Property Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letter A.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
|IIS 6.0 Metabase Properties|IIS 6.0 WMI Class|IIS 7.0 Schema Element/Attribute|IIS 7.0 WMI Class.Property|  
|---------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|AccessFlags|IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting|\<handlers accessPolicy />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.AccessPolicy|  
|AccessSSLFlags|IIsWebServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebServerSetting|\<security><br /><br /> \<access sslFlags /><br /><br /> \</security>|ConfigurationSection.AccessSection.SslFlags|  
|ADConnectionsPassword|IIsFTPServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|ADConnectionsUserName|IIsFTPServiceSetting<br /><br /> IIsFtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AddNoHeaders|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AdminACL|IIsLogModulesSetting<br /><br /> IIsWebInfoSetting<br /><br /> IIsFtpInfoSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIS_ROOT<br /><br /> IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|None **Note:**  This property is deprecated.|None|  
|AdminACLBin|IIsFtpServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsFtpServiceSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsFtpVirtualDirSetting<br /><br /> IIsLogModulesSetting<br /><br /> IIsWebInfoSetting<br /><br /> IIsFtpInfoSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|None **Note:**  This property is deprecated.|None|  
|AdminEmail|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|  
|AdminName|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|  
|AdminServer|IIsWebServiceSetting<br /><br /> IIsWebInfoSetting|None **Note:**  This property is deprecated. In IIS 7.0, see Configuring Remote Management.|None|  
|AllowAnonymous|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AllowClientPosts|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AllowControlMsgs|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AllowFeedPosts|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AllowKeepAlive|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<httpProtocol allowKeepAlive />|ConfigurationSection.ConfigurationSectionWithCollection.HttpProtocolSection.AllowKeepAlive|  
|AllowPathInfoForScriptMappings|IIsWebServiceSetting<br /><br /> IIsWebServerSetting|\<handlers allowPathInfo />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.AllowPathInfo|  
|AlwaysUseSsl|IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AnonymousOnly|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|AnonymousPasswordSync|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|  
|AnonymousUserName|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<anonymousAuthentication userName />|ConfigurationSection.AnonymousAuthenticationSection.UserName|  
|AnonymousUserPass|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<anonymousAuthentication password />|ConfigurationSection.AnonymousAuthenticationSection.Password|  
|AppAllowClientDebug|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<asp appAllowClientDebug />|ConfigurationSection.AspSection.AppAllowClientDebug|  
|AppAllowDebugging|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<asp appAllowDebugging />|ConfigurationSection.AspSection.AppAllowDebugging|  
|AppFriendlyName|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IISWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|AppIsolated|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|ApplicationDependencies|IIsWebServiceSetting|\<applicationDependencies />|ConfigurationSection.ConfigurationSectionWithCollection.ApplicationDependenciesSection.ApplicationDependencies|  
|AppOopRecoverLimit|IsWebVirtualDirSetting IIsWebServerSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|AppPackageID|IsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|AppPackageName|IsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|AppPoolAutoStart|IIsApplicationPoolSetting|\<applicationPools><br /><br /> \<add autostart /><br /><br /> \</applicationPools>|Object.ApplicationPool.Autostart<br /><br /> Object.Server.ApplicationPoolDefaults.Autostart|  
|AppPoolCommand|IIsApplicationPoolSetting|None|None|  
|AppPoolId|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<applicationPools><br /><br /> \<add name /><br /><br /> \</applicationPools>|Object.ApplicationPool.Name<br /><br /> Object.Server.ApplicationPoolDefaults.Name|  
|AppPoolIdentityType|IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<processModel identityType />|Object.ApplicationPool.ProcessModel.IdentityType<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.IdentityType|  
AppPoolQueueLength|IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<applicationPoolDefaults><br /><br /> \<applicationPools queuelength /><br /><br /> \</applicationPoolDefaults>|Object.ApplicationPool.QueueLength<br /><br /> Object.Server.ApplicationPoolDefaults.QueueLength|  
|AppPoolState|IIsApplicationPool|None|Object.ApplicationPool.GetState method|  
|AppRoot|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None|None|  
|AppWamClsid|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|ArticleTableFile|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS Management Compatibility feature.|None|  
|ArticleTimeLimit|IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  You can configure this metabase property using the IIS 6.0 Management Compatibility feature.|None|  
|AspAllowOutofProcComponents|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|None **Note:**  This property is deprecated.|None|  
|AspAllowSessionState|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<session allowSessionState /><br /><br /> \</asp>|ConfigurationSection.AspSection.Session.AllowSessionState|  
|AspAppServiceFlags|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus appServiceFlags /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.AppServiceFlags|  
|AspAppServiceFlags.AspEnableTracker|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus appServiceFlags /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.AppServiceFlags|  
|AspAppServiceFlags.AspEnableSxs|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus appServiceFlags /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.AppServiceFlags|  
|AspAppServiceFlags.AspUsePartition|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus appServiceFlags /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.AppServiceFlags|  
|AspBufferingLimit|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits bufferingLimit /><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.BufferingLimit|  
AspBufferingOn|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp bufferingOn />|ConfigurationSection.AspSection.BufferingOn|  
|AspCalcLineNumber|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp calcLineNumber />|ConfigurationSection.AspSection.CalcLineNumber|  
|AspCodePage|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp codePage />|ConfigurationSection.AspSection.CodePage|  
|AspDiskTemplateCacheDirectory|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<cache diskTemplateCacheDirectory /><br /><br /> \</asp>|ConfigurationSection.AspSection.Cache.DiskTemplateCacheDirectory|  
|AspEnableApplicationRestart|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp enableApplicationRestart />|ConfigurationSection.AspSection.EnableApplicationRestart|  
|AspEnableAspHtmlFallback|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp enableAspHtmlFallback />|ConfigurationSection.AspSection.EnableAspHtmlFallback|  
|AspEnableChunkedEncoding|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp enableChunkedEncoding />|ConfigurationSection.AspSection.EnableChunkedEncoding|  
|AspEnableParentPaths|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp enableParentPaths />|ConfigurationSection.AspSection.EnableParentPaths|  
|AspEnableTypelibCache|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<cache enableTypelibCache /><br /><br /> \</asp>|ConfigurationSection.AspSection.Cache.EnableTypelibCache|  
|AspErrorsToNTLog|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp errorsToNTLog />|ConfigurationSection.AspSection.ErrorsToNTLog|  
|AspExceptionCatchEnable|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp exceptionCatchEnable />|ConfigurationSection.AspSection.ExceptionCatchEnable|  
|AspExecuteInMTA|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus executeInMta /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.ExecuteInMta|  
AspKeepSessionIdSecure|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<session keepSessionIdSecure /><br /><br /> \</asp>|ConfigurationSection.AspSection.Session.KeepSessionIdSecure|  
|AspLCID|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp lcid />|ConfigurationSection.AspSection.LcId|  
|AspLogErrorRequests|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp logErrorRequests />|ConfigurationSection.AspSection.LogErrorRequests|  
|AspMaxDiskTemplateCacheFiles|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<cache maxDiskTemplateCacheFiles /><br /><br /> \</asp>|ConfigurationSection.AspSection.Cache.MaxDiskTemplateCacheFiles|  
|AspMaxRequestEntityAllowed|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<asp><br /><br /> \<limits maxRequestEntityAllowed /> \</asp>|ConfigurationSection.AspSection.Limits.MaxRequestEntityAllowed|  
|AspPartitionID|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus partitionId /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.PartitionId|  
|AspProcessorThreadMax|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits processorThreadMax /><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.ProcessorThreadMax|  
|AspQueueConnectionTestTime|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits queueConnectionTestTime /> \</asp>|ConfigurationSection.AspSection.Limits.QueueConnectionTestTime|  
AspQueueTimeout|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits queueTimeout /><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.QueueTimeout|  
|AspRequestQueueMax|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits requestQueueMax /><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.RequestQueueMax|  
|AspRunEndOnEndAnonymously|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp runEndOnEndAnonymously />|ConfigurationSection.AspSection.RunEndOnEndAnonymously|  
|AspScriptEngineCacheMax|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<cache scriptEngineCacheMax /><br /><br /> \</asp>|ConfigurationSection.AspSection.Cache.ScriptEngineCacheMax|  
|AspScriptErrorMessage|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp scriptErrorMessage />|ConfigurationSection.AspSection.ScriptErrorMessage|  
|AspScriptErrorSentToBrowser|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp scriptErrorSentToBrowser />|ConfigurationSection.AspSection.ScriptErrorSentToBrowser|  
|AspScriptFileCacheSize|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<cache scriptFileCacheSize /><br /><br /> \</asp>|ConfigurationSection.AspSection.Cache.ScriptFileCacheSize|  
|AspScriptLanguage|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp scriptLanguage />|ConfigurationSection.AspSection.ScriptLanguage|  
|AspScriptTimeout|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<limits scriptTimeout><br /><br /> \</asp>|ConfigurationSection.AspSection.Limits.ScriptTimeout|  
AspSessionMax|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<session max /><br /><br /> \</asp>|ConfigurationSection.AspSection.Session.Max|  
|AspSessionTimeout|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<session timeout /><br /><br /> \</asp>|ConfigurationSection.AspSection.Session.Timeout|  
|AspSxsName|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus sxsName /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.SxsName|  
|AspTrackThreadingModel|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<asp><br /><br /> \<comPlus trackThreadingModel /><br /><br /> \</asp>|ConfigurationSection.AspSection.ComPlus.TrackThreadingModel|  
|AuthChangeURL|IIsWebServiceSetting|None **Note:**  This property is deprecated.|None|  
|AuthExpiredUnsecuredURL|IIsWebServiceSetting|None **Note:**  This property is deprecated.|None|  
|AuthExpiredURL|IIsWebServiceSetting|None **Note:**  This property is deprecated.|None|  
|AuthFlags|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|None|None|  
|AuthFlags.AuthAnonymous|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<anonymousAuthentication enabled />|ConfigurationSection.AnonymousAuthenticationSection.Enabled|  
|AuthFlags.AuthBasic|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<basicAuthentication enabled />|ConfigurationSection.BasicAuthenticationSection.Enabled|  
|AuthFlags.AuthMD5|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<digestAuthentication enabled />|ConfigurationSection.DigestAuthenticationSection.Enabled|  
|AuthFlags.AuthNTLM|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|\<windowsAuthentication enabled />|ConfigurationSection.WindowsAuthenticationSection.Enabled<br /><br /> ConfigurationSection.ConfigurationSectionWithCollection.AuthenticationSection.Mode|  
|AuthFlags.AuthPassport|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebFileSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebVirtualDirSetting|None **Note:**  This property is deprecated.|ConfigurationSection.ConfigurationSectionWithCollection.AuthenticationSection.Mode|  
|AuthNotifyPwDExpUnsecureURL|IIsWebServiceSetting|None **Note:**  This property is deprecated.|None|  
|AuthNotifyPwdExpURL|IIsWebServiceSetting|None **Note:**  This property is deprecated.|None|  
|AuthPersistence|IIsWebVirtualDirSetting IIsWebServerSetting IIsWebServiceSetting IIsWebDirectorySetting|\<windowsAuthentication authPersistSingleRequest />|ConfigurationSection.WindowsAuthenticationSection.AuthPersistSingleRequest|  
|AutoShutdownAppPoolExe|IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<failure autoShutdownExe/><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.AutoShutdownExe<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.AutoShutdownExe|  
AutoShutdownAppPoolParams|IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<failure autoShutdownParams /><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.Failure.AutoShutdownParams<br /><br /> Object.Server.ApplicationPoolDefaults.Failure.AutoShutdownParams|  
|AuthTurnList|IIsSmtpDomainSetting|None **Note:**  This property is deprecated.|None|  
|AzEnabled|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IISWebDirectorySetting<br /><br /> IIsWebFileSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|  
|AzImpersonationLevel|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IISWebDirectorySetting<br /><br /> IIsWebFileSetting|None **Note:**  This property is deprecated.|None|  
|AzScopeName|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IISWebDirectorySetting<br /><br /> IIsWebFileSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|  
|AzStoreName|IIsWebServiceSetting<br /><br /> IIsWebServerSetting<br /><br /> IIsWebVirtualDirSetting<br /><br /> IISWebDirectorySetting<br /><br /> IIsWebFileSetting<br /><br /> IIsSmtpServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServiceSetting<br /><br /> IIsNntpServerSetting|None **Note:**  This property is deprecated.|None|