---
title: DestinationResponse element
description: The required DestinationResponse element contains the response information for a single ScanDestination registration.
ms.assetid: 388304ca-4d62-40cf-ad68-13607a836caf
keywords: ["DestinationResponse element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn DestinationResponse
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# DestinationResponse element


The required **DestinationResponse** element contains the response information for a single [**ScanDestination**](scandestination.md) registration.

Usage
-----

``` syntax
<wscn:DestinationResponse>
  child elements
</wscn:DestinationResponse>
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
<td><p>&lt;Any vendor-defined elements&gt;</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ClientContext</strong>](clientcontext.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>DestinationToken</strong>](destinationtoken.md)</p></td>
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
<td><p>[<strong>DestinationResponses</strong>](destinationresponses.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The **DestinationResponse** element contains the [**ClientContext**](clientcontext.md) element from its matching [**ScanDestination**](scandestination.md) element so that the client can identify the response. **DestinationResponse** also contains a [**DestinationToken**](destinationtoken.md) element for use in all [**CreateScanJobRequest**](createscanjobrequest.md) operation elements from this destination.

## <span id="see_also"></span>See also


[**ClientContext**](clientcontext.md)

[**CreateScanJobRequest**](createscanjobrequest.md)

[**DestinationResponses**](destinationresponses.md)

[**DestinationToken**](destinationtoken.md)

[**ScanDestination**](scandestination.md)

 

 






