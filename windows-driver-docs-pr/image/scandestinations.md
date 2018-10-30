---
title: ScanDestinations element
description: The required ScanDestinations element is a collection of all of the scan destinations that a client wants to register with the scan device.
ms.assetid: 50f87269-4d95-4653-ba93-aa752bdc9168
keywords: ["ScanDestinations element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ScanDestinations
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ScanDestinations element


The required **ScanDestinations** element is a collection of all of the scan destinations that a client wants to register with the scan device.

Usage
-----

``` syntax
<wscn:ScanDestinations>
  child elements
</wscn:ScanDestinations>
```

Attributes
----------

There are no attributes.

Text value
----------

None

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
<td><p>[<strong>ScanDestination</strong>](scandestination.md)</p></td>
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
<td><p>&lt;wse:Subscribe&gt;</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The client must send the **ScanDestinations** element in the **&lt;wse:Subscribe&gt;** request operation element to register one or more scan destinations with the WSD Scan Service. The client subscribes during client setup before obtaining scan ticket information from the WSD Scan Service. The **&lt;wse:Subscribe&gt;** element is defined in the specification.

The **ScanDestinations** element give clients the flexibility to register for multiple unique scan destinations at once.

## <span id="see_also"></span>See also


[**ScanDestination**](scandestination.md)

 

 






