---
title: KSPROPERTY\_EXTXPORT\_MEDIUM\_INFO
description: The KSPROPERTY\_EXTXPORT\_MEDIUM\_INFO property retrieves information about an external device's medium.
ms.assetid: 04b98c50-ebb0-4224-b476-d261b7c5dd79
keywords: ["KSPROPERTY_EXTXPORT_MEDIUM_INFO Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_EXTXPORT_MEDIUM_INFO
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

# KSPROPERTY\_EXTXPORT\_MEDIUM\_INFO


The KSPROPERTY\_EXTXPORT\_MEDIUM\_INFO property retrieves information about an external device's medium.

## <span id="ddk_ksproperty_extxport_medium_info_ks"></span><span id="DDK_KSPROPERTY_EXTXPORT_MEDIUM_INFO_KS"></span>


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
<td><p>Device</p></td>
<td><p>[<strong>KSPROPERTY_EXTXPORT_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565167)</p></td>
<td><p>[<strong>MEDIUM_INFO</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567726)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a MEDIUM\_INFO structure that describes the media loaded into the external device. For example cassette tape, tape grade and write protection.

Remarks
-------

The **MediumInfo** member of the KSPROPERTY\_EXTXPORT\_S structure specifies the information.

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

[**KSPROPERTY\_EXTXPORT\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565167)

[**MEDIUM\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff567726)

 

 






