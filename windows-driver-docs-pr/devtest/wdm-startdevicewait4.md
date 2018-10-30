---
title: StartDeviceWait4 rule (wdm)
description: The StartDeviceWait4 rule specifies that the driver should not call KeWaitForSingleObject in the context of start device IRP.
ms.assetid: 075DCDD2-CFC5-4508-A1B3-0D506CA50B58
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["StartDeviceWait4 rule (wdm)"]
topic_type:
- apiref
api_name:
- StartDeviceWait4
api_type:
- NA
ms.localizationpriority: medium
---

# StartDeviceWait4 rule (wdm)


The **StartDeviceWait4** rule specifies that the driver should not call [**KeWaitForSingleObject**](https://msdn.microsoft.com/library/windows/hardware/ff553350) in the context of start device IRP.

|              |     |
|--------------|-----|
| Driver model | WDM |

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>StartDeviceWait4</strong> rule.</p>
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

[**IoSetCompletionRoutineEx**](https://msdn.microsoft.com/library/windows/hardware/ff549686)
[**KeWaitForSingleObject**](https://msdn.microsoft.com/library/windows/hardware/ff553350)
 

 





