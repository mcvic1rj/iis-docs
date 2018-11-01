---
title: "VirtualDirectory.Create Method1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0e9a76f1-3fe0-cbb0-6ac5-e258c4b5df06
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# VirtualDirectory.Create Method1
Creates a virtual directory.  
  
## Syntax  
  
```jscript#  
objAppSrv.Get("VirtualDirectory").Create(  
   VirtualDirectoryPath,  
   ApplicationPath,  
   PhysicalPath,  
   SiteName  
);  
  
```  
  
```vbs  
objAppSrv.Get("VirtualDirectory").Create(  
   VirtualDirectoryPath,  
   ApplicationPath,  
   PhysicalPath,  
   SiteName  
)  
```  
  
#### Parameters  
  
|Name|Description|  
|----------|-----------------|  
|`VirtualDirectoryPath`|A `string` value that contains the virtual directory path (for example, "/MyVDir").|  
|`ApplicationPath`|A `string` value that contains the application path (for example, "/MyApp").|  
|`PhysicalPath`|An optional `string` value that contains the physical path to the file directory where the content for the virtual directory is stored (for example, "C:\inetpub\MyVDirFiles"). Although this parameter is optional, most implementations will require it. **Note:**  IIS does not check for the existence of the specified physical directory. If you specify an invalid path and attempt to open the virtual directory in [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)], [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] will display the error message "Could not find a part of the path '*\<path>*'".|  
|`SiteName`|A `string` value that contains the name of the Web site for the virtual directory (for example, "Default Web Site").|  
  
## Return Value  
 This method does not return a value.  
  
## Remarks  
 The `VirtualDirectory` object inherits from the [ConfiguredObject](../../reference/admin/configuredobject-class1.md) class; it does not inherit from the [VirtualDirectoryElementDefaults](../../reference/admin/virtualdirectoryelementdefaults-class1.md) class. This means that the properties on the `VirtualDirectoryElementDefaults` object must also be declared on the `VirtualDirectory` object.  
  
## Example  
 The following example creates a virtual directory called `MyVDir` under the `MyApp` application on the default Web site.  
  
```  
' Connect to the WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Define the parameters.  
strVDirPath = "/MyVDir"  
strAppPath = "/MyApp"  
strPhysicalPath = "C:\inetpub\MyVDirFiles"  
strSiteName = "Default Web Site"  
  
' Create the new virtual directory.  
oWebAdmin.Get("VirtualDirectory").Create _  
    strVDirPath, strAppPath, strPhysicalPath, strSiteName  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)   
 [VirtualDirectoryContainsConfigurationSection Class](../../reference/admin/virtualdirectorycontainsconfigurationsection-class2.md)