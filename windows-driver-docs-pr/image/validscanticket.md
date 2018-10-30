---
title: ValidScanTicket element
description: The optional ValidScanTicket element contains a valid ScanTicket.
ms.assetid: 306b5d90-068f-4b63-9155-8f35c7825f16
keywords: ["ValidScanTicket element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ValidScanTicket
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ValidScanTicket element


The optional **ValidScanTicket** element contains a valid [**ScanTicket**](scanticket.md).

Usage
-----

``` syntax
<wscn:ValidScanTicket>
  child elements
</wscn:ValidScanTicket>
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
<td><p>[<strong>DocumentParameters</strong>](documentparameters.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>JobDescription</strong>](jobdescription.md)</p></td>
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
<td><p>[<strong>ValidationInfo</strong>](validationinfo.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

A client submits a [**ScanTicket**](scanticket.md) for validation through the [**ValidateScanTicketRequest**](validatescanticketrequest.md) operation. If the submitted **ScanTicket** contains invalid settings, the WSD Scan Service must return a **ValidScanTicket** element in which it has changed any invalid settings to be valid settings. The Scan Service returns validation information, which includes **ValidScanTicket**, in [**ValidateScanTicketResponse**](validatescanticketresponse.md).

## <span id="see_also"></span>See also


[**DocumentParameters**](documentparameters.md)

[**JobDescription**](jobdescription.md)

[**ScanTicket**](scanticket.md)

[**ValidateScanTicketRequest**](validatescanticketrequest.md)

[**ValidateScanTicketResponse**](validatescanticketresponse.md)

[**ValidationInfo**](validationinfo.md)

 

 






