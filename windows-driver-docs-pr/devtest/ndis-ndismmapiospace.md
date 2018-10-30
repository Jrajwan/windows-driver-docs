---
title: NdisMMapIoSpace rule (ndis)
description: The NdisMMapIoSpace function should only be called in the context of MiniportInitializeEx.
ms.assetid: C93420DB-ADB3-4C99-8D57-059B4650308D
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["NdisMMapIoSpace rule (ndis)"]
topic_type:
- apiref
api_name:
- NdisMMapIoSpace
api_type:
- NA
ms.localizationpriority: medium
---

# NdisMMapIoSpace rule (ndis)


The [**NdisMMapIoSpace**](https://msdn.microsoft.com/library/windows/hardware/ff563613) function should only be called in the context of [*MiniportInitializeEx*](https://msdn.microsoft.com/library/windows/hardware/ff559389).

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>NdisMMapIoSpace</strong> rule.</p>
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

[**NdisMMapIoSpace**](https://msdn.microsoft.com/library/windows/hardware/ff563613)
 

 





