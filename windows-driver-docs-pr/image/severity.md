---
title: Severity element
description: The required Severity element specifies the severity level of the current DeviceCondition or ConditionHistoryEntry element.
ms.assetid: 51c08a50-0c2b-40d9-883e-32460c2024ad
keywords: ["Severity element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn Severity
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Severity element


The required **Severity** element specifies the severity level of the current [**DeviceCondition**](devicecondition.md) or [**ConditionHistoryEntry**](conditionhistoryentry.md) element.

Usage
-----

``` syntax
<wscn:Severity>
  text
</wscn:Severity>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. One of the following values:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Term</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>Informational</p></td>
<td><p>This condition is purely for user information and has no noticeable effect on the image acquisition process.</p></td>
</tr>
<tr class="even">
<td><p><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>Warning</p></td>
<td><p>This condition is not currently affecting processing, but the condition might become Critical if it is not attended to.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>Critical</p></td>
<td><p>The device cannot continue processing until this condition is resolved.</p></td>
</tr>
</tbody>
</table>

 

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
<td><p>[<strong>ConditionHistoryEntry</strong>](conditionhistoryentry.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>DeviceCondition</strong>](devicecondition.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The WSD Scan Service determines the **Severity** level that is assigned to each error condition.

You can both extend and subset the allowed values for this element.

## <span id="see_also"></span>See also


[**ConditionHistoryEntry**](conditionhistoryentry.md)

[**DeviceCondition**](devicecondition.md)

 

 






