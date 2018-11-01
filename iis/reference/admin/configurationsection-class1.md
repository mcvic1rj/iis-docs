---
title: "ConfigurationSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7b785db0-a6d8-5278-b524-bdcfc0463613
caps.latest.revision: 32
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSection Class1
Serves as a base class for classes that represent configuration sections.  
  
## Syntax  
  
```vbs  
class ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `ConfigurationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|Retrieves the `allowDefinition` attribute for a configuration section.|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|Retrieves the `allowLocation` attribute for a configuration section.|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|Reverts configuration values in a section to those of its parent section.|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|Sets the `allowDefinition` attribute for a configuration section.|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|Sets the `allowLocation` attribute for a configuration section.|  
  
## Properties  
 The following table lists the properties exposed by the `ConfigurationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Location`|A read-only `string` value that contains the path to a target object relative to the current object. For example, in the object path "MACHINE/WEBROOT/APPHOST/MYSITE/APP/", the `Location` property would contain "MYSITE/APP/". A key property.|  
|`Path`|A read-only `string` value that contains the path to the current object. For example, in the object path "MACHINE/WEBROOT/APPHOST/MYSITE/APP/", the `Path` property would contain "MACHINE/WEBROOT/APPHOST/". A key property.|  
|`SectionInformation`|A [SectionInformation](../../reference/admin/sectioninformation-class.md) object whose read/write properties provide metadata and control locking for a configuration section.|  
  
## Subclasses  
 The following table lists the subclasses exposed by the `ConfigurationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[AccessSection](../../reference/admin/accesssection-class.md)|Specifies access permissions to content protected by Secure Sockets Layer (SSL).|  
|[AnonymousAuthenticationSection](../../reference/admin/anonymousauthenticationsection-class1.md)|Configures Anonymous authentication.|  
|[AnonymousIdentificationSection](../../reference/admin/anonymousidentificationsection-class1.md)|Specifies how cookies are used in a Web application.|  
|[AspSection](../../reference/admin/aspsection-class1.md)|Exposes Active Server Pages (ASP) configuration settings for ASP applications.|  
|[BasicAuthenticationSection](../../reference/admin/basicauthenticationsection-class.md)|Configures Basic authentication.|  
|[CacheSection](../../reference/admin/cachesection-class.md)|Defines cache settings for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] Web application.|  
|[CgiSection](../../reference/admin/cgisection-class.md)|Configures Common Gateway Interface (CGI) settings.|  
|[ClientCertificateMappingAuthenticationSection](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)|Enables or disables client certificate mapping authentication.|  
|[ConfigurationHistorySection](../../reference/admin/configurationhistorysection-class.md)|Configures the configuration history settings of the ApplicationHost Helper Service.|  
|[ConfigurationRedirectionSection](../../reference/admin/configurationredirectionsection-class.md)|Configures the location of the ApplicationHost.config and Administration.config files.|  
|[ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)|Serves as a base class for configuration-section classes that contain collections.|  
|[DateTimeSerializationSection](../../reference/admin/datetimeserializationsection-class.md)|Handles configuration settings for XML serialization of [System.DateTime](http://go.microsoft.com/fwlink/?LinkId=70919) instances.|  
|[DigestAuthenticationSection](../../reference/admin/digestauthenticationsection-class.md)|Configures Digest authentication.|  
|[DirectoryBrowseSection](../../reference/admin/directorybrowsesection-class.md)|Configures directory browsing in IIS.|  
|[GlobalizationSection](../../reference/admin/globalizationsection-class.md)|Configures the globalization settings for a Web application.|  
|[HostingEnvironmentSection](../../reference/admin/hostingenvironmentsection-class.md)|Defines configuration settings that control the behavior of the application hosting environment.|  
|[HttpCookiesSection](../../reference/admin/httpcookiessection-class.md)|Configures properties for cookies used by a Web application.|  
|[HttpLoggingSection](../../reference/admin/httploggingsection-class1.md)|Configures the logging of HTTP requests.|  
|[HttpRuntimeSection](../../reference/admin/httpruntimesection-class.md)|Configures [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] HTTP run-time settings that determine how a request is processed for a given [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application.|  
|[IdentitySection](../../reference/admin/identitysection-class.md)|Specifies whether an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application should run as the application pool identity (the default), the IIS-authenticated user identity, or a custom configured identity.|  
|[LogSection](../../reference/admin/logsection-class1.md)|Configures the logging for a server or site.|  
|[MachineKeySection](../../reference/admin/machinekeysection-class.md)|Defines the configuration settings that control the key generation and algorithms that are used in encryption, decryption, and media access control (MAC) operations in Forms authentication, view-state validation, and session-state application isolation.|  
|[OdbcLoggingSection](../../reference/admin/odbcloggingsection-class1.md)|Specifies configuration settings for logging IIS events to a database through an Open Database Connectivity (ODBC) connection.|  
|[OutputCacheSection](../../reference/admin/outputcachesection-class.md)|Specifies output cache settings for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application.|  
|[ProcessModelSection](../../reference/admin/processmodelsection-class.md)|Configures the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] process model settings on a Web server that is running IIS.|  
|[RequestCachingSection](../../reference/admin/requestcachingsection-class.md)|Contains configuration information for request caching.|  
|[ServerRuntimeSection](../../reference/admin/serverruntimesection-class.md)|Configures request limits for applications on a Web server.|  
|[ServerSideIncludeSection](../../reference/admin/serversideincludesection-class.md)|Configures server-side includes (SSI) directives.|  
|[SessionPageStateSection](../../reference/admin/sessionpagestatesection-class.md)|Configures page view-state settings for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application.|  
|[SettingsSection](../../reference/admin/settingssection-class.md)|Contains settings that specify how the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] connects to the network.|  
|[SmtpMailSettingsSection](../../reference/admin/smtpmailsettingssection-class.md)|Contains Simple Mail Transfer Protocol (SMTP) configuration settings.|  
|[SystemWebDeploymentSection](../../reference/admin/systemwebdeploymentsection-class.md)|Defines configuration settings that support the deployment of a Web application.|  
|[SystemWindowsFormsSection](../../reference/admin/systemwindowsformssection-class.md)|Stores application settings for Windows Forms applications.|  
|[TraceSection](../../reference/admin/tracesection-class.md)|Configures the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] code-tracing service.|  
|[TransactionsDefaultSettingsSection](../../reference/admin/transactionsdefaultsettingssection-class.md)|Contains default settings for transactions.|  
|[TransactionsMachineSettingsSection](../../reference/admin/transactionsmachinesettingssection-class.md)|Represents an XML section in a configuration file that contains settings that can be modified only at the computer level.|  
|[TrustSection](../../reference/admin/trustsection-class.md)|Configures the level of code-access security that is applied to an application.|  
|[UrlCompressionSection](../../reference/admin/urlcompressionsection-class.md)|Enables or disables dynamic or static compression.|  
|[ValidationSection](../../reference/admin/validationsection-class.md)|Enables or disables validation checks on configuration files.|  
|[WebControlsSection](../../reference/admin/webcontrolssection-class.md)|Specifies the shared location of client script files.|  
|[WebLimitsSection](../../reference/admin/weblimitssection-class.md)|Specifies limits on client traffic to a Web server.|  
|[XhtmlConformanceSection](../../reference/admin/xhtmlconformancesection-class.md)|Specifies the XHTML rendering mode for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications.|  
|[XmlSerializerSection](../../reference/admin/xmlserializersection-class.md)|Handles the XML elements used to configure XML serialization.|  
  
## Remarks  
 The association classes that derive from the [ObjectConfigurationAssociation](../../reference/admin/objectconfigurationassociation-class.md) class use the `ConfigurationSection` class to link objects to configuration sections.  
  
 All classes that derive from `ConfigurationSection` inherit the `Location`, `Path`, and `SectionInformation` properties. `Location` and `Path` are key properties for all subclasses of `ConfigurationSection`.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [WMI Provider](../../reference/admin/wmi-provider.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ObjectConfigurationAssociation Class](../../reference/admin/objectconfigurationassociation-class.md)   
 [SectionInformation Class](../../reference/admin/sectioninformation-class.md)