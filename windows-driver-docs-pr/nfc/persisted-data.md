---
title: Persisted data
author: windows-driver-content
description: Data persistence is.
ms.assetid: 61C3C55C-00DC-4A8C-B235-7C0391FB5119
keywords:
- NFC
- near field communications
- proximity
- near field proximity
- NFP
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Persisted data


Data persistence for the registry location is described as follows.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Location</th>
<th align="left">Contents, Usage, Defaults</th>
<th align="left">Access (if not default)</th>
<th align="left">PII stored?</th>
<th align="left">Is this setting migrated?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Device node registry location</td>
<td align="left">NfcRadioTurnedOff, DWORD:
<p>TRUE: NFC RM is off</p>
<p>FALSE: NFC RM is on and subject to idle power management</p></td>
<td align="left">Inherit from the device enum tree, no special ACL set</td>
<td align="left">N/A</td>
<td align="left">No</td>
</tr>
</tbody>
</table>

 

 

 
## Related topics
[NFC device driver interface (DDI) overview](https://msdn.microsoft.com/library/windows/hardware/mt715815)  
[NFC class extension (CX) reference](https://msdn.microsoft.com/library/windows/hardware/dn905536)  

