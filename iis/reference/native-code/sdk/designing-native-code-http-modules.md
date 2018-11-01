---
title: "Designing Native-Code HTTP Modules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7af6e299-ae44-4d9b-911f-0d29f19daf2a
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# Designing Native-Code HTTP Modules
HTTP modules in [!INCLUDE[iisver](../../../reference/admin/includes/iisver-md.md)] enable developers to extend or replace core IIS functionality. For example, you could write a digest authentication module that replaces the module that is included with [!INCLUDE[iisver](../../../reference/admin/includes/iisver-md.md)]. Although some of the functionality provided by native-code modules may resemble functionality that was previously available with ISAPI filters, native-code modules are designed differently and provide a much richer feature set than ISAPI filters.  
  
## Requirements for Native-Code HTTP Modules  
  
### Adding an Exported Registration Function  
 HTTP modules are required to export a [RegisterModule](../../../web-dev-reference/native-code-api-ref/pfn-registermodule-function.md) function. You can export this function by creating a module definition (.def) file for your project, or you can compile the module by using the **/EXPORT:RegisterModule** switch.  
  
### Specifying Notifications and Module Priority  
 When you create your `RegisterModule` function, you specify a bitmask that contains a list of notifications that your request-level module will process (for more information, see [Request-Processing Constants](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md)). For example, a request-level module could specify that it will provide methods to process the [RQ_BEGIN_REQUEST](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) notification and the [RQ_MAP_PATH](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) post-notification. Similarly, a global-level module could specify that it will provide methods to process the [GL_APPLICATION_START](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) and the [GL_APPLICATION_STOP](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) notifications.  
  
 The `RegisterModule` function also lets you specify the priority for the module. The available priorities are `PRIORITY_ALIAS_FIRST`, `PRIORITY_ALIAS_HIGH`, `PRIORITY_ALIAS_MEDIUM`, `PRIORITY_ALIAS_LOW`, and `PRIORITY_ALIAS_LAST`. When modules are registered, they are processed in order of priority and configuration settings. For example, if you create an HTTP module that registers as a medium-priority module, your module will not be processed until all of the high-priority modules have been processed. You can configure your module to be processed before other medium-priority modules, and your module will be processed before any low-priority modules.  
  
> [!NOTE]
>  The order of priority levels is inverted for `RQ_SEND_RESPONSE` notifications.  
  
## Creating Request-Level Modules  
  
### Creating a Module Factory  
 Native-code request-level modules must provide a module factory that creates an instance of the [CHttpModule](../../../web-dev-reference/native-code-api-ref/chttpmodule-class.md) class. The module factory will inherit from the [IHttpModuleFactory](../../../web-dev-reference/native-code-api-ref/ihttpmodulefactory-interface.md) interface.  
  
 For more information about how to create a module factory, see the code example in [Walkthrough: Creating a Request-Level HTTP Module By Using Native Code](../../../reference/native-code/sdk/walkthrough-creating-a-request-level-http-module-by-using-native-code.md).  
  
### Creating a Class That Is Derived from CHttpModule  
 The main processing functionality for request-level HTTP modules is provided through a module that is derived from the base `CHttpModule` class. This class must contain a callback method for each notification or post-notification that is listed in the `RegisterModule` function. For example, if your module is registered for the [RQ_AUTHENTICATE_REQUEST](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) notification and the [RQ_AUTHORIZE_REQUEST](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) post-notification, your class must contain [OnAuthenticateRequest](../../../web-dev-reference/native-code-api-ref/chttpmodule-onauthenticaterequest-method.md) and [OnPostAuthorizeRequest](../../../web-dev-reference/native-code-api-ref/chttpmodule-onpostauthorizerequest-method.md) methods.  
  
### Returning from CHttpModule Methods  
 When methods in the `CHttpModule` class have finished processing, each method must return a [REQUEST_NOTIFICATION_STATUS](../../../web-dev-reference/native-code-api-ref/request-notification-status-enumeration.md) enumeration value. This value determines how IIS will handle the exit condition of the class methods. For example, a return value of [RQ_NOTIFICATION_CONTINUE](../../../web-dev-reference/native-code-api-ref/request-notification-status-enumeration.md) informs IIS to continue processing the request. In contrast, a return value of [RQ_NOTIFICATION_FINISH_REQUEST](../../../web-dev-reference/native-code-api-ref/request-notification-status-enumeration.md) instructs IIS to cease processing on the current request.  
  
### CHttpModule Cleanup  
 When a module has finished processing, IIS will call the module's [CHttpModule::Dispose](../../../web-dev-reference/native-code-api-ref/chttpmodule-dispose-method.md) method to remove the `CHttpModule` class from memory.  
  
## Creating a Global-Level Module  
  
### Creating a Class That Is Derived from CGlobalModule  
 The main processing functionality for global-level HTTP modules is provided through a module that is derived from the base [CGlobalModule](../../../web-dev-reference/native-code-api-ref/cglobalmodule-class.md) class. This class must contain a callback method for each notification that is listed in the `RegisterModule` function. For example, if your module is registered for the [GL_APPLICATION_START](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) and the [GL_APPLICATION_STOP](../../../web-dev-reference/native-code-api-ref/request-processing-constants.md) notifications, your class must contain [OnGlobalApplicationStart](../../../web-dev-reference/native-code-api-ref/cglobalmodule-onglobalapplicationstart-method.md) and [OnGlobalApplicationStop](../../../web-dev-reference/native-code-api-ref/cglobalmodule-onglobalapplicationstop-method.md) methods.  
  
### Returning from CGlobalModule Methods  
 When methods in the `CGlobalModule` class have finished processing, each method must return a [GLOBAL_NOTIFICATION_STATUS](../../../web-dev-reference/native-code-api-ref/global-notification-status-enumeration.md) enumeration value. This value determines how IIS will handle the exit condition of the class methods. For example, a return value of [GL_NOTIFICATION_CONTINUE](../../../web-dev-reference/native-code-api-ref/global-notification-status-enumeration.md) informs IIS to continue processing the notification. In contrast, a return value of [GL_NOTIFICATION_HANDLED](../../../web-dev-reference/native-code-api-ref/global-notification-status-enumeration.md) instructs IIS to cease processing on the current notification.  
  
### CGlobalModule Cleanup  
 When a module has finished processing, IIS will call the module's [CGlobalModule::Terminate](../../../web-dev-reference/native-code-api-ref/cglobalmodule-terminate-method.md) method. Your module should use this method to remove your `CGlobalModule` class from memory.  
  
## See Also  
 [Walkthrough: Creating a Request-Level HTTP Module By Using Native Code](../../../reference/native-code/sdk/walkthrough-creating-a-request-level-http-module-by-using-native-code.md)   
 [Walkthrough: Creating a Global-Level HTTP Module By Using Native Code](../../../reference/native-code/sdk/walkthrough-creating-a-global-level-http-module-by-using-native-code.md)   
 [Creating Native-Code HTTP Modules](../../../reference/native-code/sdk/creating-native-code-http-modules.md)