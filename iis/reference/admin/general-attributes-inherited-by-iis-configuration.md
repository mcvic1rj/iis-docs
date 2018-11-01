---
title: "General Attributes Inherited by IIS Configuration | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e9ef2244-fd23-4d3c-ace3-5bb48696f69c
caps.latest.revision: 4
author: "shirhatti"
manager: "wpickett"
---
# General Attributes Inherited by IIS Configuration
The following table describes the general attributes that can be set for any section elements. These general attributes are also inherited by child elements of the section elements. All the attributes whose names include the work lock are designed to protect the specified content in the configuration file from being changed. No element or attribute is locked by default..  
  
## General Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|configSource|Specifies the name of a file in which the associated configuration section is defined. This attribute can be used to isolate configuration settings for multiple sites, for example, in a hosting environment.|  
|lockAllAttributesExcept|Locks all attributes of the parent element except the ones specified. Lower levels of the configuration hierarchy can never lock levels that are above them in the hierarchy.|  
|lockAllElementsExcept|Locks all child elements of the parent element except the ones specified.|  
|lockAttributes|Locks all attributes of the parent element.|  
|lockElements|Locks all child elements of the parent element.|  
|lockItem|Specifies true if the element on which the attribute occurs should be locked; otherwise, false. The default is false.<br /><br /> This attribute, besides being used to lock any individual element, can also be used on collection elements to lock them specifically within a specified collection. Also, the attribute can be used to lock any entire section.|  
  
## Remarks  
  
## Example