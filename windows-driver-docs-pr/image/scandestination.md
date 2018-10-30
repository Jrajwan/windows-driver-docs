---
title: ScanDestination element
description: The required ScanDestination element specifies a single scan destination on the client.
ms.assetid: 3cd685b2-36b2-4f28-a80f-a68204631e0c
keywords: ["ScanDestination element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ScanDestination
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ScanDestination element


The required **ScanDestination** element specifies a single scan destination on the client.

Usage
-----

``` syntax
<wscn:ScanDestination>
  child elements
</wscn:ScanDestination>
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
<td><p>[<strong>ClientContext</strong>](clientcontext.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ClientDisplayName</strong>](clientdisplayname.md)</p></td>
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
<td><p>[<strong>ScanDestinations</strong>](scandestinations.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The client includes one or more **ScanDestination** elements within the **ScanDestinations** element that it sends when it creates a subscription. The WSD Scan Service uses the information that is provided within **ScanDestination** to create appropriate [**ScanAvailableEvent**](scanavailableevent.md) event elements.

## <span id="see_also"></span>See also


[**ClientContext**](clientcontext.md)

[**ClientDisplayName**](clientdisplayname.md)

[**ScanAvailableEvent**](scanavailableevent.md)

[**ScanDestinations**](scandestinations.md)

 

 






