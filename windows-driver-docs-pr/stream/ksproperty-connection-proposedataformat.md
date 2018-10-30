---
title: KSPROPERTY\_CONNECTION\_PROPOSEDATAFORMAT
description: Clients can use the KSPROPERTY\_CONNECTION\_PROPOSEDATAFORMAT property to propose a new data format for the connection.
ms.assetid: f5bc7cd2-0033-4761-962b-33c82925134b
keywords: ["KSPROPERTY_CONNECTION_PROPOSEDATAFORMAT Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CONNECTION_PROPOSEDATAFORMAT
api_location:
- ks.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_CONNECTION\_PROPOSEDATAFORMAT


Clients can use the KSPROPERTY\_CONNECTION\_PROPOSEDATAFORMAT property to propose a new data format for the connection.

## <span id="ddk_ksproperty_connection_proposedataformat_ks"></span><span id="DDK_KSPROPERTY_CONNECTION_PROPOSEDATAFORMAT_KS"></span>


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
<th>Property Descriptor Type</th>
<th>Property Value Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KSDATAFORMAT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff561656)</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

This property returns a [**KSDATAFORMAT**](https://msdn.microsoft.com/library/windows/hardware/ff561656) specifying the proposed data format.

The KS filter returns STATUS\_SUCCESS if the pin can be reset to the proposed data format, or an error code otherwise. Note that this property request does not change the data format. Clients use [**KSPROPERTY\_CONNECTION\_DATAFORMAT**](ksproperty-connection-dataformat.md) to change the format.

Also see [KS Data Formats and Data Ranges](https://msdn.microsoft.com/library/windows/hardware/ff567632).

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
<td>Ks.h (include Ks.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY\_CONNECTION\_DATAFORMAT**](ksproperty-connection-dataformat.md)

[*AVStrMiniPinSetDataFormat*](https://msdn.microsoft.com/library/windows/hardware/ff556355)

 

 






