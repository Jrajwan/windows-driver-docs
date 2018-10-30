---
title: PowerDownFail rule (wdm)
description: The PowerDownFail rule specifies that a FDO or FIDO driver should not fail an IRP\_MN\_SET\_POWER request when the device is powering down. This rule only applies to FDO and FIDO drivers.
ms.assetid: 1C4CFF0D-E1E3-48CE-9F5A-C02BF95973C7
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["PowerDownFail rule (wdm)"]
topic_type:
- apiref
api_name:
- PowerDownFail
api_type:
- NA
ms.localizationpriority: medium
---

# PowerDownFail rule (wdm)


The **PowerDownFail** rule specifies that a FDO or FIDO driver should not fail an IRP\_MN\_SET\_POWER request when the device is powering down. This rule only applies to FDO and FIDO drivers.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>PowerDownFail</strong> rule.</p>
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

[**IoAcquireRemoveLock**](https://msdn.microsoft.com/library/windows/hardware/ff548204)
[**IoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff548336)
[**PoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff559654)
[**PoRequestPowerIrp**](https://msdn.microsoft.com/library/windows/hardware/ff559734)
 

 





