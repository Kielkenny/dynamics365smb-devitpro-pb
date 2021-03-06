---
title: "AddNamespace Method"
ms.author: solsen
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 1
manager: edupont
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# AddNamespace Method
Adds the given namespace to the collection.  
```  
XmlNamespaceManager.AddNamespace(Prefix, Uri)  
```  
## Parameters
*Prefix*    
&emsp;Type: [String](../datatypes/devenv-text-data-type.md)  
The prefix to associate with the namespace being added. Use an empty string to add a default namespace.  
  
*Uri*    
&emsp;Type: [String](../datatypes/devenv-text-data-type.md)  
The namespace to add.  
  
## See Also
[XmlNamespaceManager](xmlnamespacemanager-class.md)  
[HTTP, JSON, TextBuilder, and XML API](../devenv-restapi-overview.md)  
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)  
