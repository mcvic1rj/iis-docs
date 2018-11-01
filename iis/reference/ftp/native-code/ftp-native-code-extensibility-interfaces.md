---
title: "FTP Native-Code Extensibility Interfaces | Microsoft Docs"
ms.custom: ""
ms.date: "09/06/2017"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: afa33f3c-e758-4cb2-873c-4b902276707c
caps.latest.revision: 7
author: "shirhatti"
ms.author: "robmcm"
manager: "wpickett"
---
# FTP Native-Code Extensibility Interfaces
Describes the native-code interfaces that developers use to extend the functionality of the [!INCLUDE[ftp75](../../../reference/ftp/native-code/includes/ftp75-md.md)] service for [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)].  
  
## In This Section  
 The following table lists the native-code interfaces that are exposed by the FTP service.  
  
|||  
|-|-|  
|Interface|Definition|  
|[IFtpAuthenticationProvider Interface](../../../reference/ftp/native-code/iftpauthenticationprovider-interface-native.md)|Provides an interface for authenticating an FTP user.|  
|[IFtpHomeDirectoryProvider Interface](../../../reference/ftp/native-code/iftphomedirectoryprovider-interface-native.md)|Provides an interface for retrieving the path to a user's FTP home directory.|  
|[IFtpLogProvider Interface](../../../reference/ftp/native-code/iftplogprovider-interface-native.md)|Provides an interface for logging FTP activity.|  
|[IFtpProviderConstruct Interface](../../../reference/ftp/native-code/iftpproviderconstruct-interface.md)|Provides an interface for passing configuration settings to a provider.|  
|[IFtpRoleProvider Interface](../../../reference/ftp/native-code/iftproleprovider-interface-native.md)|Provides an interface for FTP authorization and role checks.|  
  
## See Also  
 [FTP Native-Code Extensibility Structures](../../../reference/ftp/native-code/ftp-native-code-extensibility-structures.md)