---
title: "APPLICATIONPATH Method"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 6fb5a2e1-5eb8-44c1-8247-33643182cf22
author: SusanneWindfeldPedersen
manager: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# APPLICATIONPATH Method
Returns the path of the directory where the executable file for [!INCLUDE[d365fin_md](../includes/d365fin_md.md)] is installed.  

## Syntax  

```  

APPLICATIONPATH  
```  

## Remarks  
 This method returns a string that contains the path of the directory where the executable file for [!INCLUDE[d365fin_md](../includes/d365fin_md.md)] is installed. This string ends with a backslash \('\\'\) and does not contain the name of the executable file.  

 The string cannot contain more than 255 characters.  

 If this method is called from an application that is running on a [!INCLUDE[d365fin_md](../includes/d365fin_md.md)] Application Server, it returns the path of the directory where the [!INCLUDE[d365fin_md](../includes/d365fin_md.md)] Application Server is installed.  

## See Also  
 [GUIALLOWED Method](devenv-GUIALLOWED-Method.md)   
 [HYPERLINK Method](devenv-HYPERLINK-Method.md)   
 [SLEEP Method](devenv-SLEEP-Method.md)   
 [TEMPORARYPATH Method](devenv-TEMPORARYPATH-Method.md)
