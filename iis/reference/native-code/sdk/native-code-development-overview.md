---
title: "Native-Code Development Overview | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f7677287-55f8-40ac-94c0-fb2e0d8037ed
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# Native-Code Development Overview
IIS 7 and IIS 8 enable native-code developers to extend the Web server in a variety of new and powerful ways. For example, with the request-processing of IIS, native-code developers can create HTTP modules by using a rich set of APIs and a class-based configuration and notification infrastructure. With previous versions of IIS, such as IIS 6.0, developers could create HTTP modules by using only managed-code, and HTTP modules would process only [!INCLUDE[vstecasp](../../../reference/includes/vstecasp-md.md)] requests. With IIS 7 and IIS 8, developers can now create HTTP modules by using C++, and these modules can process all Web requests, not just [!INCLUDE[vstecasp](../../../reference/includes/vstecasp-md.md)] requests.  
  
## In This Section  
 [Creating Hosted Web Core Applications](../../../reference/native-code/sdk/creating-hosted-web-core-applications.md)  
 Describes how to create applications that use the new Hosted Web Core.  
  
 [Creating Native-Code HTTP Modules](../../../reference/native-code/sdk/creating-native-code-http-modules.md)  
 Describes how to create HTTP modules by using the new native-code extensibility features.  
  
## See Also  
 [Web Server Development Reference](../../../reference/web-server-development-reference.md)   
 [Native-Code API Reference](../../../web-dev-reference/native-code-api-ref/native-code-api-reference.md)