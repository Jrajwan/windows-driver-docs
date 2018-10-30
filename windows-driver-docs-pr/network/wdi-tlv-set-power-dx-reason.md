---
title: WDI_TLV_SET_POWER_DX_REASON
author: windows-driver-content
description: WDI_TLV_SET_POWER_DX_REASON is a TLV that contains the reason for a set power Dx.
ms.assetid: 339F3461-3478-4C54-B6FB-9F5541859C76
ms.author: windowsdriverdev 
ms.date: 07/18/2017 
ms.topic: article 
ms.prod: windows-hardware 
ms.technology: windows-devices 
keywords:
 - WDI_TLV_SET_POWER_DX_REASON Network Drivers Starting with Windows Vista
ms.localizationpriority: medium
---

# WDI\_TLV\_SET\_POWER\_DX\_REASON


WDI\_TLV\_SET\_POWER\_DX\_REASON is a TLV that contains the reason for a set power Dx.

## TLV Type


0x103

## Length


The size (in bytes) of a UINT32.

## Values


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UINT32</td>
<td>The reason for a set power Dx.
<p>Valid values are:</p>
<ul>
<li><p>WDI_SET_POWER_DX_REASON_SELETIVE_SUSPEND (1)</p>
<p>When this value is set, it implies waking on any interesting external events without explicit [<strong>WDI_TLV_ENABLE_WAKE_EVENTS</strong>](wdi-tlv-enable-wake-events.md). This is an idle low power where the device functions transparently to end users as if it were in D0. See [WDI USB remote wake sequence](https://msdn.microsoft.com/library/windows/hardware/mt269159) for more information.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Minimum supported client</p></td>
<td><p>Windows 10</p></td>
</tr>
<tr class="even">
<td><p>Minimum supported server</p></td>
<td><p>Windows Server 2016</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td>Wditypes.hpp</td>
</tr>
</tbody>
</table>

 

 




