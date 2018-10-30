---
title: KSPROPERTY\_BDA\_SIGNAL\_LOCK\_TYPE
description: Clients use KSPROPERTY\_BDA\_SIGNAL\_LOCK\_TYPE to determine the current lock type of a signal.
ms.assetid: 2ddf49c4-f0d1-4918-b564-719c695a83ac
keywords: ["KSPROPERTY_BDA_SIGNAL_LOCK_TYPE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_BDA_SIGNAL_LOCK_TYPE
api_location:
- Bdamedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_BDA\_SIGNAL\_LOCK\_TYPE


Clients use KSPROPERTY\_BDA\_SIGNAL\_LOCK\_TYPE to determine the current lock type of a signal.

### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property descriptor type</th>
<th>Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Pin or Filter</p></td>
<td><p>KSP_NODE</p></td>
<td><p>[<strong>BDA_LockType</strong>](https://msdn.microsoft.com/library/windows/hardware/ff556526)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The **NodeId** member of KSP\_NODE specifies the identifier of the control node or is set to −1 to specify a pin.

The returned [**BDA\_LockType**](https://msdn.microsoft.com/library/windows/hardware/ff556526)-typed value identifies the current lock type.

The RF tuner node should provide this indication.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Bdamedia.h (include Bdamedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**BDA\_LockType**](https://msdn.microsoft.com/library/windows/hardware/ff556526)

[**KSP\_NODE**](https://msdn.microsoft.com/library/windows/hardware/ff566720)

[**KSPROPERTY\_BDA\_SIGNAL\_LOCK\_CAPS**](ksproperty-bda-signal-lock-caps.md)

 

 






