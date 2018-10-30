---
title: KSPROPERTY\_EXTXPORT\_OUTPUT\_SIGNAL\_MODE
description: The KSPROPERTY\_EXTXPORT\_OUTPUT\_SIGNAL\_MODE property sets or gets an external device's output signal mode. For example DV-SD/NTSC/PAL, DV-SL/NTSC/PAL, MPEG2-TS, etc.
ms.assetid: 9cd1bf2a-c241-491a-af22-5cf7b654169d
keywords: ["KSPROPERTY_EXTXPORT_OUTPUT_SIGNAL_MODE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_EXTXPORT_OUTPUT_SIGNAL_MODE
api_location:
- ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_EXTXPORT\_OUTPUT\_SIGNAL\_MODE


The KSPROPERTY\_EXTXPORT\_OUTPUT\_SIGNAL\_MODE property sets or gets an external device's output signal mode. For example DV-SD/NTSC/PAL, DV-SL/NTSC/PAL, MPEG2-TS, etc.

## <span id="ddk_ksproperty_extxport_output_signal_mode_ks"></span><span id="DDK_KSPROPERTY_EXTXPORT_OUTPUT_SIGNAL_MODE_KS"></span>


### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

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
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property descriptor type</th>
<th>Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Device</p></td>
<td><p>[<strong>KSPROPERTY_EXTXPORT_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565167)</p></td>
<td><p>ULONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a ULONG that specifies the current output signal mode of the external transport.

Remarks
-------

The **SignalMode** member of the KSPROPERTY\_EXTXPORT\_S structure specifies the output signal mode.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

[**KSPROPERTY\_EXTXPORT\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565167)

 

 






