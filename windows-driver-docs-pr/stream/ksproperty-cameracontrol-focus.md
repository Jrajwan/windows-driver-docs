---
title: KSPROPERTY\_CAMERACONTROL\_FOCUS
description: User-mode clients use the KSPROPERTY\_CAMERACONTROL\_FOCUS property to get or set a camera's focus setting. This property is optional.
ms.assetid: 89a77055-1ad1-4394-8435-d057685b9eee
keywords: ["KSPROPERTY_CAMERACONTROL_FOCUS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CAMERACONTROL_FOCUS
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

# KSPROPERTY\_CAMERACONTROL\_FOCUS


User-mode clients use the KSPROPERTY\_CAMERACONTROL\_FOCUS property to get or set a camera's focus setting. This property is optional.

## <span id="ddk_ksproperty_cameracontrol_focus_ks"></span><span id="DDK_KSPROPERTY_CAMERACONTROL_FOCUS_KS"></span>


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
<td><p>Filter or node</p></td>
<td><p>[<strong>KSPROPERTY_CAMERACONTROL_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564439) or [<strong>KSPROPERTY_CAMERACONTROL_NODE_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564420)</p></td>
<td><p>LONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a LONG that specifies the focus setting. This value is expressed in millimeters.

**Caution**  When writing or testing an app, you should be aware that in practice, some drivers define a custom range of focus values and custom step values that might not be based on typical units. Drivers might implement the focus control either physically or digitally.

 

Remarks
-------

The **Value** member of the KSPROPERTY\_CAMERACONTROL\_S structure specifies the focus setting.

Every video capture minidriver that supports this property must define its own range and default value for this property.

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

[**KSPROPERTY\_CAMERACONTROL\_S**](https://msdn.microsoft.com/library/windows/hardware/ff564439)

 

 






