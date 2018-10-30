---
title: Activity sensor properties
author: windows-driver-content
description: The property keys for the activity sensor.
ms.assetid: 9C5DCE23-2690-4A22-8E38-D0571F997646
ms.author: windowsdriverdev
ms.date: 01/04/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Activity sensor properties


The property keys for the activity sensor.

|Property key|Type|Required/Optional|Description|
| --- | --- | --- | --- |
|PKEY_SensorData_SupportedActivityStates|VT_UI4|R/O|Required|The supported activity states.|
|PKEY_SensorData_MinimumDetectionIntervals_Ms|VT_VECTOR | VT_UI4|R/O|Required|The minimum time interval, expressed in milliseconds, for sampling activity data.|
 

For more information about the data types shown in the **Type** column, see [PROPVARIANT structure](http://go.microsoft.com/fwlink/p/?linkid=313395).

## Requirements


**Header:** Sensorsdef.h

## Related topics


[Other sensor properties](other-sensor-properties.md)

 

 






