---
title: ContentTypesSupported element
description: The required ContentTypesSupported element contains a list of keywords that describe the different document content types that the scanner supports.
ms.assetid: f7ed2ba9-8cd9-486c-9bb0-3eb2c925450a
keywords: ["ContentTypesSupported element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ContentTypesSupported
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ContentTypesSupported element


The required **ContentTypesSupported** element contains a list of keywords that describe the different document content types that the scanner supports.

Usage
-----

``` syntax
<wscn:ContentTypesSupported>
  child elements
</wscn:ContentTypesSupported>
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
<td><p>[<strong>ContentTypeValue</strong>](contenttypevalue.md)</p></td>
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

Each [**ContentTypeValue**](contenttypevalue.md) element that is listed in a **ContentTypesSupported** element describes the main characteristics of the original document. The client will pick one content type for its [**ScanTicket**](scanticket.md) from this list when initiating a scan.

## <span id="see_also"></span>See also


[**ScanTicket**](scanticket.md)

 

 






