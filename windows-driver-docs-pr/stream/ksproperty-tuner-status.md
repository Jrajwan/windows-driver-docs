---
title: KSPROPERTY\_TUNER\_STATUS
description: The KSPROPERTY\_TUNER\_STATUS property retrieves information about the tuning process including the current frequency, phase locked loop (PLL) offset, and signal strength. This property must be implemented.
ms.assetid: 8613cda2-f39b-4363-a1c7-ac91162b9fca
keywords: ["KSPROPERTY_TUNER_STATUS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_TUNER_STATUS
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

# KSPROPERTY\_TUNER\_STATUS


The KSPROPERTY\_TUNER\_STATUS property retrieves information about the tuning process including the current frequency, phase locked loop (PLL) offset, and signal strength. This property must be implemented.

## <span id="ddk_ksproperty_tuner_status_ks"></span><span id="DDK_KSPROPERTY_TUNER_STATUS_KS"></span>


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
<td><p>[<strong>KSPROPERTY_TUNER_STATUS_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565925)</p></td>
<td><p>[<strong>KSPROPERTY_TUNER_STATUS_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565925)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSPROPERTY\_TUNER\_STATUS\_S structure that specifies the current frequency, PLL offset, and signal strength.

Remarks
-------

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

[**KSPROPERTY\_TUNER\_STATUS\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565925)

 

 






