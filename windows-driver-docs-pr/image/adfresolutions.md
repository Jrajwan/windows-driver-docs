---
title: ADFResolutions element
description: The required ADFResolutions element contains a list of resolutions at which the front or back side of the scanner's automatic document feeder (ADF) can scan.
ms.assetid: 6747b4d9-3333-4f06-9c1e-043dde24273c
keywords: ["ADFResolutions element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ADFResolutions
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ADFResolutions element


The required **ADFResolutions** element contains a list of resolutions at which the front or back side of the scanner's automatic document feeder (ADF) can scan.

Usage
-----

``` syntax
<wscn:ADFResolutions>
  child elements
</wscn:ADFResolutions>
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
<td><p>[<strong>Heights</strong>](heights.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>Widths</strong>](widths.md)</p></td>
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
<td><p>[<strong>ADFBack</strong>](adfback.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ADFFront</strong>](adffront.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The resolution is specified as a [**Width**](width.md) x [**Height**](height.md) pair, where both **Width** and **Height** are specified in pixels per inch.

If the parent element of the **ADFResolutions** element is [**ADFFront**](adffront.md), the specified resolution applies to the front side of the ADF; otherwise, the parent element is [**ADFBack**](adfback.md) and the resolution applies to the back side of the ADF.

The WSD Scan Service should list all possible widths that the scan device supports within the **Widths** child element and all possible heights that the scan device supports within the **Heights** child element. All **Width** and **Height** values are independent of each other, and most devices will support them being paired in any combination within a [**ScanTicket**](scanticket.md) element.

## <span id="see_also"></span>See also


[**ADFBack**](adfback.md)

[**ADFFront**](adffront.md)

[**Height**](height.md)

[**Heights**](heights.md)

[**ScanTicket**](scanticket.md)

[**Width**](width.md)

[**Widths**](widths.md)

 

 






