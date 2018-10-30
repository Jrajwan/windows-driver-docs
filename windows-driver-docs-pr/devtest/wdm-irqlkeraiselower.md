---
title: IrqlKeRaiseLower rule (wdm)
description: The IrqlKeRaiseLower rule specifies that the driver does the following when raising and lowering the IRQL When the driver calls KeRaiseIrql, it is executing at an IRQL that is lower than or equal to the value of the NewIrql parameter.The driver calls KeLowerIrql only after calling KeRaiseIrql or KeRaiseIrqlToDpcLevel.
ms.assetid: 61f7e5bc-ccc5-4ee6-a580-9935a01f96e6
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["IrqlKeRaiseLower rule (wdm)"]
topic_type:
- apiref
api_name:
- IrqlKeRaiseLower
api_type:
- NA
ms.localizationpriority: medium
---

# IrqlKeRaiseLower rule (wdm)


The **IrqlKeRaiseLower** rule specifies that the driver does the following when raising and lowering the IRQL:

When the driver calls [**KeRaiseIrql**](https://msdn.microsoft.com/library/windows/hardware/ff553079), it is executing at an IRQL that is lower than or equal to the value of the *NewIrql* parameter.
The driver calls [**KeLowerIrql**](https://msdn.microsoft.com/library/windows/hardware/ff552968) only after calling **KeRaiseIrql** or [**KeRaiseIrqlToDpcLevel**](https://msdn.microsoft.com/library/windows/hardware/ff553084).
This rule permits nested calls to **KeRaiseIrql**, **KeRaiseIrqlToDpcLevel**, and **KeLowerIrql**.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>IrqlKeRaiseLower</strong> rule.</p>
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

[**KeLowerIrql**](https://msdn.microsoft.com/library/windows/hardware/ff552968)
[**KeRaiseIrql**](https://msdn.microsoft.com/library/windows/hardware/ff553079)
See also
--------

[**IrqlKeDispatchLte**](wdm-irqlkedispatchlte.md)
[**IrqlKeRaiseLower2**](wdm-irqlkeraiselower2.md)
 

 





