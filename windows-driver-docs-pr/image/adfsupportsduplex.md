---
title: ADFSupportsDuplex element
description: The required ADFSupportsDuplex element specifies whether the attached automatic document feeder (ADF) supports scanning both sides of the media.
ms.assetid: 0e85243a-5b15-4b51-9608-c8036639c735
keywords: ["ADFSupportsDuplex element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ADFSupportsDuplex
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ADFSupportsDuplex element


The required **ADFSupportsDuplex** element specifies whether the attached automatic document feeder (ADF) supports scanning both sides of the media.

Usage
-----

``` syntax
<wscn:ADFSupportsDuplex>
  text
</wscn:ADFSupportsDuplex>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. A Boolean value that must be 0, 1, false, or true.**false** or **true**

## Child elements


There are no child elements.

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
<td><p>[<strong>ADF</strong>](adf.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

If the scan device has an ADF that supports duplex scanning, the WSD Scan Service should return 1 (**true**); otherwise, it should return 0 (**false**).

You cannot extend the allowed values for this element.

## <span id="see_also"></span>See also


[**ADF**](adf.md)

 

 






