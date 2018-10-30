---
title: KSPROPERTY\_BDA\_PIDFILTER\_LIST\_PIDS
description: Clients use KSPROPERTY\_BDA\_PIDFILTER\_LIST\_PIDS to retrieve from a PID filter node the list of its PIDs that identify groups of packets that the node delivers from the input stream to the output stream.
ms.assetid: fc7dc0af-af74-4bd1-b99c-f06de25aae3c
keywords: ["KSPROPERTY_BDA_PIDFILTER_LIST_PIDS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_BDA_PIDFILTER_LIST_PIDS
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

# KSPROPERTY\_BDA\_PIDFILTER\_LIST\_PIDS


Clients use KSPROPERTY\_BDA\_PIDFILTER\_LIST\_PIDS to retrieve from a PID filter node the list of its PIDs that identify groups of packets that the node delivers from the input stream to the output stream.

## <span id="ddk_ksproperty_bda_pidfilter_list_pids_ks"></span><span id="DDK_KSPROPERTY_BDA_PIDFILTER_LIST_PIDS_KS"></span>


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
<td><p>Yes</p></td>
<td><p>Filter</p></td>
<td><p>KSP_NODE</p></td>
<td><p>List of PIDs</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The **NodeId** member of KSP\_NODE specifies the identifier of the PID filter node.

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


[**KSP\_NODE**](https://msdn.microsoft.com/library/windows/hardware/ff566720)

 

 






