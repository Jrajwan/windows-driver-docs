---
title: BufAfterReqCompletedIoctlA rule (kmdf)
description: The BufAfterReqCompletedIoctlA rule specifies that within the EvtIoDeviceControl callback function, the I/O request buffer retrieved cannot be accessed after the I/O request is completed.
ms.assetid: c81f80b0-290e-41f1-b7df-9f6528261366
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["BufAfterReqCompletedIoctlA rule (kmdf)"]
topic_type:
- apiref
api_name:
- BufAfterReqCompletedIoctlA
api_type:
- NA
ms.localizationpriority: medium
---

# BufAfterReqCompletedIoctlA rule (kmdf)


The **BufAfterReqCompletedIoctlA** rule specifies that within the [*EvtIoDeviceControl*](https://msdn.microsoft.com/library/windows/hardware/ff541758) callback function, the I/O request buffer retrieved cannot be accessed after the I/O request is completed.

Within the driver's **EvtIoDeviceControl** callback function, the request buffer that was retrieved by calling [**WdfRequestRetrieveInputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550014), [**WdfRequestRetrieveOutputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550018), [**WdfRequestRetrieveUnsafeUserInputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550022), or [**WdfRequestRetrieveUnsafeUserOutputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550024) cannot be accessed after calling [**WdfRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff549945), [**WdfRequestCompleteWithInformation**](https://msdn.microsoft.com/library/windows/hardware/ff549948), or [**WdfRequestCompleteWithPriorityBoost**](https://msdn.microsoft.com/library/windows/hardware/ff549949) on the I/O request.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>BufAfterReqCompletedIoctlA</strong> rule.</p>
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

[**WDF\_MEMORY\_DESCRIPTOR\_INIT\_BUFFER**](https://msdn.microsoft.com/library/windows/hardware/ff552393)
[**WdfMemoryAssignBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548697)
[**WdfMemoryCopyFromBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548701)
[**WdfMemoryCopyToBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548703)
[**WdfMemoryCreatePreallocated**](https://msdn.microsoft.com/library/windows/hardware/ff548712)
[**WdfRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff549945)
[**WdfRequestCompleteWithInformation**](https://msdn.microsoft.com/library/windows/hardware/ff549948)
[**WdfRequestCompleteWithPriorityBoost**](https://msdn.microsoft.com/library/windows/hardware/ff549949)
[**WdfRequestRetrieveInputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550014)
[**WdfRequestRetrieveOutputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550018)
[**WdfRequestRetrieveUnsafeUserInputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550022)
[**WdfRequestRetrieveUnsafeUserOutputBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff550024)
[**RtlCompareMemory**](https://msdn.microsoft.com/library/windows/hardware/ff561778)
[**RtlMoveMemory**](https://msdn.microsoft.com/library/windows/hardware/ff562030)
[**RtlZeroMemory**](https://msdn.microsoft.com/library/windows/hardware/ff563610)
[**ZwReadFile**](https://msdn.microsoft.com/library/windows/hardware/ff567072)
See also
--------

[**BufAfterReqCompletedIoctl**](kmdf-bufafterreqcompletedioctl.md)
 

 





