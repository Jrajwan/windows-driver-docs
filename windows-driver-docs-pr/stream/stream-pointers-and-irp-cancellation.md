---
title: Stream Pointers and IRP Cancellation
author: windows-driver-content
description: Stream Pointers and IRP Cancellation
ms.assetid: ce392496-ca07-497d-af8a-709239a7bd5e
keywords:
- stream pointers WDK AVStream , IRP cancellations
- IRP cancellations WDK AVStream
- canceling IRPs WDK AVStream
- locked stream pointers WDK AVStream
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Stream Pointers and IRP Cancellation





If a frame has a locked stream pointer referencing it, the IRP that corresponds to this frame cannot be canceled. See [Locking and Unlocking Stream Pointers](locking-and-unlocking-stream-pointers.md).

The following table lists techniques that your minidriver can use to support IRP cancellation. Your cancellation strategy should be based on the stream access requirements of your minidriver, as described in the leftmost column.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>If you need..</th>
<th>Do this</th>
<th>Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Brief access to stream data at a single access point</p></td>
<td><p>Call [<strong>KsPinGetLeadingEdgeStreamPointer</strong>](https://msdn.microsoft.com/library/windows/hardware/ff563513) with the <em>State</em> parameter set to KSSTREAM_POINTER_STATE_LOCKED. Then call [<strong>KsStreamPointerUnlock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567137) or [<strong>KsStreamPointerAdvanceOffsetsAndUnlock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567127) immediately after processing is complete.</p></td>
<td><p>Provides fast responsiveness to cancellation unless the thread blocks between acquiring the pointer and unlocking it.</p></td>
</tr>
<tr class="even">
<td><p>Indefinite length of access time, but can relinquish the claim in the context of a cancellation callback</p></td>
<td><p>Call [<strong>KsStreamPointerClone</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567129) to clone a locked stream pointer (usually the leading edge), unlock it, and respond to <em>CancelCallback</em>. The callback occurs with the queue's spin lock held, hence at DISPATCH_LEVEL. Accordingly, the vendor-supplied <em>CancelCallback</em> routine cannot perform queue manipulation or call functions that acquire a mutex. Instead, in the callback routine, the minidriver verifies that the associated data will not be accessed later, and then calls [<strong>KsStreamPointerDelete</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567130).</p></td>
<td><p>Can be more difficult to implement, but often provides the best balance between efficient access and quick response to cancellation.</p></td>
</tr>
<tr class="odd">
<td><p>Periodic access to a frame and can tolerate the disappearance of the frame between accesses</p></td>
<td><p>Maintain an unlocked clone and call [<strong>KsStreamPointerLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567134) to lock it at access time. If the frame is canceled, the next attempt to lock the stream pointer fails, and the minidriver can call [<strong>KsStreamPointerDelete</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567130).</p></td>
<td><p>As with the first option, responsiveness to cancellation is a function of how long the stream pointer is locked.</p></td>
</tr>
<tr class="even">
<td><p>Indefinite length of access time and cannot relinquish the claim in response to a callback</p></td>
<td><p>Maintain a locked clone stream pointer for any length of time to prevent cancellation. To create a clone stream pointer, call [<strong>KsStreamPointerClone</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567129). Then call [<strong>KsStreamPointerLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567134) and [<strong>KsStreamPointerUnlock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567137) to lock or unlock the clone.</p></td>
<td><p>Responsiveness to cancellation may be poor. Consider using [<strong>stream pointer timeouts</strong>](https://msdn.microsoft.com/library/windows/hardware/ff567135) with this technique.</p></td>
</tr>
</tbody>
</table>

 

If a frame has a stream pointer referencing it, the minidriver can call [**KsStreamPointerGetIrp**](https://msdn.microsoft.com/library/windows/hardware/ff567131) to access the IRP corresponding to this frame. To retrieve the memory descriptor list (MDL) associated with a frame, call [**KsStreamPointerGetMdl**](https://msdn.microsoft.com/library/windows/hardware/ff567132).

 

 




