---
title: ScalingRangeSupported element
description: The required ScalingRangeSupported element describes the range of values that the scan device supports for scaling the output document.
ms.assetid: 0af5a00e-fdca-438f-b463-3150abf0f871
keywords: ["ScalingRangeSupported element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ScalingRangeSupported
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ScalingRangeSupported element


The required **ScalingRangeSupported** element describes the range of values that the scan device supports for scaling the output document.

Usage
-----

``` syntax
<wscn:ScalingRangeSupported>
  child elements
</wscn:ScalingRangeSupported>
```

Attributes
----------

There are no attributes.

## Child elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>ScalingHeight</strong>](scalingheight2.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ScalingWidth</strong>](scalingwidth2.md)</p></td>
</tr>
</tbody>
</table>

## Parent elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>DeviceSettings</strong>](devicesettings.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The [**ScalingWidth**](scalingwidth2.md) and [**ScalingHeight**](scalingheight2.md) elements specify the scaling range for the width and height of an image, respectively.

## <span id="see_also"></span>See also


[**DeviceSettings**](devicesettings.md)

[**ScalingHeight**](scalingheight2.md)

[**ScalingWidth**](scalingwidth2.md)

 

 






