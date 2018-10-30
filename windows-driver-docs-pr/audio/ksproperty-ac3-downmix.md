---
title: KSPROPERTY\_AC3\_DOWNMIX
description: The KSPROPERTY\_AC3\_DOWNMIX property specifies whether the program channels in an AC-3-encoded stream need to be downmixed to accommodate the speaker configuration.
ms.assetid: 1d47f890-f7da-423f-adef-72b06a0f79d8
keywords: ["KSPROPERTY_AC3_DOWNMIX Audio Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_AC3_DOWNMIX
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

# KSPROPERTY\_AC3\_DOWNMIX


The KSPROPERTY\_AC3\_DOWNMIX property specifies whether the program channels in an AC-3-encoded stream need to be downmixed to accommodate the speaker configuration.

## <span id="ddk_ksproperty_ac3_downmix_ks"></span><span id="DDK_KSPROPERTY_AC3_DOWNMIX_KS"></span>


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
<th align="left">Get</th>
<th align="left">Set</th>
<th align="left">Target</th>
<th align="left">Property descriptor type</th>
<th align="left">Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Yes</p></td>
<td align="left"><p>Yes</p></td>
<td align="left"><p>Pin</p></td>
<td align="left"><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td align="left"><p>[<strong>KSAC3_DOWNMIX</strong>](https://msdn.microsoft.com/library/windows/hardware/ff537079)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSAC3\_DOWNMIX structure that specifies whether the program channels should be downmixed.

### <span id="Return_Value"></span><span id="return_value"></span><span id="RETURN_VALUE"></span>Return Value

A KSPROPERTY\_AC3\_DOWNMIX property request returns STATUS\_SUCCESS to indicate that it has completed successfully. Otherwise, the request returns an appropriate error status code.

Remarks
-------

Downmixing is required if the number of channels being output by the decoder is less than the number of channels encoded in the AC-3 stream.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Header</p></td>
<td align="left">Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

[**KSAC3\_DOWNMIX**](https://msdn.microsoft.com/library/windows/hardware/ff537079)

 

 






