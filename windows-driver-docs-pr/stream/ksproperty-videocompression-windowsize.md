---
title: KSPROPERTY\_VIDEOCOMPRESSION\_WINDOWSIZE
description: The KSPROPERTY\_VIDEOCOMPRESSION\_WINDOWSIZE property controls the data rate that describes the average frame size. This property must be implemented.
ms.assetid: 44cf4bb6-7ddb-4a72-8a77-7dc390aa8c12
keywords: ["KSPROPERTY_VIDEOCOMPRESSION_WINDOWSIZE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VIDEOCOMPRESSION_WINDOWSIZE
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

# KSPROPERTY\_VIDEOCOMPRESSION\_WINDOWSIZE


The KSPROPERTY\_VIDEOCOMPRESSION\_WINDOWSIZE property controls the data rate that describes the average frame size. This property must be implemented.

## <span id="ddk_ksproperty_videocompression_windowsize_ks"></span><span id="DDK_KSPROPERTY_VIDEOCOMPRESSION_WINDOWSIZE_KS"></span>


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

 

The property value (operation data) is a LONG that specifies a data rate that represents the average frame size.

Remarks
-------

The **Value** member of the KSPROPERTY\_VIDEOCOMPRESSION\_S structure specifies the window size.

Minidrivers that support this property should set the **KS\_CompressionCaps\_CanWindow** flag in the **Capabilities** member of the [**KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565979) structure that retrieves the minidriver's video compression capabilities. If a minidriver sets the **KS\_CompressionCaps\_CanWindow** flag, it should provide both get and set support for the property.

For a window of size *n,* the average frame size of any consecutive *n* frames must not exceed the stream's specified data rate, although *individual* frames may be larger or smaller. For example, if the data rate has been set to 150 kilobytes per second (KBps) on a 15 frame per second (fps) movie, the *average* size of each frame must therefore be less than or equal to 10 kilobytes. Individual frames may be larger or smaller just so long as the average size (calculated across 15 frames per second of movie) is less than or equal to 10 kilobytes.

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

 

 






