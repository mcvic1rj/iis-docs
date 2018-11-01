---
title: "ConfigurationSection.RevertToParent Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7266c221-dc31-4bc5-a895-63f78f48d52f
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSection.RevertToParent Method
Reverts configuration values in a section to their defaults.  
  
## Syntax  
  
```jscript#  
ConfigurationSection.RevertToParent();  
ConfigurationSection.RevertToParent(PropertyName);  
```  
  
```vbs  
ConfigurationSection.RevertToParent  
ConfigurationSection.RevertToParent(PropertyName)  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`PropertyName`|An optional `string` value that contains the name of a property in the configuration section. The property can be nested (for example, `oLogSection.RevertToParent("CentralBinaryLogFile.Directory")`.|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 This method provides a way to delete configuration values that have been written to a configuration file.  
  
## Example  
 The following example shows two ways of using the `RevertToParent` method:  
  
1.  The first part reverts a specified property to the default value. The following line from the example reverts the `Enabled` property of `DefaultDocumentSection` of the default Web site by specifying the property name as a `RevertToParent` parameter.  
  
    ```  
    oDefaultDocumentSection.RevertToParent("Enabled")  
    ```  
  
     This removes the value of `false`, which was specified in the Web.config file of the default Web site, and replaces it with the default value of `true`.  
  
2.  The second part reverts an entire section to the default values. The following line from the example reverts the entire `DefaultDocumentSection` contents of the default Web site by specifying no parameters for `RevertToParent`.  
  
    ```  
    oDefaultDocumentSection.RevertToParent  
    ```  
  
     This removes all values from the default document section in the Web.config file of the default Web site. The default values of the default Web site replace the removed values.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the DefaultDocumentSection for the Default Web Site.  
Set oSite=oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "DefaultDocumentSection", oDefaultDocumentSection  
  
' 1. Revert the Enabled property to its default value.  
oDefaultDocumentSection.RevertToParent("Enabled")  
  
' 2. Revert the entire default document section.  
oDefaultDocumentSection.RevertToParent  
  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ConfiguredObject Class](../../reference/admin/configuredobject-class1.md)   
 [DefaultDocumentSection Class](../../reference/admin/defaultdocumentsection-class1.md)