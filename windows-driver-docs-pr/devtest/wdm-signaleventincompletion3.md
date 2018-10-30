---
title: SignalEventInCompletion3 rule (wdm)
description: The SignalEventInCompletion3 rule specifies that when processing a asynchronous IRP, the driver needs to call the KeSetEvent in the completion routine when the Irp- PendingReturned flag is set.
ms.assetid: 1FCEB660-A156-4B70-9121-FF166C629FF8
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["SignalEventInCompletion3 rule (wdm)"]
topic_type:
- apiref
api_name:
- SignalEventInCompletion3
api_type:
- NA
ms.localizationpriority: medium
---

# SignalEventInCompletion3 rule (wdm)


The **SignalEventInCompletion3** rule specifies that when processing a asynchronous IRP, the driver needs to call the [**KeSetEvent**](https://msdn.microsoft.com/library/windows/hardware/ff553253) in the completion routine when the **Irp-&gt;PendingReturned** flag is set.

In this case, the completion routine will not be called.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>SignalEventInCompletion3</strong> rule.</p>
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

[**IoSetCompletionRoutine**](https://msdn.microsoft.com/library/windows/hardware/ff549679)
[**IoSetCompletionRoutineEx**](https://msdn.microsoft.com/library/windows/hardware/ff549686)
[**KeInitializeEvent**](https://msdn.microsoft.com/library/windows/hardware/ff552137)
 

 





