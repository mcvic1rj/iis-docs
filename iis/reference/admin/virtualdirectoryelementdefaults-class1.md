---
title: "VirtualDirectoryElementDefaults Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 270a77bc-b340-b5b7-05f2-d7fbc0f9f34a
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# VirtualDirectoryElementDefaults Class1
Exposes default configuration settings for IIS virtual directories.  
  
## Syntax  
  
```vbs  
class VirtualDirectoryElementDefaults : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `VirtualDirectoryElementDefaults` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AllowSubDirConfig`|A read/write `boolean` value. `true` if by default IIS looks for Web.config files in content directories lower than the current level; `false` if IIS does not look for these files in directories lower than the current level.|  
|`LogonMethod`|A read/write `sint32` enumeration that specifies the default method by which a user is locally logged on. The type of logon will determine whether the resulting token can also be used remotely. The possible values are listed later in the Remarks section.|  
|`Password`|A read/write `string` value that specifies the default encrypted password for access to the virtual root directory. The default is `null`.|  
|`Path`|A read/write `string` value that contains the default virtual directory path.|  
|`PhysicalPath`|A read/write `string` value that specifies the default physical path that is associated with the virtual directory.|  
|`UserName`|A read/write `string` value that specifies a default user who has rights to access any configuration files or content in a virtual directory. The default is `null`.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `VirtualDirectoryDefaults` property of the [Server](../../reference/admin/server-class1.md), [Site](../../reference/admin/site-class1.md), and [Application](../../reference/admin/application-class1.md) classes.  
  
 The following table contains the possible values and keywords for the `LogonMethod` property. The default is 3 (ClearText). For more information, see the [LogonUserEx](http://go.microsoft.com/fwlink/?LinkId=60074) function.  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|Interactive|Enables the user to log on interactively through a terminal server, remote shell, or similar process. Because this logon type caches logon information for disconnected operations, performance may be affected. This logon type is, therefore, inappropriate for client/server applications, such as mail servers.|  
|1|Batch|Enables the user to log on through a batch server, where processes can be executed for the user without the user's intervention. This logon type is appropriate for servers, such as mail or Web servers, that process many plaintext authentication attempts at a time. Credentials are not cached for this logon type.|  
|2|Network|Enables the user to log on through a high-performance server that authenticates plaintext passwords. Credentials are not cached for this logon type.|  
|3|ClearText|Enables the user to log on by using Basic authentication. The user's name and password are preserved in an authentication package, which allows the server to make connections to other network servers while impersonating the client.<br /><br /> An authentication package is a DLL that encapsulates the authentication logic that determines whether to permit a user to log on. Local Security Authority (LSA) authenticates a user logon by sending the request to an authentication package. The authentication package then examines the logon information and either authenticates or rejects the user logon attempt.|  
  
## Example  
 The following example shows how to set the user name and password for all virtual directories on a Web site. It then shows how to retrieve all the virtual directory defaults for the site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Set the virtual directory defaults on the Web site.  
oSite.VirtualDirectoryDefaults.UserName = "JohnV"  
oSite.VirtualDirectoryDefaults.Password = "p@ssw0rd."  
oSite.Put_  
  
' List all the virtual directory defaults for the Web site.  
WScript.Echo "AllowSubDirConfig: " & _  
    oSite.VirtualDirectoryDefaults.AllowSubDirConfig  
WScript.Echo "LogonMethod: " & _  
    GetLogonMethodText(oSite.VirtualDirectoryDefaults.LogonMethod)  
WScript.Echo "Password: " & oSite.VirtualDirectoryDefaults.Password  
WScript.Echo "Path: " & oSite.VirtualDirectoryDefaults.Path  
WScript.Echo "PhysicalPath: " & _  
    oSite.VirtualDirectoryDefaults.PhysicalPath  
WScript.Echo "UserName: " & oSite.VirtualDirectoryDefaults.UserName  
  
' This helper function converts the LogonMethod value to text.  
Function GetLogonMethodText(LogonMethodValue)  
    Select Case LogonMethodValue  
        Case 0  
            GetLogonMethodText = "Interactive"  
        Case 1  
            GetLogonMethodText = "Batch"  
        Case 2  
            GetLogonMethodText = "Network"  
        Case 3  
            GetLogonMethodText = "ClearText"  
        Case Else  
            GetLogonMethodText = "Unknown logon method."  
    End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `VirtualDirectoryElementDefaults`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [Application Class](../../reference/admin/application-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)   
 [LogonUserEx](http://go.microsoft.com/fwlink/?LinkId=60074)