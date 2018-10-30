---
title: KSPROPERTY\_VIDEODECODER\_CAPS
description: The KSPROPERTY\_VIDEODECODER\_CAPS property describes the basic capabilities of a video decoder. This property must be implemented.
ms.assetid: 8b252f36-911b-4f51-894d-3aae9aa9dfde
keywords: ["KSPROPERTY_VIDEODECODER_CAPS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VIDEODECODER_CAPS
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

# KSPROPERTY\_VIDEODECODER\_CAPS


The KSPROPERTY\_VIDEODECODER\_CAPS property describes the basic capabilities of a video decoder. This property must be implemented.

## <span id="ddk_ksproperty_videodecoder_caps_ks"></span><span id="DDK_KSPROPERTY_VIDEODECODER_CAPS_KS"></span>


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
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY_VIDEODECODER_CAPS_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566047)</p></td>
<td><p>[<strong>KSPROPERTY_VIDEODECODER_CAPS_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566047)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSPROPERTY\_VIDEODECODER\_CAPS\_S structure that specifies the hardware capabilities of the video decoder device, such as supported standards, settling time, and horizontal sync pulses the video decoder produces during the vertical sync period.

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

[**KSPROPERTY\_VIDEODECODER\_CAPS\_S**](https://msdn.microsoft.com/library/windows/hardware/ff566047)

 

 






