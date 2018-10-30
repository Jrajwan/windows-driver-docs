---
title: MarkIrpPending2 rule (wdm)
description: The MarkIrpPending2 rule specifies that if a dispatch routine returns STATUS\_PENDING, it has called IoMarkIrpPending or passed the IRP to the lower driver. See MarkIrpPending for a complimentary specification.
ms.assetid: 91e22348-f5f3-4ba0-b8dd-ec0aa4b1df5e
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["MarkIrpPending2 rule (wdm)"]
topic_type:
- apiref
api_name:
- MarkIrpPending2
api_type:
- NA
ms.localizationpriority: medium
---

# MarkIrpPending2 rule (wdm)


The **MarkIrpPending2** rule specifies that if a dispatch routine returns STATUS\_PENDING, it has called [**IoMarkIrpPending**](https://msdn.microsoft.com/library/windows/hardware/ff549422) or passed the IRP to the lower driver. See [**MarkIrpPending**](wdm-markirppending.md) for a complimentary specification.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>MarkIrpPending2</strong> rule.</p>
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

[**IoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff548336)
[**IoMarkIrpPending**](https://msdn.microsoft.com/library/windows/hardware/ff549422)
[**KeWaitForSingleObject**](https://msdn.microsoft.com/library/windows/hardware/ff553350)
[**PoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff559654)
[**RemoveHeadList**](https://msdn.microsoft.com/library/windows/hardware/ff561032)
See also
--------

[**MarkIrpPending**](wdm-markirppending.md)
[**Synchronizing IRP Cancellation**](https://msdn.microsoft.com/library/windows/hardware/ff564531)
 

 





