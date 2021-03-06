---
title: "OPENNEW Method (TestPage)"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: c484da23-ec11-4545-b52c-dab493291720
caps.latest.revision: 8
manager: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# OPENNEW Method (TestPage)
Opens a blank test page in edit mode.  
  
## Syntax  
  
```  
  
TestPage.OPENNEW  
```  
  
#### Parameters  
 *TestPage*  
 Type: TestPage  
  
 The test page variable that you use to refer to the new test page.  
  
## Remarks  
 If *TestPage* is already open, then a run-time error occurs, and the outcome of the test method is FAILURE.  
  
## Example  
 This example requires that you create a TestPage variable named CustTestPage with a Subtype of Customer List and that the codeunit in which you write the code is a test codeunit.  
  
```  
// Opens a blank Customer Card test page.   
CustTestPage.OPENNEW;  
```