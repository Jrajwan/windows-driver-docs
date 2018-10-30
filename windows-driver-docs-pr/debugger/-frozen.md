---
title: frozen
description: The frozen extension displays the state of each processor.
ms.assetid: aa2761b7-e7e1-435e-98d3-bfaac64925bf
keywords: ["processor states", "frozen Windows Debugging"]
ms.author: domars
ms.date: 05/23/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
topic_type:
- apiref
api_name:
- frozen
api_type:
- NA
ms.localizationpriority: medium
---

# !frozen


The **!frozen** extension displays the state of each processor.

```
!frozen
```

### <span id="DLL"></span><span id="dll"></span>DLL

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows 2000</strong></p></td>
<td align="left"><p>Unavailable</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows XP and later</strong></p></td>
<td align="left"><p>Kdexts.dll</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

Here is an example of the output from this extension:

```
0: kd> !frozen
Processor states:
       0 : Current
       1 : Frozen
```

 

 





