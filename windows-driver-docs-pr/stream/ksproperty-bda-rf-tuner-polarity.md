---
title: KSPROPERTY\_BDA\_RF\_TUNER\_POLARITY
description: Clients use KSPROPERTY\_BDA\_RF\_TUNER\_POLARITY to control the polarity setting of the tuner node.
ms.assetid: 6778b4ac-2444-4e27-ab80-5802dda09fdd
keywords: ["KSPROPERTY_BDA_RF_TUNER_POLARITY Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_BDA_RF_TUNER_POLARITY
api_location:
- Bdamedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_BDA\_RF\_TUNER\_POLARITY


Clients use KSPROPERTY\_BDA\_RF\_TUNER\_POLARITY to control the polarity setting of the tuner node.

## <span id="ddk_ksproperty_bda_rf_tuner_polarity_ks"></span><span id="DDK_KSPROPERTY_BDA_RF_TUNER_POLARITY_KS"></span>


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
<td><p>KSP_NODE</p></td>
<td><p>ULONG</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The **NodeId** member of KSP\_NODE specifies the identifier of the tuner node.

The property value specifies the polarity to set for the transmitted signal.

For some transmissions, particularly satellite transmissions, the signal may be polarized. This property informs the tuner node about the polarization of the transmitted signal. The Polarization enumerated type contains values that specify the polarity of the signal.

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
<td>Bdamedia.h (include Bdamedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSP\_NODE**](https://msdn.microsoft.com/library/windows/hardware/ff566720)

[**Polarization**](https://msdn.microsoft.com/library/windows/hardware/ff567780)

 

 






