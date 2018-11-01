---
title: "WebServicesSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5ab3a470-f3e2-9b55-dbc6-01b4e64b0d70
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# WebServicesSection Class
Controls the behavior of XML Web services and their clients.  
  
## Syntax  
  
```vbs  
class WebServicesSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `WebServicesSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|(Inherited from [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md).)|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `WebServicesSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`ConformanceWarnings`|A [ConformanceWarningSettings](../../reference/admin/conformancewarningsettings-class.md) value that lists the WS-I (Web Services Interoperability Organization) profiles that are used to validate the Web services. **Note:**  Currently, the only WS-I profile supported in the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] is Basic Profile Version 1.1 (BasicProfile 1_1).|  
|`Diagnostics`|A [DiagnosticsSettings](../../reference/admin/diagnosticssettings-class.md) value that specifies whether to return exceptions to the client for debugging.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Protocols`|A [WebServicesProtocolSettings](../../reference/admin/webservicesprotocolsettings-class.md) value that specifies the transmission protocols that [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] can use to decrypt data sent from a client browser in the HTTP request.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`ServiceDescriptionFormatExtensionTypes`|A [ServiceDescriptionFormatSettings](../../reference/admin/servicedescriptionformatsettings-class.md) value that specifies the service description format extensions to run in the scope of the configuration file.|  
|`SoapEnvelopeProcessing`|A [SoapEnvelopeProcessingInfo](../../reference/admin/soapenvelopeprocessinginfo-class.md) value that configures a time-out to help mitigate denial of service attacks.|  
|`SoapExtensionImporterTypes`|A [SoapExtensionImporterTypesSettings](../../reference/admin/soapextensionimportertypessettings-class.md) value that specifies the SOAP extensions to run when a service description for a Web service in the scope of the configuration file is accessed to create a proxy class.|  
|`SoapExtensionReflectorTypes`|A [SoapExtensionReflectorTypesSettings](../../reference/admin/soapextensionreflectortypessettings-class.md) value that specifies the SOAP extensions to run when a service description is generated for all Web services in the scope of the configuration file.|  
|`SoapExtensionTypes`|A [SoapExtensionTypesInfo](../../reference/admin/soapextensiontypesinfo-class.md) value that specifies the SOAP extensions to run with all Web services in the scope of the configuration file.|  
|`SoapServerProtocolFactory`|A [SoapServerProtocolFactory](../../reference/admin/soapserverprotocolfactory-class.md) value that sets a [System.Web.Services.Configuration.TypeElement](http://go.microsoft.com/fwlink/?LinkId=70958) object that corresponds to the protocol that is used to call the Web service.|  
|`SoapTransportImporterTypes`|A [SoapTransportImporterTypesInfo](../../reference/admin/soaptransportimportertypesinfo-class.md) value that contains  [SoapTransportImporterTypeElement](../../reference/admin/soaptransportimportertypeelement-class.md) instances that import SOAP transmission protocols into Web services.|  
|`WsdlHelpGenerator`|A [WsdlHelpGeneratorInfo](../../reference/admin/wsdlhelpgeneratorinfo-class.md) value that specifies the Web service Help page (an .aspx file) that is displayed to a browser when the user browses to an .asmx page.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `WebServicesSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.SystemWebSectionGroup.WebServices%2A?displayProperty=fullName>   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ConformanceWarning Class](../../reference/admin/conformancewarning-class.md)   
 [ConformanceWarningSettings Class](../../reference/admin/conformancewarningsettings-class.md)   
 [DiagnosticsSettings Class](../../reference/admin/diagnosticssettings-class.md)   
 [ServiceDescriptionFormatSettings Class](../../reference/admin/servicedescriptionformatsettings-class.md)   
 [SoapEnvelopeProcessingInfo Class](../../reference/admin/soapenvelopeprocessinginfo-class.md)   
 [SoapExtensionImporterTypesSettings Class](../../reference/admin/soapextensionimportertypessettings-class.md)   
 [SoapExtensionReflectorTypesSettings Class](../../reference/admin/soapextensionreflectortypessettings-class.md)   
 [SoapExtensionTypesInfo Class](../../reference/admin/soapextensiontypesinfo-class.md)   
 [SoapServerProtocolFactory Class](../../reference/admin/soapserverprotocolfactory-class.md)   
 [SoapTransportImporterTypeElement Class](../../reference/admin/soaptransportimportertypeelement-class.md)   
 [SoapTransportImporterTypesInfo Class](../../reference/admin/soaptransportimportertypesinfo-class.md)   
 [TypeElement Class](../../reference/admin/typeelement-class.md)   
 [WebServicesProtocolSettings Class](../../reference/admin/webservicesprotocolsettings-class.md)   
 [IIS 7.0: WebServicesSection Class](../../reference/admin/webservicessection-class.md)   
 [WsdlHelpGeneratorInfo Class](../../reference/admin/wsdlhelpgeneratorinfo-class.md)   
 [System.Web.Services.Description.SoapTransportImporter](http://go.microsoft.com/fwlink/?LinkId=70959)