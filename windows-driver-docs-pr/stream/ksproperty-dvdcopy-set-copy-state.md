---
title: KSPROPERTY\_DVDCOPY\_SET\_COPY\_STATE
description: The KSPROPERTY\_DVDCOPY\_SET\_COPY\_STATE property sets the copy state of the DVD decoder stream. This property is optional to implement.
ms.assetid: f4e46d79-c70b-413a-9702-a73d3776ee2c
keywords: ["KSPROPERTY_DVDCOPY_SET_COPY_STATE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_DVDCOPY_SET_COPY_STATE
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

# KSPROPERTY\_DVDCOPY\_SET\_COPY\_STATE


The KSPROPERTY\_DVDCOPY\_SET\_COPY\_STATE property sets the copy state of the DVD decoder stream. This property is optional to implement.

## <span id="ddk_ksproperty_dvdcopy_set_copy_state_ks"></span><span id="DDK_KSPROPERTY_DVDCOPY_SET_COPY_STATE_KS"></span>


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
<td><p>[<strong>KS_DVDCOPY_SET_COPY_STATE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567639)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KS\_DVDCOPY\_SET\_COPY\_STATE structure that describes the copyright protection state of the DVD decoder stream.

Remarks
-------

This property indicates whether this pin requires CSS authentication. If the property is not implemented, the default is assumed to be the **KS\_DVDCOPYSTATE\_AUTHENTICATION\_REQUIRED** value from the [**KS\_DVDCOPYSTATE**](https://msdn.microsoft.com/library/windows/hardware/ff567634) enumeration.

The main use for this property is for a decoder that supports multiple pins with the same decrypter. For example, if one filter provides both subpicture and video decoding, the keys only need to be exchanged for one of the two pins. If a filter is going to return **KS\_DVDCOPYSTATE\_AUTHENTICATION\_NOT\_REQUIRED** on one of the pins, then it must always return **KS\_DVDCOPYSTATE\_AUTHENTICATION\_REQUIRED** on the first pin that the property is issued on.

When this property is issued as a **Get** call, the filter can respond with either **KS\_DVDCOPYSTATE\_AUTHENTICATION\_REQUIRED** or KS\_DVDCOPYSTATE\_AUTHENTICATION\_NOT\_REQUIRED.

When this property is issued as a **Set** call, this is an informational call used by hardware decoders to indicate what phase of the copyright protection negotiation is being entered. The decoder can hold off the SET\_STATE with one of the following until the correct bits, indicating that a new CSS key is required, have been received:

<span id="KS_DVDCOPYSTATE_INITIALIZE"></span><span id="ks_dvdcopystate_initialize"></span>**KS\_DVDCOPYSTATE\_INITIALIZE**  
Indicates the start of a disc key negotiation sequence.

<span id="KS_DVDCOPYSTATE_INITIALIZE_TITLE"></span><span id="ks_dvdcopystate_initialize_title"></span>**KS\_DVDCOPYSTATE\_INITIALIZE\_TITLE**  
Indicates the start of a title key negotiation sequence.

<span id="KS_DVDCOPYSTATE_DONE"></span><span id="ks_dvdcopystate_done"></span>**KS\_DVDCOPYSTATE\_DONE**  
Indicates the completion of a key negotiation sequence.

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


[**KS\_DVDCOPY\_SET\_COPY\_STATE**](https://msdn.microsoft.com/library/windows/hardware/ff567639)

[**KS\_DVDCOPYSTATE**](https://msdn.microsoft.com/library/windows/hardware/ff567634)

[DVD Copyright Protection](https://msdn.microsoft.com/library/windows/hardware/ff558736)

[Multiple Data Streams on the same Hardware](https://msdn.microsoft.com/library/windows/hardware/ff567744)

[Synchronizing Key Exchange with Data Flow](https://msdn.microsoft.com/library/windows/hardware/ff568511)

 

 






