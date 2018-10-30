---
title: Video Decoder Properties
author: windows-driver-content
description: Video Decoder Properties
ms.assetid: 671a310b-52a6-49f0-8848-e586a37c25ff
keywords:
- video decoder properties WDK video capture
- decoder properties WDK video capture
- PROPSETID_VIDCAP_VIDEODECODER
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Video Decoder Properties


The [PROPSETID\_VIDCAP\_VIDEODECODER](https://msdn.microsoft.com/library/windows/hardware/ff568121) property set contains properties related to the operation of analog video decoder devices, such as the transmission standard and timing signals. The following table describes the properties that are part of the PROPSETID\_VIDCAP\_VIDEODECODER property set.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>PROPSETID_VIDCAP_VIDEODECODER KS properties</th>
<th>Property description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>KSPROPERTY_VIDEODECODER_CAPS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566046)</p></td>
<td><p>Returns information on the capabilities of the video decoder device, such as signal standard (NTSC, PAL, SECAM) and settling time.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>KSPROPERTY_VIDEODECODER_STANDARD</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566058)</p></td>
<td><p>Controls the current analog video standard.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>KSPROPERTY_VIDEODECODER_STATUS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566060)</p></td>
<td><p>Returns the status of the video decoding device, such as number of lines in the video signal and whether the signal is locked.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>KSPROPERTY_VIDEODECODER_OUTPUT_ENABLE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566051)</p></td>
<td><p>Controls three-state output of the video decoder.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>KSPROPERTY_VIDEODECODER_VCR_TIMING</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566062)</p></td>
<td><p>Controls whether the video decoder uses VCR timing or broadcast timing.</p></td>
</tr>
</tbody>
</table>

 

 

 




