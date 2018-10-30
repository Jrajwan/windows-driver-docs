---
title: '#Endif Conditional Preprocessor Directive'
author: windows-driver-content
description: '#Endif Conditional Preprocessor Directive'
ms.assetid: dfbfdb4a-955b-4ccf-b496-c8c5ddc42d2b
keywords:
- preprocessor directives WDK GDL , conditional directives
- directives WDK GDL , conditional directives
- conditional directives WDK GDL
- Endif directive WDK GDL
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# \#Endif Conditional Preprocessor Directive


```
#Endif:
```

The \#Endif directive defines the end of the previous section and the conditional construct. No symbol is used. You can use a fake symbol name as the value of the \#Endif directive to help the reader. Consider the following code example.

```
    #Ifdef: symbolA

        #Ifdef: symbolB

        #Elseifdef: symbolD

        #Endif: symbolB

    #Endif: symbolA
```

Indentation of each nested construct might also be helpful to the reader.

 

 




