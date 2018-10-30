---
title: CODECAPI\_VIDEO\_ENCODER
description: CODECAPI\_VIDEO\_ENCODER
ms.assetid: e08f26ff-1e11-42a4-a9f8-3af9b885a901
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# CODECAPI\_VIDEO\_ENCODER


## <span id="ddk_codecapi_video_encoder_ks"></span><span id="DDK_CODECAPI_VIDEO_ENCODER_KS"></span>


Video encoders use the support of this GUID (queried by the user-mode KsProperty BASICSUPPORT) to indicate they are a video encoder.

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
<td><p>Filter</p></td>
<td><p>KSPROPERTY</p></td>
<td><p>BOOL</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is of type BOOL and specifies whether the minidriver supports video encoding. A value of **TRUE** indicates that the minidriver supports video encoding. The filter should not support this GUID if it is not a video encoder.

### <span id="headers"></span><span id="HEADERS"></span>Headers

Declared in *ksmedia.h*. Include *ksmedia.h*.

### <span id="requirements"></span><span id="REQUIREMENTS"></span>Requirements

**Headers:** Declared in *ksmedia.h*. Include *ksmedia.h*.

### <span id="see_also"></span><span id="SEE_ALSO"></span>See Also

[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

 

 





