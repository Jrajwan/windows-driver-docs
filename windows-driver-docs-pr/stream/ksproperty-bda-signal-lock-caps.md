---
title: KSPROPERTY\_BDA\_SIGNAL\_LOCK\_CAPS
description: Clients use KSPROPERTY\_BDA\_SIGNAL\_LOCK\_CAPS to determine the lock types that the driver can support for a signal.
ms.assetid: 753f1a3c-5308-49a6-96ee-f7d0090f021a
keywords: ["KSPROPERTY_BDA_SIGNAL_LOCK_CAPS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_BDA_SIGNAL_LOCK_CAPS
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

# KSPROPERTY\_BDA\_SIGNAL\_LOCK\_CAPS


Clients use KSPROPERTY\_BDA\_SIGNAL\_LOCK\_CAPS to determine the lock types that the driver can support for a signal.

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
<td><p>A 32-bit value that contains a bitwise OR of [<strong>BDA_LockType</strong>](https://msdn.microsoft.com/library/windows/hardware/ff556526)-typed values</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The **NodeId** member of KSP\_NODE specifies the identifier of the control node or is set to −1 to specify a pin.

The returned 32-bit value is a bitwise OR of [**BDA\_LockType**](https://msdn.microsoft.com/library/windows/hardware/ff556526)-typed values that indicates the lock types that the driver supports.

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

[**KSPROPERTY\_BDA\_SIGNAL\_LOCK\_TYPE**](ksproperty-bda-signal-lock-type.md)

 

 






