---
title: KSPROPERTY\_PIN\_PHYSICALCONNECTION
description: Audio adapter drivers use the KSPROPERTY\_PIN\_PHYSICALCONNECTION property to denote physical connections between miniports.
ms.assetid: a679ce41-93d2-4b46-a26d-ce05408ec6aa
keywords: ["KSPROPERTY_PIN_PHYSICALCONNECTION Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_PIN_PHYSICALCONNECTION
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

# KSPROPERTY\_PIN\_PHYSICALCONNECTION


Audio adapter drivers use the KSPROPERTY\_PIN\_PHYSICALCONNECTION property to denote physical connections between miniports.

## <span id="ddk_ksproperty_pin_physicalconnection_ks"></span><span id="DDK_KSPROPERTY_PIN_PHYSICALCONNECTION_KS"></span>


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
<td><p>[<strong>KSP_PIN</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566722)</p></td>
<td><p>[<strong>KSPIN_PHYSICALCONNECTION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff563539)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

Specify this property using KSP\_PIN, where the member specifies the relevant pin factory.

KSPROPERTY\_PIN\_PHYSICALCONNECTION returns a structure of type [**KSPIN\_PHYSICALCONNECTION**](https://msdn.microsoft.com/library/windows/hardware/ff563539), specifying the connected **PinId** and the symbolic link name of the connected filter.

The class driver does not handle this property; the stream minidriver must provide handling on its own.

Audio adapter drivers register connections with [**PcRegisterPhysicalConnection**](https://msdn.microsoft.com/library/windows/hardware/ff537726).

Subsequently, the SysAudio system driver (*sysaudio.sys*) queries this property and builds the graph accordingly. SysAudio uses this property to determine which wave filter pin is connected to which topology filter pin.

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


[**KSP\_PIN**](https://msdn.microsoft.com/library/windows/hardware/ff566722)

[**KSPIN\_PHYSICALCONNECTION**](https://msdn.microsoft.com/library/windows/hardware/ff563539)

[**PcRegisterPhysicalConnection**](https://msdn.microsoft.com/library/windows/hardware/ff537726)

 

 






