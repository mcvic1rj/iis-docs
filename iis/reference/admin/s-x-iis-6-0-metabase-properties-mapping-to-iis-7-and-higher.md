---
title: "S  -  X  (IIS 6.0 Metabase Properties Mapping to IIS 7 and higher) | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 78d84bb3-fa10-446f-bef5-be321fc2428b
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# S  -  X  (IIS 6.0 Metabase Properties Mapping to IIS 7 and higher)
The table below contains the:  
  
-   Names of the IIS 6.0 metabase properties that begin with letter A.  
  
-   IIS 6.0 WMI classes used to configure each metabase property.  
  
-   IIS 7.0 XML configuration elements or attributes.  
  
-   IIS 7.0 WMI class used to configure the XML configuration element.  
  
-   Names of IIS 6.0 metabase properties not supported or not mapped to an IIS 7.0 configuration element.  
  
|IIS 6.0 Metabase Properties|IIS 6.0 WMI Class|IIS 7.0 Schema Element/Attribute|IIS 7.0 WMI Class.Property|  
|---------------------------------|-----------------------|---------------------------------------|--------------------------------|  
|SaslLogonDomain|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ScriptMaps|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWevVirtualDirSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<handlers />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers|  
|ScriptMaps.Extension|IIsWebServerSetting|\<handlers path />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.Path<br /><br /> ConfigurationSectionWithCollectionElement.HandlerSection.Path|  
|ScriptMaps.Flags|IIsWebServiceSetting|\<handlers requireAccess />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.RequireAccess|  
|ScriptMaps.Script|IIsWevVirtualDirSetting|See \<handlers requireAccess />|See ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.RequireAccess|  
|ScriptMaps.Flags.Script|IIsWebDirectorySetting|See \<handlers requireAccess />|See ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.RequireAccess|  
|ScriptMaps.Check_Path_Info|IIsWebFileSetting|\<handlers resourceType />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.ResourceType|  
|ScriptMaps.ScriptProcessor|IIsWebServerSetting|\<handlers scriptProcessor />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.ScriptProcessor|  
|ScriptMaps.Verbs|IIsWebServiceSetting|\<handlers verb />|ConfigurationSection.ConfigurationSectionWithCollection.HandlersSection.Handlers.Verb|  
|SecureBindings|IIsSmtpServerSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsWebServerSetting|\<site><br /><br /> \<bindings /><br /><br /> \</site>|Object.ConfiguredObject.Site.Bindings|  
|SecuritySetupRequired|None|None **Note:**  This metabase property is deprecated.|None|  
|SendBadTo|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|SendNdrTo|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ServerAutostart|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<sites><br /><br /> \<site serverAutoStart />  \</sites>|Object.ConfiguredObject.Site.ServerAutoStart<br /><br /> Object.Server.SiteDefaults.ServerAutoStart|  
|ServerBindings|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<site><br /><br /> \<bindings /><br /><br /> \</site>|Object.ConfiguredObject.Site.Bindings|  
|ServerCommand|IIsWebServerSetting|See RSCA|None|  
|ServerComment|IIsWebServerSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ServerConfigFlags|IIsWebInfoSetting|None **Note:**  This metabase property is deprecated.|None|  
|ServerListenBacklog|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None **Note:**  This metabase property is deprecated.|None|  
|ServerListenTimeout|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ServerSize|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ServerState|IIsWebServerSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|SessionKey|IIS_Global|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
ShouldDeliver|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ShouldPickupMail|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ShouldPipelineIn|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ShouldPipelineOut|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ShutdownLatency|IIsNntpServerSetting<br /><br /> IIsNntpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|ShutdownTimeLimit|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWevVirtualDirSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting<br /><br /> IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<processModel shutdownTimeLimit /><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.ShutdownTimeLimit<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.ShutdownTimeLimit|  
|SmartHost|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|SmartHostType|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|SMPAffinitized|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|\<applicationPools><br /><br /> \<cpu smpAffinitized><br /><br /> \</applicationPools>|Object.ApplicationPool.Cpu.SmpAffinitized<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.SmpAffinitized|  
|SMPProcessorAffinityMask|IIsApplicationPool<br /><br /> IIsApplicationPools|\<applicationPools><br /><br /> \<cpu SmpProcessorAffinityMask><br /><br /> \</applicationPools>|Object.ApplicationPool.Cpu.SmpProcessorAffinityMask<br /><br /> Object.ApplicationPool.Cpu.SmpProcessorAffinityMask2<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.SmpProcessorAffinityMask<br /><br /> Object.Server.ApplicationPoolDefaults.Cpu.SmpProcessorAffinityMask2|  
|Smtpproperties|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|SSIExecDisable|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWevVirtualDirSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<serverSideInclude ssiExecDisable />|ConfigurationSection.ServerSideIncludeSection.SsiExecDisable|  
|SSLAlwaysNegoClientCert|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|None<br /><br /> See HTTP_SERVICE_CONFIG_SSL_FLAG_NEGOTIATE_CLIENT_CERT flag of the DefaultFlags member of the HTTP_SSL_INFO structure in the HTTP API.|None|  
|SSLCertHash|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpServerSetting|None<br /><br /> See HTTP_SERVICE_CONFIG_SSL_PARAM structure in the HTTP API|None|  
|SslCtlIdentifier|IIsWebServerSetting|None<br /><br /> See DefaultSslCtlIdentifier member of the HTTP_SERVICE_CONFIG_SSL_PARAM structure in the HTTP API|None|  
|SslCtlStoreName|IIsWebServerSetting|None<br /><br /> See DefaultSslCtlStoreName member of the HTTP_SERVICE_CONFIG_SSL_PARAM structure in the HTTP API|None|  
SSLStoreName|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|HTTP_SERVICE_CONFIG_SSL_PARAM structure in the HTTP API|None|  
|SslUseDsMapper|IIsWebServiceSetting|None<br /><br /> See HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER flag of the DefaultFlags member of the HTTP_SERVICE_CONFIG_SSL_PARAM structure in the HTTP API|None|  
|StartupTimeLimit|IIsApplicationPoolSetting<br /><br /> IIsApplicationPoolsSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<processModel StartupTimeLimit /><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.StartupTimeLimit<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.StartupTimeLimit|  
|SuppressDefaultFtpBanner|IIsFtpServerSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|TraceUriPrefix|IIsWebServerSetting<br /><br /> IIsWebServiceSetting|\<httpTracing><br /><br /> \<traceUrls /><br /><br /> \<httpTracing><br /><br /> \<traceFailedRequests><br /><br /> \<add path /><br /><br /> \</traceFailedRequests>|ConfigurationSection.ConfigurationSectionWithCollection.HttpTracingSection.TraceUrls.TraceUrls<br /><br /> ConfigurationSection.ConfigurationSectionWithCollection.TraceFailedRequestsSection.TraceFailedRequests.Path|  
|UNCPassword|IIsWebVirtualDirSetting<br /><br /> IIsFtpVirtualDirSetting<br /><br /> IIsSmtpVirtualDirSetting<br /><br /> IIsNntpVirtualDirSetting|\<virtualDirectory password />|Object.ConfiguredObject.VirtualDirectory.Password<br /><br /> Object.ConfiguredObject.Application.VirtualDirectoryDefaults.Password<br /><br /> Object.ConfiguredObject.Site.VirtualDirectoryDefaults.Password<br /><br /> Object.Server.VirtualDirectoryDefaults.Password|  
|UNCUserName|IIsWebVirtualDirSetting<br /><br /> IIsFtpVirtualDirSetting<br /><br /> IIsSmtpVirtualDirSetting<br /><br /> IIsNntpVirtualDirSetting|\<virtualDirectory userName />|Object.ConfiguredObject.VirtualDirectory.UserName<br /><br /> Object.ConfiguredObject.Application.VirtualDirectoryDefaults.UserName<br /><br /> Object.ConfiguredObject.Site.VirtualDirectoryDefaults.UserName<br /><br /> Object.Server.VirtualDirectoryDefaults.UserName|  
|UpdateDefaultDomain|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|UpdateFQDN|IIsSmtpServerSetting<br /><br /> IIsSmtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|UploadReadAheadSize|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWevVirtualDirSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|\<serverRuntime uploadReadAheadSize />|ConfigurationSection.ConfigurationSectionWithCollection.ServerRuntimeSection.UploadReadAheadSize|  
UseDigestSSP|IIsWebServerSetting<br /><br /> IIsWebServiceSetting<br /><br /> IIsWevVirtualDirSetting<br /><br /> IIsWebDirectorySetting<br /><br /> IIsWebFileSetting|None **Note:**  This metabase property is deprecated.|None|  
|UserIsolationMode|IIsFtpServerSetting<br /><br /> IIsFtpServiceSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|VrDoExpire|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|VrDriverClsid|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|VrDriverProgid|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|VrOwnModerator|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|VrUseAccount|IIsNntpVirtualDirSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|  
|WAMUserName|IIsWebServiceSetting<br /><br /> IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<processModel userName /><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.UserName<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.UserName|  
|WAMUserPass|IIsWebServiceSetting<br /><br /> IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|\<applicationPools><br /><br /> \<add><br /><br /> \<processModel password /><br /><br /> \</add><br /><br /> \</applicationPools>|Object.ApplicationPool.ProcessModel.Password<br /><br /> Object.Server.ApplicationPoolDefaults.ProcessModel.Password|  
|WebSvcExtRestrictionList|IIsWebServiceSetting|\<isapicgiRestriction />|ConfigurationSection.ConfigurationSectionWithCollection.IsapicgiRestrictionSection|  
|WebSvcExtRestrictionList AllowDenyFlag|IIsWebServiceSetting|\<isapicgiRestriction allowed />|ConfigurationSection.ConfigurationSectionWithCollection.IsapicgiRestrictionSection.IsapiCgiRestriction.Allowed|  
|WebSvcExtRestrictionList Description|IIsWebServiceSetting|\<isapicgiRestriction description/>|ConfigurationSection.ConfigurationSectionWithCollection.IsapicgiRestrictionSection.IsapiCgiRestriction.Description|  
|WebSvcExtRestrictionList GroupID|IIsWebServiceSetting|\<isapicgiRestriction groupId />|ConfigurationSection.ConfigurationSectionWithCollection.IsapicgiRestrictionSection.IsapiCgiRestriction.GroupID|  
|WebSvcExtRestrictionList Path|IIsWebServiceSetting|\<isapicgiRestriction path/>|ConfigurationSection.ConfigurationSectionWithCollection.IsapicgiRestrictionSection.IsapiCgiRestriction.Path|  
|WebSvcExtRestrictionList UIDeletableFlag|IIsWebServiceSetting|None|None|  
|Win32Error|IIsWevVirtualDirSetting<br /><br /> IsWebServerSetting<br /><br /> IIsFtpVirtualDirSetting<br /><br /> IIsFtpServerSetting<br /><br /> IIsSmtpVirtualDirSetting<br /><br /> IIsSmtpServerSetting<br /><br /> IIsNntpVirtualDirSetting<br /><br /> IIsNntpServerSetting<br /><br /> IIsApplicationPoolsSetting<br /><br /> IIsApplicationPoolSetting|None<br /><br /> See IRSCA AppPool::QueryState|None|  
|XMLSchemaTimeStamp|IIs_Global|None **Note:**  This metabase property is deprecated.|None|  
|XoverTableFile|IIsNntpServerSetting|None **Note:**  You can configure this metabase property using IIS Management Compatibility feature.|None|