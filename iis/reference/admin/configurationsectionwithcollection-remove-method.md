---
title: "ConfigurationSectionWithCollection.Remove Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 96394dd0-a3f3-196c-f70c-7b67b8e5a3ad
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationSectionWithCollection.Remove Method
Removes the specified element from a collection in a configuration section.  
  
## Syntax  
  
```jscript#  
ConfigurationSectionWithCollection.Remove collectionName, element;  
```  
  
```vbs  
ConfigurationSectionWithCollection.Remove collectionName, element  
```  
  
#### Parameters  
  
|Name|Definition|  
|----------|----------------|  
|`collectionName`|A `string` value that specifies the name of the collection that has an element to be removed.|  
|`element`|A [CollectionElement](../../reference/admin/collectionelement-class.md) object that contains the element to be removed.|  
  
## Return Value  
 This method does not return a value.  
  
## Example  
 The following example displays the names of the handlers for the default Web site, removes the handler element named "CGI-exe" if it is present, and then lists the handler names again. The code will cause the following XML to be added to the `<system.webServer>` section of the Web.config file for the default Web site:  
  
 `<handlers>`  
  
 `<remove name="CGI-exe" />`  
  
 `</handlers>`  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = GetObject("winmgmts:root\WebAdministration")  
  
' Get the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
  
' Get the handlers section.  
oSite.GetSection "HandlersSection", oHandlersSection  
  
' Display the current handler names.  
Wscript.Echo "---[Current Handler List]---"  
Call DisplayHandlerNames  
  
' Remove the CGI-exe handler by matching its name.  
For Each oHandler In oHandlersSection.Handlers  
     If oHandler.Name = "CGI-exe" Then  
        oHandlersSection.Remove "Handlers", oHandler  
    End If   
Next  
  
' Refresh the oHandlersSection object so that its contents will  
' reflect the updated configuration.  
oHandlersSection.Refresh_      
  
' List the handler names again to show the change.  
Wscript.Echo "---[New Handler List]---"  
Call DisplayHandlerNames  
  
' Provide a subroutine to display handler names.  
Sub DisplayHandlerNames  
    For Each oHandler In oHandlersSection.Handlers  
        WScript.Echo "Handler Name: " & oHandler.Name  
    Next  
    Wscript.Echo  
End Sub  
  
```  
  
 **Note** Calling the `Remove_` method updates the underlying configuration store but not the `oHandlersSection` object that is running in memory. Calling the `Refresh_` method on `oHandlersSection` will ensure that its data is accurate if you need to use it later in the same script.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [HandlerAction Class](../../reference/admin/handleraction-class.md)   
 [HandlersSection Class](../../reference/admin/handlerssection-class.md)