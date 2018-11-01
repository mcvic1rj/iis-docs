---
title: "ConfigurationSectionWithCollection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b0963c4c-d99f-2f45-3532-ab003df8db2c
caps.latest.revision: 31
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSectionWithCollection Class
Serves as a base class for configuration-section classes that contain collections.  
  
## Syntax  
  
```vbs  
class ConfigurationSectionWithCollection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `ConfigurationSectionWithCollection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|Adds an element to a collection in a configuration section.|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|Clears all elements from a collection in a configuration section.|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|Retrieves the specified member of a collection from a configuration section.|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|Removes the specified element from a collection in a configuration section.|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `ConfigurationSectionWithCollection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 The following table lists the subclasses exposed by the `ConfigurationSectionWithCollection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[ApplicationDependenciesSection](../../reference/admin/applicationdependenciessection-class1.md)|Exposes application dependency information.|  
|[AppSettingsSection](../../reference/admin/appsettingssection-class1.md)|Contains custom application settings, such as file paths, XML Web service URLs, or information that is stored in the .ini file for an application.|  
|[AuthenticationModulesSection](../../reference/admin/authenticationmodulessection-class1.md)|Specifies the authentication modules that conduct the authentication process with a server.|  
|[AuthenticationSection](../../reference/admin/authenticationsection-class1.md)|Configures [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] authentication.|  
|[AuthorizationSection](../../reference/admin/authorizationsection-class1.md)|Configures authorization for access to URLs.|  
|[CachingSection](../../reference/admin/cachingsection-class.md)|Configures output and kernel caching.|  
|[ClientTargetSection](../../reference/admin/clienttargetsection-class.md)|Specifies a collection of mappings between aliases and user agents.|  
|[CompilationSection](../../reference/admin/compilationsection-class.md)|Configures compilation settings for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications.|  
|[ConfigProtectedDataSection](../../reference/admin/configprotecteddatasection-class.md)|Contains protected configuration provider information.|  
|[ConnectionManagementSection](../../reference/admin/connectionmanagementsection-class.md)|Contains a collection that specifies the maximum number of connections to specified network hosts for System.Net APIs.|  
|[ConnectionStringsSection](../../reference/admin/connectionstringssection-class.md)|Specifies a collection of database connection strings for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications.|  
|[CustomErrorsSection](../../reference/admin/customerrorssection-class.md)|Configures [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] custom error messages.|  
|[DefaultDocumentSection](../../reference/admin/defaultdocumentsection-class1.md)|Specifies the Web page file names to serve to clients by default.|  
|[DefaultProxySection](../../reference/admin/defaultproxysection-class.md)|Configures Web proxy server defaults.|  
|[DeviceFiltersSection](../../reference/admin/devicefilterssection-class.md)|Represents a collection of device filters that determine mobile device types or mobile browser capabilities.|  
|[FastCgiSection](../../reference/admin/fastcgisection-class.md)|Contains configuration settings for FastCGI applications.|  
|[GlobalModulesSection](../../reference/admin/globalmodulessection-class.md)|Exposes configuration settings for IIS global modules.|  
|[HandlersSection](../../reference/admin/handlerssection-class.md)|Stores the handlers for a URL.|  
|[HealthMonitoringSection](../../reference/admin/healthmonitoringsection-class.md)|Configures an application for health monitoring.|  
|[HttpCompressionSection](../../reference/admin/httpcompressionsection-class.md)|Configures HTTP compression.|  
|[HttpErrorsSection](../../reference/admin/httperrorssection-class.md)|Configures HTTP error handling for a Web server.|  
|[HttpHandlersSection](../../reference/admin/httphandlerssection-class.md)|Configures settings for [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] handlers.|  
|[HttpModulesSection](../../reference/admin/httpmodulessection-class.md)|Contains [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] modules.|  
|[HttpProtocolSection](../../reference/admin/httpprotocolsection-class.md)|Represents an HTTP protocol configuration section.|  
|[HttpRedirectSection](../../reference/admin/httpredirectsection-class.md)|Configures HTTP redirection.|  
|[HttpTracingSection](../../reference/admin/httptracingsection-class.md)|Represents an HTTP tracing configuration section.|  
|[IisClientCertificateMappingAuthenticationSection](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)|Configures mapping for IIS client certificates.|  
|[IPSecuritySection](../../reference/admin/ipsecuritysection-class.md)|Configures access to Web server content based on IP address-related information.|  
|[IsapiCgiRestrictionSection](../../reference/admin/isapicgirestrictionsection-class.md)|Configures ISAPI and Common Gateway Interface (CGI) restrictions for a Web server that runs in ISAPI mode.|  
|[IsapiFiltersSection](../../reference/admin/isapifilterssection-class.md)|Configures the ISAPI filters on a Web server.|  
|[ListenerAdaptersSection](../../reference/admin/listeneradapterssection-class.md)|Exposes a collection of listener adapters.|  
|[MembershipSection](../../reference/admin/membershipsection-class.md)|Validates user credentials and manages user settings.|  
|[MobileControlsSection](../../reference/admin/mobilecontrolssection-class.md)|Exposes configuration information for mobile controls, their adapters, and device filters.|  
|[ModulesSection](../../reference/admin/modulessection-class.md)|Represents the modules section in a configuration file.|  
|[OutputCacheSettingsSection](../../reference/admin/outputcachesettingssection-class.md)|Specifies the output-cache profile settings that can be applied to pages in an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application.|  
|[PagesSection](../../reference/admin/pagessection-class.md)|Represents the `<pages>` section of a Web.config file.|  
|[ProtocolsSection](../../reference/admin/protocolssection-class.md)|Contains a list of transmission protocols that [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] can use to decrypt data sent from a client browser in the HTTP request.|  
|[RequestFilteringSection](../../reference/admin/requestfilteringsection-class.md)|Configures the scanning of incoming URL requests.|  
|[RoleManagerSection](../../reference/admin/rolemanagersection-class.md)|Defines configuration settings that are used to support the role management infrastructure of Web applications.|  
|[SchemaImporterExtensionsSection](../../reference/admin/schemaimporterextensionssection-class.md)|Contains a collection of extensions that map XML Schema (XSD) types to [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] types.|  
|[SecurityPolicySection](../../reference/admin/securitypolicysection-class.md)|Defines a collection of mappings between security policy files and their trust-level names.|  
|[SessionStateSection](../../reference/admin/sessionstatesection-class.md)|Configures the session state for a Web application.|  
|[SiteMapSection](../../reference/admin/sitemapsection-class.md)|Defines configuration settings for site navigation.|  
|[SqlCacheDependencySection](../../reference/admin/sqlcachedependencysection-class.md)|Represents a <xref:System.Web.Caching.SqlCacheDependency?displayProperty=fullName> configuration section.|  
|[StaticContentSection](../../reference/admin/staticcontentsection-class.md)|Exposes configuration settings for static content on a Web site.|  
|[SystemCodeDomSection](../../reference/admin/systemcodedomsection-class.md)|Specifies a collection of compilers that provide Code Document Object Model (CodeDOM) support.|  
|[SystemDataSection](../../reference/admin/systemdatasection-class.md)|Specifies a list of installed [!INCLUDE[vstecado](../../reference/admin/includes/vstecado-md.md)] data providers.|  
|[SystemDiagnosticsSection](../../reference/admin/systemdiagnosticssection-class.md)|Configures system diagnostics and tracing.|  
|[TraceFailedRequestsSection](../../reference/admin/tracefailedrequestssection-class.md)|Represents a failed-request tracing configuration section.|  
|[TraceProviderDefinitionsSection](../../reference/admin/traceproviderdefinitionssection-class.md)|Represents the configuration section that defines trace providers.|  
|[UrlMappingsSection](../../reference/admin/urlmappingssection-class.md)|Represents a `<urlMappings>` section that contains pairs of inbound/outbound URL mappings.|  
|[WebRequestModulesSection](../../reference/admin/webrequestmodulessection-class.md)|Contains a collection of registered Web request modules.|  
|[WebServicesSection](../../reference/admin/webservicessection-class.md)|Controls the behavior of XML Web services and their clients.|  
|[WindowsAuthenticationSection](../../reference/admin/windowsauthenticationsection-class.md)|Configures Integrated Windows authentication.|  
  
## Remarks  
 If you change a key property that is in a collection, the positional order (and index) of the property in the collection may change. The changed key property will be added to the beginning or end of the collection depending on the value of the `mergeAppend` attribute.  
  
> [!NOTE]
>  The `mergeAppend` attribute is in the appropriate schema file in the section that corresponds to the class property. If the `mergeAppend` attribute is `false`, new items are added to the beginning of the collection; if the `mergeAppend` attribute is `true`, new items are added to the end of the collection.  
  
 You should be careful how you access a key property in a collection after the key property's value has changed. For example, if you change the value of a key property whose index is 4, the new index for the key property will be 0 if the `mergeAppend` attribute is `false`.  
  
> [!NOTE]
>  You should be aware of this behavior when you create any custom schema and custom configuration files. You should not modify the `mergeAppend` attributes in the schema files that ship with [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)]. You cannot modify the `mergeAppend` attribute by using the WMI provider for [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].  
  
 The `mergeAppend` attribute affects the following `ConfigurationSectionWithCollection` class properties that ship with [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)]. The table lists these properties and their corresponding schema files. In all these cases, the schema files that ship with [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] specify `false` for the `mergeAppend` attribute.  
  
|Class|Property|Schema file|  
|-----------|--------------|-----------------|  
|[AuthorizationSection](../../reference/admin/authorizationsection-class1.md)|`Authorization`|ASPNET_Schema.xml|  
|[CachingSection](../../reference/admin/cachingsection-class.md)|`Profiles.Profiles`|IIS_Schema.xml|  
|[DefaultDocumentSection](../../reference/admin/defaultdocumentsection-class1.md)|`Files.Files`|IIS_Schema.xml|  
|[HandlersSection](../../reference/admin/handlerssection-class.md)|`Handlers`|IIS_Schema.xml|  
|[HttpHandlersSection](../../reference/admin/httphandlerssection-class.md)|`HttpHandlers`|ASPNET_Schema.xml|  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|Webadministration.mof|  
  
## See Also  
 [AuthorizationRule Class](../../reference/admin/authorizationrule-class.md)   
 [AuthorizationSection Class](../../reference/admin/authorizationsection-class1.md)   
 [CachingProfileElement Class](../../reference/admin/cachingprofileelement-class.md)   
 [CachingProfileSettings Class](../../reference/admin/cachingprofilesettings-class.md)   
 [CachingSection Class](../../reference/admin/cachingsection-class.md)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [DefaultDocumentSection Class](../../reference/admin/defaultdocumentsection-class1.md)   
 [FileSettings Class](../../reference/admin/filesettings-class1.md)   
 [HandlerAction Class](../../reference/admin/handleraction-class.md)   
 [HandlersSection Class](../../reference/admin/handlerssection-class.md)   
 [HttpHandlerAction Class](../../reference/admin/httphandleraction-class.md)   
 [HttpHandlersSection Class](../../reference/admin/httphandlerssection-class.md)   
 [StringElement Class](../../reference/admin/stringelement-class.md)