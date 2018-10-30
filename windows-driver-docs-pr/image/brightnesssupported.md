---
title: BrightnessSupported element
description: The required BrightnessSupported element specifies whether the scan device supports user control of the scan brightness setting.
ms.assetid: aa0eb627-694f-45a1-a923-07fc04b0612b
keywords: ["BrightnessSupported element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn BrightnessSupported
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# BrightnessSupported element


The required **BrightnessSupported** element specifies whether the scan device supports user control of the scan brightness setting.

Usage
-----

``` syntax
<wscn:BrightnessSupported>
  text
</wscn:BrightnessSupported>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. A Boolean value that must be 0, 1, false, or true.**falsetrue**

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
<td><p>[<strong>DeviceSettings</strong>](devicesettings.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

If the scan device allows user control of the scan brightness setting, the WSD Scan Service should return 1 (**true**); otherwise, it should return 0 (**false**).

You cannot extend the allowed values for this element.

## <span id="see_also"></span>See also


[**DeviceSettings**](devicesettings.md)

 

 






