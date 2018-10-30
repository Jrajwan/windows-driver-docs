---
title: ExclusiveResourceAccess rule (wdm)
description: The ExclusiveResourceAccess rule specifies that the driver calls ExAcquireResourceExclusiveLite before calling ExReleaseResourceLite or ExReleaseResourceForThreadLite and specifies that the driver calls ExReleaseResourceLite or ExReleaseResourceForThreadLite before any subsequent calls to ExAcquireResourceExclusiveLite.
ms.assetid: 3de539c0-5af2-4ced-8111-44918f4effc4
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["ExclusiveResourceAccess rule (wdm)"]
topic_type:
- apiref
api_name:
- ExclusiveResourceAccess
api_type:
- NA
ms.localizationpriority: medium
---

# ExclusiveResourceAccess rule (wdm)


The **ExclusiveResourceAccess** rule specifies that the driver calls [**ExAcquireResourceExclusiveLite**](https://msdn.microsoft.com/library/windows/hardware/ff544351) before calling [**ExReleaseResourceLite**](https://msdn.microsoft.com/library/windows/hardware/ff545597) or [**ExReleaseResourceForThreadLite**](https://msdn.microsoft.com/library/windows/hardware/ff545585) and specifies that the driver calls **ExReleaseResourceLite** or **ExReleaseResourceForThreadLite** before any subsequent calls to **ExAcquireResourceExclusiveLite**.

Nested calls are permitted if they are acquiring and releasing different resources. Nested calls to acquire or release the same resources violate this rule.

This rule also states that when the routine ends, the driver must not have exclusive access to the resource. Static Driver Verifier monitors the end of the **DriverEntry**, **AddDevice**, **StartIo**, **StartDevice**, **DpcForIsr**, **Cancel**, **Dispatch**, **RemoveDevice**, and **Unload** routines.

|              |     |
|--------------|-----|
| Driver model | WDM |

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left">Bug check(s) found with this rule</td>
<td align="left"></td>
</tr>
</tbody>
</table>

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>ExclusiveResourceAccess</strong> rule.</p>
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

[**ExAcquireResourceExclusiveLite**](https://msdn.microsoft.com/library/windows/hardware/ff544351)
[**ExReleaseResourceForThreadLite**](https://msdn.microsoft.com/library/windows/hardware/ff545585)
[**ExReleaseResourceLite**](https://msdn.microsoft.com/library/windows/hardware/ff545597)
See also
--------

[**Preventing Errors and Deadlocks While Using Spin Locks**](https://msdn.microsoft.com/library/windows/hardware/ff559854)
 

 





