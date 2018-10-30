---
title: Irql\_MCM\_Function rule (ndis)
description: The Irql\_MCM\_Function rule specifies that the NDIS MCM functions for drivers must be called at correct IRQL levels.
ms.assetid: 8cd71bf0-92ee-409d-90e3-6bb0c14ebda4
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["Irql_MCM_Function rule (ndis)"]
topic_type:
- apiref
api_name:
- Irql_MCM_Function
api_type:
- NA
ms.localizationpriority: medium
---

# Irql\_MCM\_Function rule (ndis)


The **Irql\_MCM\_Function** rule specifies that the NDIS MCM functions for drivers must be called at correct IRQL levels.

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>Irql_MCM_Function</strong> rule.</p>
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

[**NdisMCmActivateVc**](https://msdn.microsoft.com/library/windows/hardware/ff562792)
[**NdisMCmAddPartyComplete**](https://msdn.microsoft.com/library/windows/hardware/ff562798)
[**NdisMCmCloseAddressFamilyComplete**](https://msdn.microsoft.com/library/windows/hardware/ff562800)
[**NdisMCmCloseCallComplete**](https://msdn.microsoft.com/library/windows/hardware/ff562803)
[**NdisMCmCreateVc**](https://msdn.microsoft.com/library/windows/hardware/ff562812)
[**NdisMCmDeactivateVc**](https://msdn.microsoft.com/library/windows/hardware/ff562818)
[**NdisMCmDeleteVc**](https://msdn.microsoft.com/library/windows/hardware/ff562819)
[**NdisMCmDeregisterSapComplete**](https://msdn.microsoft.com/library/windows/hardware/ff562821)
[**NdisMCmDispatchCallConnected**](https://msdn.microsoft.com/library/windows/hardware/ff562826)
[**NdisMCmDispatchIncomingCall**](https://msdn.microsoft.com/library/windows/hardware/ff562830)
[**NdisMCmDispatchIncomingCallQoSChange**](https://msdn.microsoft.com/library/windows/hardware/ff563540)
[**NdisMCmDispatchIncomingCloseCall**](https://msdn.microsoft.com/library/windows/hardware/ff563541)
[**NdisMCmDispatchIncomingDropParty**](https://msdn.microsoft.com/library/windows/hardware/ff563542)
[**NdisMCmDropPartyComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563543)
[**NdisMCmMakeCallComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563544)
[**NdisMCmModifyCallQoSComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563545)
[**NdisMCmNotifyCloseAddressFamily**](https://msdn.microsoft.com/library/windows/hardware/ff563546)
[**NdisMCmOidRequest**](https://msdn.microsoft.com/library/windows/hardware/ff563548)
[**NdisMCmOidRequestComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563551)
[**NdisMCmOpenAddressFamilyComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563552)
[**NdisMCmRegisterAddressFamilyEx**](https://msdn.microsoft.com/library/windows/hardware/ff563554)
[**NdisMCmRegisterSapComplete**](https://msdn.microsoft.com/library/windows/hardware/ff563557)
 

 





