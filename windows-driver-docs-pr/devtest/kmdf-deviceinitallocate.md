---
title: DeviceInitAllocate rule (kmdf)
description: The DeviceInitAllocate rule specifies that, for a PDO device or a control device object, the framework device object initialization methods WdfPdoInitAllocate or WdfControlDeviceInitAllocate must be called before the driver calls WdfDeviceCreate.
ms.assetid: 81bad62a-4bc3-4e34-9634-2a980e1941e5
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["DeviceInitAllocate rule (kmdf)"]
topic_type:
- apiref
api_name:
- DeviceInitAllocate
api_type:
- NA
ms.localizationpriority: medium
---

# DeviceInitAllocate rule (kmdf)


The **DeviceInitAllocate** rule specifies that, for a PDO device or a control device object, the framework device object initialization methods [**WdfPdoInitAllocate**](https://msdn.microsoft.com/library/windows/hardware/ff548786) or [**WdfControlDeviceInitAllocate**](https://msdn.microsoft.com/library/windows/hardware/ff545841) must be called before the driver calls [**WdfDeviceCreate**](https://msdn.microsoft.com/library/windows/hardware/ff545926).

|              |      |
|--------------|------|
| Driver model | KMDF |

How to test
-----------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">At compile time</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>DeviceInitAllocate</strong> rule.</p>
Use the following steps to run an analysis of your code:
<ol>
<li>[Prepare your code (use role type declarations).](https://msdn.microsoft.com/library/windows/hardware/hh454281#preparing-your-source-code)</li>
<li>[Run Static Driver Verifier.](https://msdn.microsoft.com/library/windows/hardware/hh454281#running-static-driver-verifier)</li>
<li>[View and analyze the results.](https://msdn.microsoft.com/library/windows/hardware/hh454281#viewing-and-analyzing-the-results)</li>
</ol>
<p>For more information, see [Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281).</p></td>
</tr>
</tbody>
</table>

Applies to
----------

[**WdfDeviceCreate**](https://msdn.microsoft.com/library/windows/hardware/ff545926)
 

 





