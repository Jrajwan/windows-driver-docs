---
title: KSPROPERTY\_VPCONFIG\_INVERTPOLARITY
description: The KSPROPERTY\_VPCONFIG\_INVERTPOLARITY property toggles the global polarity flag, forcing the video port to be inverted.
ms.assetid: c0b69aa4-0f81-42b4-9a69-5afcf702f5f1
keywords: ["KSPROPERTY_VPCONFIG_INVERTPOLARITY Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VPCONFIG_INVERTPOLARITY
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

# KSPROPERTY\_VPCONFIG\_INVERTPOLARITY


The KSPROPERTY\_VPCONFIG\_INVERTPOLARITY property toggles the global polarity flag, forcing the video port to be inverted.

## <span id="ddk_ksproperty_vpconfig_invertpolarity_ks"></span><span id="DDK_KSPROPERTY_VPCONFIG_INVERTPOLARITY_KS"></span>


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
<td><p>Boolean</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a Boolean. Specify **TRUE** to invert the polarity, or specify **FALSE** to prevent inverting the polarity.

Remarks
-------

KSPROPERTY\_VPCONFIG\_INVERTPOLARITY property requests return STATUS\_SUCCESS to indicate successful completion. Otherwise, requests return an appropriate error status code.

Because this feature is hardware dependent, models that do not use this feature must return STATUS\_NOT\_IMPLEMENTED.

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

 

 






