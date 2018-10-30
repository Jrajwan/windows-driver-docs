---
title: ValidTicket element
description: The required ValidTicket element indicates whether a client's ScanTicket was valid.
ms.assetid: 8c2f35b5-1b1e-49a4-8aab-4d57ff9f1803
keywords: ["ValidTicket element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ValidTicket
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ValidTicket element


The required **ValidTicket** element indicates whether a client's [**ScanTicket**](scanticket.md) was valid.

Usage
-----

``` syntax
<wscn:ValidTicket>
  text
</wscn:ValidTicket>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. A Boolean value that must be 0, false, 1, or true.

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
<td><p>[<strong>ValidationInfo</strong>](validationinfo.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

A client submits a [**ScanTicket**](scanticket.md) for validation through the [**ValidateScanTicketRequest**](validatescanticketrequest.md) operation. The WSD Scan Service returns validation information, which includes **ValidTicket**, in [**ValidateScanTicketResponse**](validatescanticketresponse.md).

## <span id="see_also"></span>See also


[**ScanTicket**](scanticket.md)

[**ValidateScanTicketRequest**](validatescanticketrequest.md)

[**ValidateScanTicketResponse**](validatescanticketresponse.md)

[**ValidationInfo**](validationinfo.md)

 

 






