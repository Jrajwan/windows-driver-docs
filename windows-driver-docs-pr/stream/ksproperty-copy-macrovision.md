---
title: KSPROPERTY\_COPY\_MACROVISION
description: The KSPROPERTY\_COPY\_MACROVISION property indicates the Macrovision level of the data stream.
ms.assetid: 6863bcf6-06bc-4bd2-896e-43c083aa07d5
keywords: ["KSPROPERTY_COPY_MACROVISION Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_COPY_MACROVISION
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

# KSPROPERTY\_COPY\_MACROVISION


The KSPROPERTY\_COPY\_MACROVISION property indicates the Macrovision level of the data stream.

## <span id="ddk_ksproperty_copy_macrovision_ks"></span><span id="DDK_KSPROPERTY_COPY_MACROVISION_KS"></span>


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
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KS_COPY_MACROVISION</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567316)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KS\_COPY\_MACROVISION structure the specifies the Macrovision level of the data stream.

Remarks
-------

For more information about Macrovision level, see [DVD Copyright Protection](https://msdn.microsoft.com/library/windows/hardware/ff558736).

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


[**KS\_COPY\_MACROVISION**](https://msdn.microsoft.com/library/windows/hardware/ff567316)

 

 






