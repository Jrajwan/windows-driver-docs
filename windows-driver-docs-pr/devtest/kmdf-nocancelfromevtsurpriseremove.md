---
title: NoCancelFromEvtSurpriseRemove rule (kmdf)
description: The NoCancelFromEvtSurpriseRemove rule specifies that WDF Drivers shouldn’t cancel requests from the EvtDeviceSurpriseRemoval callback function, instead self-managed I/O callback functions should be used.
ms.assetid: 15C95BD4-6D19-4CCA-9B2E-679B2F3058F1
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["NoCancelFromEvtSurpriseRemove rule (kmdf)"]
topic_type:
- apiref
api_name:
- NoCancelFromEvtSurpriseRemove
api_type:
- NA
ms.localizationpriority: medium
---

# NoCancelFromEvtSurpriseRemove rule (kmdf)


The **NoCancelFromEvtSurpriseRemove** rule specifies that WDF Drivers shouldn’t cancel requests from the [*EvtDeviceSurpriseRemoval*](https://msdn.microsoft.com/library/windows/hardware/ff540913) callback function, instead self-managed I/O callback functions should be used. *EvtDeviceSurpriseRemoval* callback function isn’t synchronized with the power-down path.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>NoCancelFromEvtSurpriseRemove</strong> rule.</p>
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

[**WdfIoQueueDrain**](https://msdn.microsoft.com/library/windows/hardware/ff547406)
[**WdfIoQueueDrainSynchronously**](https://msdn.microsoft.com/library/windows/hardware/ff547412)
[**WdfIoQueuePurge**](https://msdn.microsoft.com/library/windows/hardware/ff548442)
[**WdfIoQueuePurgeSynchronously**](https://msdn.microsoft.com/library/windows/hardware/ff548449)
[**WdfIoQueueStop**](https://msdn.microsoft.com/library/windows/hardware/ff548482)
[**WdfIoQueueStopAndPurge**](https://msdn.microsoft.com/library/windows/hardware/hh439289)
[**WdfIoQueueStopAndPurgeSynchronously**](https://msdn.microsoft.com/library/windows/hardware/hh439293)
[**WdfIoQueueStopSynchronously**](https://msdn.microsoft.com/library/windows/hardware/ff548489)
[**WdfRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff549945)
[**WdfRequestCompleteWithInformation**](https://msdn.microsoft.com/library/windows/hardware/ff549948)
[**WdfRequestCompleteWithPriorityBoost**](https://msdn.microsoft.com/library/windows/hardware/ff549949)
 

 





