---
title: KSPROPERTY\_CAMERACONTROL\_TILT
description: User-mode clients use the KSPROPERTY\_CAMERACONTROL\_TILT property to get or set a camera's tilt setting. This property is optional.
ms.assetid: 265315ce-6f35-4f5a-907f-b5595e7fb5af
keywords: ["KSPROPERTY_CAMERACONTROL_TILT Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CAMERACONTROL_TILT
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

# KSPROPERTY\_CAMERACONTROL\_TILT


User-mode clients use the KSPROPERTY\_CAMERACONTROL\_TILT property to get or set a camera's tilt setting. This property is optional.

## <span id="ddk_ksproperty_cameracontrol_tilt_ks"></span><span id="DDK_KSPROPERTY_CAMERACONTROL_TILT_KS"></span>


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

 

The property value (operation data) is a LONG that specifies a camera's tilt setting. This value is expressed in degrees.

Positive values point the imaging plane up. Negative values point the imaging plane down, as shown in the following illustration.

![illustration showing camera tilt values](images/cam-tilt-1.png)

Every video capture minidriver that supports this property must define a range and default value for this property. The range for the device must -180 through +180. The default value must be 0.

**Caution**  When writing or testing an app, you should be aware that in practice, some drivers define a custom range of tilt values and custom step values that might not be based on typical units. Drivers might implement the tilt control either physically or digitally.

 

Remarks
-------

The **Value** member of the KSPROPERTY\_CAMERACONTROL\_S structure specifies the tilt setting.

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

 

 






