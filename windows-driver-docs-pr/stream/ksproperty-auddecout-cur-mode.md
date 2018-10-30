---
title: KSPROPERTY\_AUDDECOUT\_CUR\_MODE
description: The KSPROPERTY\_AUDDECOUT\_CUR\_MODE property indicates the current audio output mode.
ms.assetid: 4ac6d181-f532-4ac6-b8fd-2975214a3618
keywords: ["KSPROPERTY_AUDDECOUT_CUR_MODE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_AUDDECOUT_CUR_MODE
api_location:
- ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_AUDDECOUT\_CUR\_MODE


The KSPROPERTY\_AUDDECOUT\_CUR\_MODE property indicates the current audio output mode.

## <span id="ddk_ksproperty_auddecout_cur_mode_ks"></span><span id="DDK_KSPROPERTY_AUDDECOUT_CUR_MODE_KS"></span>


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
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>DWORD</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a DWORD that represents the current output mode of the audio decoder.

Remarks
-------

The property value can be one of the following mode constants defined in the header file *ksmedia.h*:

<span id="KSAUDDECOUTMODE_STEREO_ANALOG"></span><span id="ksauddecoutmode_stereo_analog"></span>**KSAUDDECOUTMODE\_STEREO\_ANALOG**  
Indicates that the output is in analog stereo.

<span id="KSAUDDECOUTMODE_PCM_51"></span><span id="ksauddecoutmode_pcm_51"></span>**KSAUDDECOUTMODE\_PCM\_51**  
Indicates that the output is in PCM 5.1 channel digital.

<span id="KSAUDDECOUTMODE_SPDIFF"></span><span id="ksauddecoutmode_spdiff"></span>**KSAUDDECOUTMODE\_SPDIFF**  
Indicates that the output is SPDIFF format AC3 digital.

The audio miniport driver get-property handler returns the current mode of the decoder, whereas the audio miniport driver set-property handler requests that the decoder switch the output audio format to the requested mode.

We recommend that you specify a default value for the KSPROPERTY\_AUDDECOUT\_CUR\_MODE property in the minidriver's serialized property set in the registry.

For more information, see [Audio Miniport Drivers](https://msdn.microsoft.com/library/windows/hardware/ff536206).

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


[**KSPROPERTY\_AUDDECOUT\_MODES**](ksproperty-auddecout-modes.md)

 

 






