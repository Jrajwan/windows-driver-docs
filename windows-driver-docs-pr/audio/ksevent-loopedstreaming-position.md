---
title: KSEVENT\_LOOPEDSTREAMING\_POSITION
description: The KSEVENT\_LOOPEDSTREAMING\_POSITION event indicates that the audio stream has reached a specified position in a looped buffer.Usage Summary TableTargetEvent Descriptor TypeEvent Value TypePinKSEVENTLOOPEDSTREAMING\_POSITION\_EVENT\_DATA The event value type (operation data) is a LOOPEDSTREAMING\_POSITION\_EVENT\_DATA structure that contains the following information The type of notification that the system will send to the client when the position event occurs.The buffer position that triggers the event.
ms.assetid: 6609ddac-e506-4fab-b580-0def30be2e9c
keywords: ["KSEVENT_LOOPEDSTREAMING_POSITION Audio Devices"]
topic_type:
- apiref
api_name:
- KSEVENT_LOOPEDSTREAMING_POSITION
api_location:
- Ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSEVENT\_LOOPEDSTREAMING\_POSITION


The KSEVENT\_LOOPEDSTREAMING\_POSITION event indicates that the audio stream has reached a specified position in a looped buffer.

**Usage Summary Table**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Target</th>
<th align="left">Event Descriptor Type</th>
<th align="left">Event Value Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Pin</p></td>
<td align="left"><p>[<strong>KSEVENT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff561744)</p></td>
<td align="left"><p>[<strong>LOOPEDSTREAMING_POSITION_EVENT_DATA</strong>](https://msdn.microsoft.com/library/windows/hardware/ff537505)</p></td>
</tr>
</tbody>
</table>

 

The event value type (operation data) is a LOOPEDSTREAMING\_POSITION\_EVENT\_DATA structure that contains the following information:

-   The type of notification that the system will send to the client when the position event occurs.

-   The buffer position that triggers the event.

This event is intended only for internal use by the system.

Remarks
-------

In Windows Server 2003, Windows XP, Windows 2000, Windows Me, and Windows 98, the WavePci and WaveCyclic port drivers contain their own built-in handlers for KSEVENT\_LOOPEDSTREAMING\_POSITION events. WavePci and WaveCyclic miniport drivers should not implement handlers for these events.

In Windows Vista, none of the Wave*Xxx* port drivers implement event handlers or other support for KSEVENT\_LOOPEDSTREAMING\_POSITION events.

A looped buffer is a data buffer for an audio stream of type [**KSINTERFACE\_STANDARD\_LOOPED\_STREAMING**](https://msdn.microsoft.com/library/windows/hardware/ff563381). When a play or record cursor reaches the end of a looped buffer, the cursor wraps around to the start of the buffer.

For more information about looped buffers, buffer positions, and play and record cursors, see [Audio Position Property](https://msdn.microsoft.com/library/windows/hardware/ff536211).

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Header</p></td>
<td align="left">Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSEVENT**](https://msdn.microsoft.com/library/windows/hardware/ff561744)

[**KSINTERFACE\_STANDARD\_LOOPED\_STREAMING**](https://msdn.microsoft.com/library/windows/hardware/ff563381)

[**LOOPEDSTREAMING\_POSITION\_EVENT\_DATA**](https://msdn.microsoft.com/library/windows/hardware/ff537505)

 

 






