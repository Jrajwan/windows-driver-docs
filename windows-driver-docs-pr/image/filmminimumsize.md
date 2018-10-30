---
title: FilmMinimumSize element
description: The required FilmMinimumSize element specifies the smallest size original that an end user can scan with the film scanning option.
ms.assetid: bce03ce1-9f2f-489f-ae71-a81474895410
keywords: ["FilmMinimumSize element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn FilmMinimumSize
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# FilmMinimumSize element


The required **FilmMinimumSize** element specifies the smallest size original that an end user can scan with the film scanning option.

Usage
-----

``` syntax
<wscn:FilmMinimumSize>
  child elements
</wscn:FilmMinimumSize>
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
<td><p>[<strong>Height</strong>](height.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>Width</strong>](width.md)</p></td>
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

The [**Width**](width.md) child element specifies the minimum size of media that the film scanning input source supports in the fast scan direction. The [**Height**](height.md) child element specifies the minimum size of media that the film scanning input source supports in the slow scan direction.

All media dimensions are measured in one-thousandths (1/1000) of an inch. The possible values for both **Width** and **Height** range from 1 through 2147483648.

## <span id="see_also"></span>See also


[**Film**](film.md)

[**Height**](height.md)

[**Width**](width.md)

 

 






