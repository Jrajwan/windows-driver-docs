---
title: DeviceCreateFail rule (kmdf)
description: The DeviceCreateFail rule specifies that EVT\_WDF\_DRIVER\_DEVICE\_ADD returns an error status when the call to WdfDeviceCreate fails.
ms.assetid: 07272d72-d9a2-42b2-b89b-c7bc903c1425
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["DeviceCreateFail rule (kmdf)"]
topic_type:
- apiref
api_name:
- DeviceCreateFail
api_type:
- NA
ms.localizationpriority: medium
---

# DeviceCreateFail rule (kmdf)


The **DeviceCreateFail** rule specifies that EVT\_WDF\_DRIVER\_DEVICE\_ADD returns an error status when the call to [**WdfDeviceCreate**](https://msdn.microsoft.com/library/windows/hardware/ff545926) fails.

For the driver to service a device, the device object must be created successfully.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>DeviceCreateFail</strong> rule.</p>
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
 

 





