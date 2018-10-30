---
title: Driver-Specific Bins
author: windows-driver-content
description: Driver-Specific Bins
ms.assetid: 4c014e64-9e82-4058-9ec9-51769102f815
keywords:
- device-specific bins WDK printer
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Driver-Specific Bins


You are free to extend the bidi communications schema with driver-specific bin names. In this case, only the driver will be able to recognize the additional bin names.

```
<InputBin name="AAA" mibName="TRAY A"/>
```

The preceding code example results in the following four queries. Recall that an InputBin construct generates four new queries.

```
\Printer.Layout.InputBins.AAA:Installed
\Printer.Layout.InputBins.AAA:Level
\Printer.Layout.InputBins.AAA:MediaType
\Printer.Layout.InputBins.AAA:MediaSize

<OutputBin name="BBB" mibName="BIN B"/>
```

The preceding code example results in the following two queries. Recall that an OutputBin construct generates two new queries.

```
\Printer.Finishing.OutputBins.BBB:Installed
\Printer.Finishing.OutputBins.BBB:Level
```

 

 




