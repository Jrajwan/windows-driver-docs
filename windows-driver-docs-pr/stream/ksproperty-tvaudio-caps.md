---
title: KSPROPERTY\_TVAUDIO\_CAPS
description: The KSPROPERTY\_TVAUDIO\_CAPS property retrieves the capabilities of the TV audio device. This property must be implemented.
ms.assetid: a5b7348e-0f85-430c-acf0-c35e289ef338
keywords: ["KSPROPERTY_TVAUDIO_CAPS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_TVAUDIO_CAPS
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

# KSPROPERTY\_TVAUDIO\_CAPS


The KSPROPERTY\_TVAUDIO\_CAPS property retrieves the capabilities of the TV audio device. This property must be implemented.

## <span id="ddk_ksproperty_tvaudio_caps_ks"></span><span id="DDK_KSPROPERTY_TVAUDIO_CAPS_KS"></span>


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
<td><p>[<strong>KSPROPERTY_TVAUDIO_CAPS_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565936)</p></td>
<td><p>ULONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a ULONG that specifies the capabilities of the TV audio device, such as stereo versus mono audio support and multiple language capabilities.

Remarks
-------

The **Capabilities** member of the KSPROPERTY\_TVAUDIO\_CAPS\_S structure specifies the capabilities of the TV audio device.

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

[**KSPROPERTY\_TVAUDIO\_CAPS\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565936)

 

 






