---
title: SetCompletionRoutineFromDispatch rule (kmdf)
description: The SetCompletionRoutineFromDispatch rule verifies that the driver does not specify a completion routine on an IRP from their EvtDeviceWdmIrpDispatch callback function.
ms.assetid: 2D7BA8DC-7288-4DE5-B335-A289C1E995AF
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["SetCompletionRoutineFromDispatch rule (kmdf)"]
topic_type:
- apiref
api_name:
- SetCompletionRoutineFromDispatch
api_type:
- NA
ms.localizationpriority: medium
---

# SetCompletionRoutineFromDispatch rule (kmdf)


The **SetCompletionRoutineFromDispatch** rule verifies that the driver does not specify a completion routine on an IRP from their [*EvtDeviceWdmIrpDispatch*](https://msdn.microsoft.com/library/windows/hardware/hh406404) callback function.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>SetCompletionRoutineFromDispatch</strong> rule.</p>
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
 

 





