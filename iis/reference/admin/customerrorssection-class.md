---
title: "CustomErrorsSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e5dc46f2-d3ae-7978-93ba-9ee594b54e70
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# CustomErrorsSection Class
Configures [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] custom error messages.  
  
## Syntax  
  
```vbs  
class CustomErrorsSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `CustomErrorsSection` class.  
  
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
 The following table lists the properties exposed by the `CustomErrorsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`CustomErrors`|An array of [CustomError](../../reference/admin/customerror-class.md) values that specify [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] custom errors.|  
|`DefaultRedirect`|A required, nonempty read/write `string` value that contains the default path of either an HTTP error message file or the URL of an error message. This value is inherited by the `Redirect` property of newly created [CustomError](../../reference/admin/customerror-class.md) objects.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Mode`|A read/write `sint32` enumeration that specifies whether custom or default error pages are shown locally or remotely. The possible values are listed later in the Remarks section.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The custom errors represented by the `CustomErrorsSection` class are specific to [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and are in the `<system.web>` section of the Web.config file. Each of these errors is represented by an instance of the [CustomError](../../reference/admin/customerror-class.md) class.  
  
 The custom errors represented by the [HttpErrorsSection](../../reference/admin/httperrorssection-class.md) class are related to [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] and are in the `<system.webServer>` section of the ApplicationHost.config file. Each of these errors is represented by an instance of the [HttpErrorElement](../../reference/admin/httperrorelement-class.md) class. The integration of [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] with IIS in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] made this name change necessary.  
  
 The following table lists the possible values for the `Mode` property. The default is 0 (`RemoteOnly`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`RemoteOnly`|The default [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] error page is shown to local users. Remote users will receive a custom error page if one is defined. If no custom error page is defined for the error received, an IIS error page is shown.|  
|1|`On`|A user-defined [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] custom error page is shown for both local and remote users.|  
|2|`Off`|The default [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] error page is shown for both local and remote users.|  
  
## Example  
 The following example sets the `DefaultRedirect` property to "CustomError.htm" and the `Mode` property to `On`.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the custom errors section for the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "CustomErrorsSection", oSection  
  
' Set the default redirect page to CustomError.htm,  
' and set the Mode property to On.  
oSection.DefaultRedirect = "CustomError.htm"  
oSection.Mode = 1  
oSection.Put_  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `CustomErrorsSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [CustomError Class](../../reference/admin/customerror-class.md)   
 [HttpErrorElement Class](../../reference/admin/httperrorelement-class.md)   
 [HttpErrorsSection Class](../../reference/admin/httperrorssection-class.md)