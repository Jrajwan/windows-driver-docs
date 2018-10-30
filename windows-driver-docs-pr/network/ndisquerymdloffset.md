---
title: NdisQueryMdlOffset macro
author: windows-driver-content
description: The NdisQueryMdlOffset macro retrieves the offset within a physical page at which a given MDL buffer begins and the length of the buffer.
ms.assetid: d6f23e9c-5015-4087-b7a2-badee00bdafa
ms.author: windowsdriverdev 
ms.date: 07/18/2017 
ms.topic: article 
ms.prod: windows-hardware 
ms.technology: windows-devices 
keywords:
 - NdisQueryMdlOffset macro Network Drivers Starting with Windows Vista
ms.localizationpriority: medium
---

# NdisQueryMdlOffset macro


The **NdisQueryMdlOffset** macro retrieves the offset within a physical page at which a given MDL buffer begins and the length of the buffer.

Syntax
------

```ManagedCPlusPlus
VOID NdisQueryMdlOffset(
    _Mdl,
    _Offset,
    _Length
);
```

Parameters
----------

*\_Mdl*   
A pointer to an MDL.

*\_Offset*   
A pointer to a caller-supplied variable in which this macro returns the zero-based byte offset within the physical page that contains the MDL-specified buffer.

*\_Length*   
A pointer to a caller-supplied variable in which this macro returns the length, in bytes, of the virtual address range that is specified by the MDL.

Return value
------------

None

Remarks
-------

The **NdisQueryMdlOffset** macro provides an MDL-based version of the [**NdisQueryBufferOffset**](https://msdn.microsoft.com/library/windows/hardware/ff554411) function.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Target platform</p></td>
<td>Desktop</td>
</tr>
<tr class="even">
<td><p>Version</p></td>
<td><p>Supported in NDIS 6.0 and later.</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td>Ndis.h (include Ndis.h)</td>
</tr>
<tr class="even">
<td><p>IRQL</p></td>
<td><p>&lt;= DISPATCH_LEVEL</p></td>
</tr>
<tr class="odd">
<td><p>DDI compliance rules</p></td>
<td>[<strong>Irql_NetBuffer_Function</strong>](https://msdn.microsoft.com/library/windows/hardware/ff547985)</td>
</tr>
</tbody>
</table>

## See also


[**NdisQueryBufferOffset**](https://msdn.microsoft.com/library/windows/hardware/ff554411)

 

 




