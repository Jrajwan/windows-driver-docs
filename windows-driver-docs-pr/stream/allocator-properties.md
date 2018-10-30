---
title: Allocator Properties
author: windows-driver-content
description: Allocator Properties
ms.assetid: 851bc3d8-46f6-46d0-87a8-81de2536492a
keywords:
- allocator properties WDK video capture
- PROPSETID_ALLOCATOR_CONTROL
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Allocator Properties


The [PROPSETID\_ALLOCATOR\_CONTROL](https://msdn.microsoft.com/library/windows/hardware/ff567792) property set contains properties related to controlling the allocation and operations of video port surfaces. User-mode filters, such as the Overlay Mixer, use PROPSETID\_ALLOCATOR\_CONTROL. The following table describes properties that are part of the PROPSETID\_ALLOCATOR\_CONTROL property set.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>PROPSETID_ALLOCATOR_CONTROL KS properties</th>
<th>Property description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>KSPROPERTY_ALLOCATOR_CONTROL_HONOR_COUNT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564276)</p></td>
<td><p>Controls how a filter determines the number of video port overlay surfaces to allocate.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>KSPROPERTY_ALLOCATOR_CONTROL_SURFACE_SIZE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564278)</p></td>
<td><p>Controls the dimensions of the video port overlay surface.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>KSPROPERTY_ALLOCATOR_CONTROL_CAPTURE_CAPS</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564267)</p></td>
<td><p>Describes the capture capabilities of the video port.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>KSPROPERTY_ALLOCATOR_CONTROL_CAPTURE_INTERLEAVE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564271)</p></td>
<td><p>Returns if the video port supports interleaved capture.</p></td>
</tr>
</tbody>
</table>

 

 

 




