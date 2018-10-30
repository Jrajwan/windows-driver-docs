---
title: MediaSides element
description: The optional MediaSides element contains the parameters that are unique to each physical side of the scanned media.
ms.assetid: 9bd3de21-4b2c-4cea-add6-51240ad6c19f
keywords: ["MediaSides element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn MediaSides wscn MustHonor ""
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# MediaSides element


The optional **MediaSides** element contains the parameters that are unique to each physical side of the scanned media.

Usage
-----

``` syntax
<wscn:MediaSides wscn:MustHonor=""
  MustHonor = "xs:string">
  child elements
</wscn:MediaSides wscn:MustHonor="">
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
<td><p><strong><strong>MustHonor</strong></strong></p></td>
<td><p>xs:string</p></td>
<td><p>No</p></td>
<td><p></p>
<p>Optional. A Boolean value that must be 0, false, 1, or true.<strong>falsetrue</strong></p></td>
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
<td><p>[<strong>MediaBack</strong>](mediaback.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>MediaFront</strong>](mediafront.md)</p></td>
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
<td><p>[<strong>DocumentFinalParameters</strong>](documentfinalparameters.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>DocumentParameters</strong>](documentparameters.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

Many duplex-capable scanners allow for setting different scan regions, color processing, and resolutions for each physical side of the scanned media. The **MediaSides** element contains separate data for the front and back sides of the media. Every scan job can have parameters for the media front.

The [**MediaBack**](mediaback.md) element is valid only when the scanner supports duplex scanning, and the current [**InputSource**](inputsource.md) is **ADFDuplex**.

If **InputSource** is **ADFDuplex** and the **MediaBack** element is missing, all parameters that are specified in **MediaFront** will apply to the back side scanning as well.

The client can specify the optional **MustHonor** attribute only when the **MediaSides** element is contained within a **CreateScanJobRequest** hierarchy. For more information about **MustHonor** and its usage, see [**CreateScanJobRequest**](createscanjobrequest.md).

The WSD Scan Service can specify the optional **Override** and **UsedDefault** attributes only when the **MediaSides** element is contained within a **DocumentFinalParameters** hierarchy. For more information about **Override** and **UsedDefault** and their usage, see [**DocumentFinalParameters**](documentfinalparameters.md).

## <span id="see_also"></span>See also


[**CreateScanJobRequest**](createscanjobrequest.md)

[**DocumentFinalParameters**](documentfinalparameters.md)

[**DocumentParameters**](documentparameters.md)

[**InputSource**](inputsource.md)

[**MediaBack**](mediaback.md)

[**MediaFront**](mediafront.md)

 

 






