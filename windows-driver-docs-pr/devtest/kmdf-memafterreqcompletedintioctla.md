---
title: MemAfterReqCompletedIntIoctlA rule (kmdf)
description: The MemAfterReqCompletedIntIoctlA rule specifies that within the EvtIoInternalDeviceControl callback function, the framework memory object cannot be accessed after the I/O request is completed.
ms.assetid: ff64d344-8b8e-4dec-adc3-d1e99f737e8a
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["MemAfterReqCompletedIntIoctlA rule (kmdf)"]
topic_type:
- apiref
api_name:
- MemAfterReqCompletedIntIoctlA
api_type:
- NA
ms.localizationpriority: medium
---

# MemAfterReqCompletedIntIoctlA rule (kmdf)


The **MemAfterReqCompletedIntIoctlA** rule specifies that within the [*EvtIoInternalDeviceControl*](https://msdn.microsoft.com/library/windows/hardware/ff541768) callback function, the framework memory object cannot be accessed after the I/O request is completed.

Within the driver's *EvtIoInternalDeviceControl* callback function, the framework memory object that was retrieved by calling the [**WdfRequestRetrieveInputMemory**](https://msdn.microsoft.com/library/windows/hardware/ff550015) or [**WdfRequestRetrieveOutputMemory**](https://msdn.microsoft.com/library/windows/hardware/ff550019) methods cannot be accessed after calling [**WdfRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff549945), [**WdfRequestCompleteWithInformation**](https://msdn.microsoft.com/library/windows/hardware/ff549948), or [**WdfRequestCompleteWithPriorityBoost**](https://msdn.microsoft.com/library/windows/hardware/ff549949) on the I/O request.

This rule considers the following memory access methods:

[**WdfMemoryGetBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548715)
[**WDF\_MEMORY\_DESCRIPTOR\_INIT\_HANDLE**](https://msdn.microsoft.com/library/windows/hardware/ff552395)
[**WdfMemoryAssignBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548697)
[**WdfMemoryCopyToBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548703)
[**WdfMemoryCopyFromBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548701)
[**WdfObjectReference**](https://msdn.microsoft.com/library/windows/hardware/ff548758)
[**WdfObjectDereference**](https://msdn.microsoft.com/library/windows/hardware/ff548739)
[**WdfObjectDelete**](https://msdn.microsoft.com/library/windows/hardware/ff548734)
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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>MemAfterReqCompletedIntIoctlA</strong> rule.</p>
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

[**WDF\_MEMORY\_DESCRIPTOR\_INIT\_HANDLE**](https://msdn.microsoft.com/library/windows/hardware/ff552395)
[**WdfMemoryAssignBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548697)
[**WdfMemoryCopyFromBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548701)
[**WdfMemoryCopyToBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548703)
[**WdfMemoryGetBuffer**](https://msdn.microsoft.com/library/windows/hardware/ff548715)
[**WdfObjectDelete**](https://msdn.microsoft.com/library/windows/hardware/ff548734)
[**WdfObjectDereference**](https://msdn.microsoft.com/library/windows/hardware/ff548739)
[**WdfObjectReference**](https://msdn.microsoft.com/library/windows/hardware/ff548758)
[**WdfRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff549945)
[**WdfRequestCompleteWithInformation**](https://msdn.microsoft.com/library/windows/hardware/ff549948)
[**WdfRequestCompleteWithPriorityBoost**](https://msdn.microsoft.com/library/windows/hardware/ff549949)
[**WdfRequestRetrieveInputMemory**](https://msdn.microsoft.com/library/windows/hardware/ff550015)
[**WdfRequestRetrieveOutputMemory**](https://msdn.microsoft.com/library/windows/hardware/ff550019)
 

 





