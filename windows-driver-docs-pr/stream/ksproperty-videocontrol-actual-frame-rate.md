---
title: KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE
description: The KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE property retrieves the frame rate at which the device is streaming for the specified pin. This property is optional.
ms.assetid: 1681bb54-bdd8-499d-b544-c0e8b14deaa5
keywords: ["KSPROPERTY_VIDEOCONTROL_ACTUAL_FRAME_RATE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VIDEOCONTROL_ACTUAL_FRAME_RATE
api_location:
- Ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE


The KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE property retrieves the frame rate at which the device is streaming for the specified pin. This property is optional.

## <span id="ddk_ksproperty_videocontrol_actual_frame_rate_ks"></span><span id="DDK_KSPROPERTY_VIDEOCONTROL_ACTUAL_FRAME_RATE_KS"></span>


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
<td><p>No</p></td>
<td><p>Filter</p></td>
<td><p>[<strong>KSPROPERTY_VIDEOCONTROL_ACTUAL_FRAME_RATE_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566031)</p></td>
<td><p>KSPROPERTY_VIDEOCONTROL</p>
<p>_ACTUAL_FRAME_RATE_S</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE\_S structure that specifies actual frame rate information at the time of query, such as the dimensions (width and height) of the image, current actual frame rate, and current maximum available frame rate.

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

[**KSPROPERTY\_VIDEOCONTROL\_ACTUAL\_FRAME\_RATE\_S**](https://msdn.microsoft.com/library/windows/hardware/ff566031)

 

 






