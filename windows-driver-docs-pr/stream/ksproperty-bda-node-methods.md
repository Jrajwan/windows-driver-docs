---
title: KSPROPERTY\_BDA\_NODE\_METHODS
description: Clients use KSPROPERTY\_BDA\_NODE\_METHODS to retrieve a list of methods supported on a node.
ms.assetid: 143456dc-1910-4db4-8584-9cd19d09e8ce
keywords: ["KSPROPERTY_BDA_NODE_METHODS Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_BDA_NODE_METHODS
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

# KSPROPERTY\_BDA\_NODE\_METHODS


Clients use KSPROPERTY\_BDA\_NODE\_METHODS to retrieve a list of methods supported on a node.

## <span id="ddk_ksproperty_bda_node_methods_ks"></span><span id="DDK_KSPROPERTY_BDA_NODE_METHODS_KS"></span>


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
<td><p>Filter</p></td>
<td><p>KSPROPERTY</p></td>
<td><p>List of GUIDs</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The list of methods supported by a node is a list of GUIDs.

The network provider will use this property to query the capabilities of each node in the BDA template connection list.

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


[**BdaPropertyNodeMethods**](https://msdn.microsoft.com/library/windows/hardware/ff556491)

[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

 

 






