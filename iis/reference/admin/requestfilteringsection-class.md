---
title: "RequestFilteringSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 73911071-57c6-2fc8-5e52-9f5cfd4595a8
caps.latest.revision: 38
author: "shirhatti"
manager: "wpickett"
---
# RequestFilteringSection Class
Configures the scanning of incoming URL requests.  
  
## Syntax  
  
```vbs  
class RequestFilteringSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `RequestFilteringSection` class.  
  
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
 The following table lists the properties exposed by the `RequestFilteringSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AllowDoubleEscaping`|A read/write `boolean` value. `true` if double escape characters are permitted in URLs; otherwise, `false`. The default is `false`.|  
|`AllowHighBitCharacters`|A read/write `boolean` value. `true` if non-ASCII characters are permitted in URLs; otherwise, `false`. The default is `true`.|  
|`DenyUrlSequences`|A [UrlSequenceSettings](../../reference/admin/urlsequencesettings-class.md) value that contains URL sequences that can be used to attack a Web server and, therefore, will be denied.|  
|`FileExtensions`|A read/write [FileExtensionsSettings](../../reference/admin/fileextensionssettings-class.md) value that specifies file extensions that can be allowed or denied in a request.|  
|`HiddenSegments`|A [HiddenSegmentSettings](../../reference/admin/hiddensegmentsettings-class.md) value that specifies segments whose content will not be served to the client. **Note:**  A segment is the part of a URL between two slashes or the part of the URL following the last slash. For example, the URL /segment1/segment2/segment3.asp has three segments: segment1, segment2, and segment3.asp. **Note:**  The following segments are blocked by default: bin, App_code, App_GlobalResources, App_LocalResources, App_WebReferences, App_Data, and App_Browsers.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`RequestLimits`|A [RequestLimitsElement](../../reference/admin/requestlimitselement-class.md) value that specifies size limits on incoming HTTP requests.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`Verbs`|A read/write [VerbsSettings](../../reference/admin/verbssettings-class.md) value that specifies HTTP verbs to allow or deny. **Note:**  Wildcards for HTTP verbs are not supported.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 This class integrates into [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] the functionality of the URLScan tool used by previous versions of IIS.  
  
> [!NOTE]
>  For the functionality in the `RequestFilteringSection` class to work, the Request Filtering Module (Modrqflt.dll) must be installed.  
  
## Example  
 The following example shows all of the properties for the request-filtering section in the ApplicationHost.config file.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set objWMIService = GetObject("winmgmts:root\WebAdministration")  
  
' Get the request-filtering section.  
Set oRequestFilteringSection = objWMIService.Get( _  
"RequestFilteringSection.Path='MACHINE/WEBROOT/APPHOST',Location=''")  
  
' Show the path.  
WScript.Echo "[Request Filtering Path]"  
WScript.Echo oRequestFilteringSection.Path_  
WScript.Echo   
  
' Show the AllowDoubleEscaping property as "True" or "False."  
WScript.Echo "[AllowDoubleEscaping]"  
WScript.Echo CStr(oRequestFilteringSection.AllowDoubleEscaping)  
WScript.Echo   
  
' Show the AllowHighBitCharacters property as "True" or "False."  
WScript.Echo "[AllowHighBitCharacters]"  
WScript.Echo CStr(oRequestFilteringSection.AllowHighBitCharacters)  
WScript.Echo   
  
' List the denied URL sequences.  
WScript.Echo "[Denied Url Sequences]"  
For Each oSequence In _  
    oRequestFilteringSection.DenyUrlSequences.DenyUrlSequences  
    WScript.Echo oSequence.Sequence  
Next  
WScript.Echo   
  
' List the file extensions settings.  
WScript.Echo "[File Extensions]"  
  
' Show the AllowUnlisted property as "True" or "False."  
WScript.Echo "Allow unlisted file extensions: " & _  
    oRequestFilteringSection.FileExtensions.AllowUnlisted  
WScript.Echo  
  
' List each file extension and show whether it is allowed.  
For Each oFileExtension In _  
    oRequestFilteringSection.FileExtensions.FileExtensions  
    WScript.Echo "File extension: " & oFileExtension.FileExtension  
    WScript.Echo "File extension allowed: " & oFileExtension.Allowed  
    WScript.Echo  
Next  
WScript.Echo   
  
' List the hidden segments.  
WScript.Echo "[Hidden Segments]"  
For Each oHiddenSegment In _  
    oRequestFilteringSection.HiddenSegments.HiddenSegments  
    WScript.Echo oHiddenSegment.Segment  
Next  
WScript.Echo   
  
' Show the request limits settings.  
WScript.Echo "[Request Limits]"  
WScript.Echo "maxAllowedContentLength: " & _  
oRequestFilteringSection.RequestLimits.maxAllowedContentLength  
WScript.Echo "maxUrl: " & oRequestFilteringSection.RequestLimits.maxUrl  
WScript.Echo "maxQueryString: " & oRequestFilteringSection.RequestLimits.maxQueryString  
WScript.Echo   
  
' Show the header limits settings.  
WScript.Echo vbtab & "[Header Limits]"  
For Each oHeaderLimit In _  
    oRequestFilteringSection.RequestLimits.HeaderLimits.HeaderLimits  
    WScript.Echo vbtab & "Header: " & oHeaderLimit.Header  
    WScript.Echo vbtab & "Header size limit: " & oHeaderLimit.SizeLimit  
    WScript.Echo   
Next  
  
' List the verbs settings.  
WScript.Echo "[Verbs]"  
WScript.Echo "Allow unlisted verbs: " & oRequestFilteringSection.Verbs.AllowUnlisted  
WScript.Echo   
  
' List each verb and show whether it is allowed.  
For Each oVerb In oRequestFilteringSection.Verbs.Verbs  
    WScript.Echo "Verb: " & oVerb.Verb  
    WScript.Echo "Verb allowed: " & oVerb.Allowed  
    WScript.Echo  
Next  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `RequestFilteringSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [FileExtensionElement Class](../../reference/admin/fileextensionelement-class.md)   
 [FileExtensionsSettings Class](../../reference/admin/fileextensionssettings-class.md)   
 [HeaderLimitsSettings Class](../../reference/admin/headerlimitssettings-class.md)   
 [HiddenSegmentSettings Class](../../reference/admin/hiddensegmentsettings-class.md)   
 [\<requestFiltering>](../../reference/admin/requestfiltering-element-for-security.md)   
 [RequestLimitsElement Class](../../reference/admin/requestlimitselement-class.md)   
 [UrlSequence Class](../../reference/admin/urlsequence-class.md)   
 [UrlSequenceSettings Class](../../reference/admin/urlsequencesettings-class.md)   
 [VerbElement Class](../../reference/admin/verbelement-class.md)   
 [VerbsSettings Class](../../reference/admin/verbssettings-class.md)