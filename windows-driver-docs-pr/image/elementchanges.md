---
title: ElementChanges element
description: The required ElementChanges element contains the changes to the ScannerDescription, ScannerConfiguration, DefaultScanTicket, and vendor-extended elements.
ms.assetid: d6f1d188-beb6-4ea3-a362-de64d8d8dacb
keywords: ["ElementChanges element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn ElementChanges
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ElementChanges element


The required **ElementChanges** element contains the changes to the [**ScannerDescription**](scannerdescription.md), [**ScannerConfiguration**](scannerconfiguration.md), [**DefaultScanTicket**](defaultscanticket.md), and vendor-extended elements.

Usage
-----

``` syntax
<wscn:ElementChanges>
  child elements
</wscn:ElementChanges>
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
<td><p>[<strong>DefaultScanTicket</strong>](defaultscanticket.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ScannerConfiguration</strong>](scannerconfiguration.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>ScannerDescription</strong>](scannerdescription.md)</p></td>
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
<td><p>[<strong>ScannerElementsChangeEvent</strong>](scannerelementschangeevent.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The WSD Scan Service must include an **ElementChanges** element when it generates a [**ScannerElementsChangeEvent**](scannerelementschangeevent.md) element. Each child element of **ElementChanges** must contain all of its required child elements. If an optional element is missing from the returned XML, the WSD Scan Service is indicating to the client that the service no longer supports that element.

## <span id="see_also"></span>See also


[**DefaultScanTicket**](defaultscanticket.md)

[**ScannerConfiguration**](scannerconfiguration.md)

[**ScannerDescription**](scannerdescription.md)

[**ScannerElementsChangeEvent**](scannerelementschangeevent.md)

 

 






