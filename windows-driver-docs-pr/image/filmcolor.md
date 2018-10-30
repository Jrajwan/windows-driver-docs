---
title: FilmColor element
description: The required FilmColor element contains the list of color processing capabilities that the film scanning input source supports.
ms.assetid: daea2cb8-a29f-4be8-bc58-8ed45d64870c
keywords: ["FilmColor element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn FilmColor
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# FilmColor element


The required **FilmColor** element contains the list of color processing capabilities that the film scanning input source supports.

Usage
-----

``` syntax
<wscn:FilmColor>
  child elements
</wscn:FilmColor>
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
<td><p>[<strong>ColorEntry</strong>](colorentry.md)</p></td>
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
<td><p>[<strong>Film</strong>](film.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The **FilmColor** element contains the information that is needed to determine the type of color processing and acquisition that the scanner's film scanning input source supports.

The amount of information that is needed to describe each pixel depends on the specific [**ColorEntry**](colorentry.md) keyword. Black and white images require only one bit per pixel (bpp), whereas grayscale and color images require significantly more information. The exact amount of information is determined by the color space and technical capabilities of the scan device.

Another important aspect of the returned scan data is the photometric interpretation of the acquired data. All image data that the scan device returns is required to be black on white, where black is represented by 0 and white is represented by 1.

## <span id="see_also"></span>See also


[**ColorEntry**](colorentry.md)

[**Film**](film.md)

 

 






