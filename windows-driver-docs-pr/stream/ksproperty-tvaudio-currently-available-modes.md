---
title: KSPROPERTY\_TVAUDIO\_CURRENTLY\_AVAILABLE\_MODES
description: The KSPROPERTY\_TVAUDIO\_CURRENTLY\_AVAILABLE\_MODES property retrieves TV audio modes that are available for the device. This property must be implemented.
ms.assetid: 9c98771a-7a41-469d-a441-da5c1ac5a697
keywords: ["KSPROPERTY_TVAUDIO_CURRENTLY_AVAILABLE_MODES Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_TVAUDIO_CURRENTLY_AVAILABLE_MODES
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

# KSPROPERTY\_TVAUDIO\_CURRENTLY\_AVAILABLE\_MODES


The KSPROPERTY\_TVAUDIO\_CURRENTLY\_AVAILABLE\_MODES property retrieves TV audio modes that are available for the device. This property must be implemented.

## <span id="ddk_ksproperty_tvaudio_currently_available_modes_ks"></span><span id="DDK_KSPROPERTY_TVAUDIO_CURRENTLY_AVAILABLE_MODES_KS"></span>


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
<td><p>[<strong>KSPROPERTY_TVAUDIO_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565953)</p></td>
<td><p>ULONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a ULONG that specifies the currently available TV audio modes, such as stereo or mono audio and multiple language settings.

Remarks
-------

The **Mode** member of the KSPROPERTY\_TVAUDIO\_S structure specifies the audio mode. It contains a bitwise ORing of the KS\_TVAUDIO\_MODE\_\* flags indicating the modes supported by the device at the time the information was requested.

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

[**KSPROPERTY\_TVAUDIO\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565953)

 

 






