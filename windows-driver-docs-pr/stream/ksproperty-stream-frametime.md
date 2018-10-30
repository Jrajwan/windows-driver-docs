---
title: KSPROPERTY\_STREAM\_FRAMETIME
description: The KSPROPERTY\_STREAM\_FRAMETIME property allows a client to determine the duration of the next frame based on the particular media stream, and use that information to step-frame a sequence.
ms.assetid: 0cc218eb-1f21-4b45-ac48-b3e308bddfaf
keywords: ["KSPROPERTY_STREAM_FRAMETIME Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_STREAM_FRAMETIME
api_location:
- ks.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_STREAM\_FRAMETIME


The KSPROPERTY\_STREAM\_FRAMETIME property allows a client to determine the duration of the next frame based on the particular media stream, and use that information to step-frame a sequence.

## <span id="ddk_ksproperty_stream_frametime_ks"></span><span id="DDK_KSPROPERTY_STREAM_FRAMETIME_KS"></span>


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
<th>Property Descriptor Type</th>
<th>Property Value Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KSFRAMETIME</strong>](https://msdn.microsoft.com/library/windows/hardware/ff562558)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

KSPROPERTY\_STREAM\_FRAMETIME is an optional property that should be implemented if a pin recognizes the specifics of the media type it is transporting.

The property is supported by rendering pins and is used to return the duration of the next frame of data and any flags associated with that frame. A frame is generally the smallest usable unit into which the data can be split. For a video stream, this might be a video frame or a field. For audio, this would be a sample for each channel in the stream. For MIDI, this would be the next MIDI event.

The duration is measured in terms of the presentation time units provided by the pin. This is dependent on the interface and the numerator/denominator pair used in the presentation time. This does not apply to streams that are not oriented toward any specific media type, such as generic file readers.

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
<td>Ks.h (include Ks.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

[**KSFRAMETIME**](https://msdn.microsoft.com/library/windows/hardware/ff562558)

 

 






