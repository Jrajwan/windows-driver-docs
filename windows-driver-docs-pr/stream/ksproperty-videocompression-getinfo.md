---
title: KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO
description: The KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO property retrieves the video compression capabilities of the device. This property must be implemented.
ms.assetid: 87e19e19-d90e-49c6-a6f0-cf33abf28c01
keywords: ["KSPROPERTY_VIDEOCOMPRESSION_GETINFO Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VIDEOCOMPRESSION_GETINFO
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

# KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO


The KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO property retrieves the video compression capabilities of the device. This property must be implemented.

## <span id="ddk_ksproperty_videocompression_getinfo_ks"></span><span id="DDK_KSPROPERTY_VIDEOCOMPRESSION_GETINFO_KS"></span>


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
<td><p>[<strong>KSPROPERTY_VIDEOCOMPRESSION_GETINFO_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565979)</p></td>
<td><p>[<strong>KSPROPERTY_VIDEOCOMPRESSION_GETINFO_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565979)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO\_S structure that specifies video compression settings such as the stream whose compression capabilities are to be queried, default key frame rate, default predicted frame rate, default quality setting, number of quality settings, and various compression capabilities.

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

[**KSPROPERTY\_VIDEOCOMPRESSION\_GETINFO\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565979)

 

 






