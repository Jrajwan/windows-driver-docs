---
title: KSPROPERTY\_VIDEOCOMPRESSION\_PFRAMES\_PER\_KEYFRAME
description: The KSPROPERTY\_VIDEOCOMPRESSION\_PFRAMES\_PER\_KEYFRAME property controls the predicted frame (P-Frame) interval. This property must be implemented.
ms.assetid: feb839b4-32fc-4fe9-b015-019d9d683c66
keywords: ["KSPROPERTY_VIDEOCOMPRESSION_PFRAMES_PER_KEYFRAME Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VIDEOCOMPRESSION_PFRAMES_PER_KEYFRAME
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

# KSPROPERTY\_VIDEOCOMPRESSION\_PFRAMES\_PER\_KEYFRAME


The KSPROPERTY\_VIDEOCOMPRESSION\_PFRAMES\_PER\_KEYFRAME property controls the predicted frame (P-Frame) interval. This property must be implemented.

## <span id="ddk_ksproperty_videocompression_pframes_per_keyframe_ks"></span><span id="DDK_KSPROPERTY_VIDEOCOMPRESSION_PFRAMES_PER_KEYFRAME_KS"></span>


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
<td><p>Filter</p></td>
<td><p>[<strong>KSPROPERTY_VIDEOCOMPRESSION_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566018)</p></td>
<td><p>LONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a LONG that specifies the number of predicted frames per key frame.

Remarks
-------

The **Value** member of the KSPROPERTY\_VIDEOCOMPRESSION\_S structure specifies the number of P-Frames per key frame. If a set request provides a negative **Value**, the minidriver should set the P-Frame rate to the default value.

Minidrivers that support this property should set the KS\_VideoCompressionCaps\_CanBFrame flag in the **Capabilities** member of the [**KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565979) structure that retrieves the minidriver's video compression capabilities.

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

[**KSPROPERTY\_VIDEOCOMPRESSION\_S**](https://msdn.microsoft.com/library/windows/hardware/ff566018)

[**KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565979)

 

 






