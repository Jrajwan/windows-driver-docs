---
title: NdisMIndicateStatusEx rule (ndis)
description: The driver must not call NdisMIndicateStatusEx after it returns from the MiniportHaltEx function.
ms.assetid: 488882DB-F294-40A1-BF35-E65262554E11
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["NdisMIndicateStatusEx rule (ndis)"]
topic_type:
- apiref
api_name:
- NdisMIndicateStatusEx
api_type:
- NA
ms.localizationpriority: medium
---

# NdisMIndicateStatusEx rule (ndis)


The driver must not call [**NdisMIndicateStatusEx**](https://msdn.microsoft.com/library/windows/hardware/ff563600) after it returns from the [*MiniportHaltEx*](https://msdn.microsoft.com/library/windows/hardware/ff559388) function.

|              |      |
|--------------|------|
| Driver model | NDIS |

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>NdisMIndicateStatusEx</strong> rule.</p>
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

[**NdisMIndicateStatusEx**](https://msdn.microsoft.com/library/windows/hardware/ff563600)
 

 





