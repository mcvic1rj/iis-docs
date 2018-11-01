---
title: "ValidationSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: da81aca7-b37a-42a3-8b32-b1ae2a4966e2
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# ValidationSection Class
Enables or disables validation checks on configuration files.  
  
## Syntax  
  
```vbs  
class ValidationSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `ValidationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `ValidationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`ValidateIntegratedModeConfiguration`|A read/write `boolean` value. `true` if IIS generates a migration error message when it detects that an ASP.NET 1.0 Web application should be modified to run in Integrated mode; otherwise, `false`. The default value is `true`. For more information about this property, see the Remarks section.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 IIS generates a migration error message if the `ValidateIntegratedModeConfiguration` property is enabled and one of the following is true:  
  
-   Your application defines an `<httpModules>` section in its Web.config file.  
  
     In [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] Integrated mode, [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] modules are specified with native modules in a unified `<modules>` section under `<system.webServer>`.  
  
-   Your application defines an `<httpHandlers>` section in its Web.config file.  
  
     In [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] Integrated mode, the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] handler mappings are specified in a unified `<handlers>` section inside `<system.webServer>`. The `<handlers>` section replaces both the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] `<httpHandlers>` and IIS script-processor-mapping configurations, which were both required to set up a ASP.NET 1.0 handler mapping.  
  
-   Your application's Web.config file specifies `<identity impersonate="true" />`.  
  
     In [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] Integrated mode, client impersonation is not available in some early request processing stages. Therefore, IIS will generate the migration error message. If your [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] Web application impersonates client credentials (most common with intranet scenarios), you may want to set the `ValidateIntegratedModeConfiguration` property to `false`.  
  
 If you migrate your configuration manually, or you do not migrate your configuration but you want IIS to remain in Integrated mode (which you should avoid), you can disable migration error messages by setting the `ValidateIntegratedModeConfiguration` property to `false`.  
  
> [!NOTE]
>  Because IIS will no longer provide warnings for unsupported configurations when `ValidateIntegratedModeConfiguration` is `false`, ensure that your application works correctly in Integrated mode before you make this setting.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `ValidationSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)