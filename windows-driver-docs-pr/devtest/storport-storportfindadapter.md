---
title: StorPortFindAdapter rule (storport)
description: The HwStorFindAdapter routine must set the MaximumTransferLength and the NumberOfPhysicalBreaks fields in the PORT\_CONFIGURATION\_INFORMATION structure.
ms.assetid: 8BE79E99-078E-4CCE-A6C1-0DEB1F1252DA
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["StorPortFindAdapter rule (storport)"]
topic_type:
- apiref
api_name:
- StorPortFindAdapter
api_type:
- NA
ms.localizationpriority: medium
---

# StorPortFindAdapter rule (storport)


The [**HwStorFindAdapter**](https://msdn.microsoft.com/library/windows/hardware/ff557390) routine must set the **MaximumTransferLength** and the **NumberOfPhysicalBreaks** fields in the **PORT\_CONFIGURATION\_INFORMATION** structure. By default, the value of both these fields is **SP\_UNINITIALIZED\_VALUE**. If either of these fields is still set to **SP\_UNINITIALIZED\_VALUE** upon exit from **FindAdapter**, the driver fails the rule.

|              |          |
|--------------|----------|
| Driver model | Storport |

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>StorPortFindAdapter</strong> rule.</p>
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

 

 





