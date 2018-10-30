---
title: JobStateReasons element
description: The required JobStateReasons element contains all additional information about why a job is in its current state.
ms.assetid: 52d6519e-2392-4fa4-bac0-f1bf60eccc99
keywords: ["JobStateReasons element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn JobStateReasons
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# JobStateReasons element


The required **JobStateReasons** element contains all additional information about why a job is in its current state.

Usage
-----

``` syntax
<wscn:JobStateReasons>
  child elements
</wscn:JobStateReasons>
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
<td><p>[<strong>JobStateReason</strong>](jobstatereason.md)</p></td>
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
<td><p>[<strong>JobStatus</strong>](jobstatus.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>JobSummary</strong>](jobsummary.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The **JobStateReasons** element contains a list of [**JobStateReason**](jobstatereason.md) elements, each of which specifies one reason why a job is in its current state.

## <span id="see_also"></span>See also


[**JobStateReason**](jobstatereason.md)

[**JobStatus**](jobstatus.md)

[**JobSummary**](jobsummary.md)

 

 






