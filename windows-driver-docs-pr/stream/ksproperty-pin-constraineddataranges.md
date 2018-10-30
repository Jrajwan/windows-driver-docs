---
title: KSPROPERTY\_PIN\_CONSTRAINEDDATARANGES
description: The KSPROPERTY\_PIN\_CONSTRAINEDDATARANGES property specifies the list of data ranges currently supported by pins instantiated on the pin factory.
ms.assetid: 6328a128-c6f8-4de1-a86a-0a7c8a940e18
keywords: ["KSPROPERTY_PIN_CONSTRAINEDDATARANGES Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_PIN_CONSTRAINEDDATARANGES
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

# KSPROPERTY\_PIN\_CONSTRAINEDDATARANGES


The KSPROPERTY\_PIN\_CONSTRAINEDDATARANGES property specifies the list of data ranges currently supported by pins instantiated on the pin factory.

## <span id="ddk_ksproperty_pin_constraineddataranges_ks"></span><span id="DDK_KSPROPERTY_PIN_CONSTRAINEDDATARANGES_KS"></span>


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
<td><p>[<strong>KSMULTIPLE_ITEM</strong>](https://msdn.microsoft.com/library/windows/hardware/ff563441) and [<strong>KSDATARANGE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff561658)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The **PinId** member of the [**KSP\_PIN**](https://msdn.microsoft.com/library/windows/hardware/ff566722) structure specifies the pin factory for which to query.

This property returns a [**KSMULTIPLE\_ITEM**](https://msdn.microsoft.com/library/windows/hardware/ff563441) structure, followed by a sequence of 64-bit aligned [**KSDATARANGE**](https://msdn.microsoft.com/library/windows/hardware/ff561658) structures.

A KS filter uses this property to report the data ranges currently supported by pins instantiated on this pin factory, based on any constraints imposed by the current internal state of the KS filter. Use the [**KSPROPERTY\_PIN\_DATARANGES**](ksproperty-pin-dataranges.md) property to report the complete list of all data ranges supported by the KS filter, regardless of dynamic constraints.

Stream minidrivers do not need to handle this property directly; the stream class driver handles this property using stream request blocks to query for more information.

For more information, see [KS Data Formats and Data Ranges](https://msdn.microsoft.com/library/windows/hardware/ff567632).

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


[**KSMULTIPLE\_ITEM**](https://msdn.microsoft.com/library/windows/hardware/ff563441)

[**KSDATARANGE**](https://msdn.microsoft.com/library/windows/hardware/ff561658)

[**KSPROPERTY\_PIN\_DATARANGES**](ksproperty-pin-dataranges.md)

 

 






