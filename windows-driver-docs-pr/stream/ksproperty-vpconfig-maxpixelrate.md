---
title: KSPROPERTY\_VPCONFIG\_MAXPIXELRATE
description: The KSPROPERTY\_VPCONFIG\_MAXPIXELRATE property specifies the maximum pixel rate based on pixel format and specifies the dimension (width by height) of the connection.
ms.assetid: 5a1e70b6-32ab-4a6c-82f7-3e6e828262a4
keywords: ["KSPROPERTY_VPCONFIG_MAXPIXELRATE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VPCONFIG_MAXPIXELRATE
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

# KSPROPERTY\_VPCONFIG\_MAXPIXELRATE


The KSPROPERTY\_VPCONFIG\_MAXPIXELRATE property specifies the maximum pixel rate based on pixel format and specifies the dimension (width by height) of the connection.

## <span id="ddk_ksproperty_vpconfig_maxpixelrate_ks"></span><span id="DDK_KSPROPERTY_VPCONFIG_MAXPIXELRATE_KS"></span>


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
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KSVPMAXPIXELRATE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567234)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a KSVPMAXPIXELRATE structure that describes the width, height, and maximum number of pixels per second that the video port supports.

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

[**KSVPMAXPIXELRATE**](https://msdn.microsoft.com/library/windows/hardware/ff567234)

 

 






