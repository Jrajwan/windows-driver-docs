---
title: ElementData for JobElements element
description: The required ElementData element contains the data that is returned for a job-related schema request.
ms.assetid: 6d9724cd-c076-4c87-9c01-ec2c16cd2aac
keywords: ["ElementData for JobElements element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ElementData Name "" Valid ""
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ElementData for JobElements element


The required **ElementData** element contains the data that is returned for a job-related schema request.

Usage
-----

``` syntax
<wscn:ElementData Name="" Valid=""
  Name = "xs:string"
  Valid = "xs:string">
  child elements
</wscn:ElementData Name="" Valid="">
```

Attributes
----------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Type</th>
<th>Required</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><strong>Name</strong></strong></p></td>
<td><p>xs:string</p></td>
<td><p>No</p></td>
<td><p></p>
<p>Required. One of the following QName values:xmlns:JobStatusReturn the current JobStatusschema.xmlns:ScanTicketReturn the ScanTicket element.xmlns:DocumentsReturn the Documents element.xmlns:VendorSectionGet the identified section of a vendor-defined extension to the WSD Scan Service.</p></td>
</tr>
<tr class="even">
<td><p><strong><strong>Valid</strong></strong></p></td>
<td><p>xs:string</p></td>
<td><p>No</p></td>
<td><p></p>
<p>Required. A Boolean value that must be 0, false, 1, or true.</p></td>
</tr>
</tbody>
</table>

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
<td><p>Any vendor-defined elements</p></td>
</tr>
<tr class="even">
<td><p>[<strong>Documents</strong>](documents.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>JobStatus</strong>](jobstatus.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ScanTicket</strong>](scanticket.md)</p></td>
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
<td><p>[<strong>JobElements</strong>](jobelements.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The WSD Scan Service returns the **ElementData** element in a [**GetJobElementsResponse**](getjobelementsresponse.md) operation element.

## <span id="see_also"></span>See also


[**Documents**](documents.md)

[**GetJobElementsResponse**](getjobelementsresponse.md)

[**JobElements**](jobelements.md)

[**JobStatus**](jobstatus.md)

[**ScanTicket**](scanticket.md)

 

 






