---
title: Width element
description: The required Width element specifies a width value that the scan device supports for scanner configuration elements that require a Width.
ms.assetid: 2e9b6c4a-8180-4c09-8d60-64f8ede7bdfc
keywords: ["Width element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn Width wscn Override "" wscn UsedDefault ""
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Width element


The required **Width** element specifies a width value that the scan device supports for scanner configuration elements that require a **Width**.

Usage
-----

``` syntax
<wscn:Width wscn:Override="" wscn:UsedDefault=""
  Override = "xs:string"
  UsedDefault = "xs:string">
  text
</wscn:Width wscn:Override="" wscn:UsedDefault="">
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
<td><p><strong><strong>Override</strong></strong></p></td>
<td><p>xs:string</p></td>
<td><p>No</p></td>
<td><p></p>
<p>Optional. A Boolean value that must be 0, false, 1, or true.<strong>falsetrue</strong></p></td>
</tr>
<tr class="even">
<td><p><strong><strong>UsedDefault</strong></strong></p></td>
<td><p>xs:string</p></td>
<td><p>No</p></td>
<td><p></p>
<p>Optional. A Boolean value that must be 0, false, 1, or true.<strong>falsetrue</strong></p></td>
</tr>
</tbody>
</table>

Text value
----------

Required. For possible values, see the specific parent element.

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
<td><p>[<strong>ADFOpticalResolution</strong>](adfopticalresolution.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>InputMediaSize</strong>](inputmediasize.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>PlatenMaximumSize</strong>](platenmaximumsize.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>PlatenMinimumSize</strong>](platenminimumsize.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>PlatenOpticalResolution</strong>](platenopticalresolution.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>Widths</strong>](widths.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The **Width** element is a required child element for all of its parent elements. The value of **Width** depends on its parent element. For possible values, see the appropriate parent element.

The WSD Scan Service can specify the optional **Override** and **UsedDefault** attributes only when the **Width** element is contained within a **DocumentFinalParameters** hierarchy. For more information about **Override** and **UsedDefault** and about their usage, see [**DocumentFinalParameters**](documentfinalparameters.md).

## <span id="see_also"></span>See also


[**ADFOpticalResolution**](adfopticalresolution.md)

[**DocumentFinalParameters**](documentfinalparameters.md)

[**Height**](height.md)

[**InputMediaSize**](inputmediasize.md)

[**PlatenMaximumSize**](platenmaximumsize.md)

[**PlatenMinimumSize**](platenminimumsize.md)

[**PlatenOpticalResolution**](platenopticalresolution.md)

[**Widths**](widths.md)

 

 






