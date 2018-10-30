---
title: Macros Defined by RDBSS
author: windows-driver-content
description: Macros Defined by RDBSS
ms.assetid: 11add885-ecd9-4b43-be42-ef060e847183
keywords:
- RDBSS WDK file systems , macros
- Redirected Drive Buffering Subsystem WDK file systems , macros
- macros WDK RDBSS
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Macros Defined by RDBSS


## <span id="ddk_macros_defined_by_rdbss_if"></span><span id="DDK_MACROS_DEFINED_BY_RDBSS_IF"></span>


A number of useful macros are defined in the Window Driver Kit (WDK)header files that call these RDBSS routines or other kernel routines. Some of these macros are normally used instead of calling the RDBSS routines directly. Some of these macros are used as convenience routines.

The following macros are defined by RDBSS.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Macro</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>RxAcquirePrefixTableLockExclusive</strong> (<em>TABLE</em>, <em>WAIT</em>)</p></td>
<td align="left"><p>This macro acquires the prefix table lock in exclusive mode for change operations.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxAcquirePrefixTableLockShared</strong> (<em>TABLE</em>, <em>WAIT</em>)</p></td>
<td align="left"><p>This macro acquires the prefix table lock in shared mode for lookup operations.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxAllocatePoolWithTag</strong> (<em>type</em>, <em>size</em>, <em>tag</em>)</p></td>
<td align="left"><p>On checked builds, this macro allocates memory from a pool with a four-byte tag at the beginning of the block that can be used to help catch instances of memory trashing.</p>
<p>On retail builds, this macro becomes a direct call to [<strong>ExAllocatePoolWithTag</strong>](https://msdn.microsoft.com/library/windows/hardware/ff544520).</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxCheckMemoryBlock</strong> (<em>ptr</em>)</p></td>
<td align="left"><p>On checked builds, this macro checks a memory block for a special RX_POOL_HEADER header signature.</p>
<p>On retail builds, this macro does nothing.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxDereferenceAndFinalizeNetFcb</strong> (<em>Fcb ,RxContext</em>, <em>RecursiveFinalize</em>, <em>ForceFinalize</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on FCB structures.</p>
<p>Note that this macro manipulates the reference count and also returns the status of the final dereference call.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxDereferenceNetFcb</strong> (<em>Fcb</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on FCB structures.</p>
<p>Note that this macro manipulates the reference count and also returns the status of the final dereference call.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxDereferenceNetFobx</strong> (<em>Fobx,LockHoldingState</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on FOBX structures.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxDereferenceNetRoot</strong> (<em>NetRoot</em>, <em>LockHoldingState</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on NET_ROOT structures.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxDereferenceSrvCall</strong> (<em>SrvCall</em>, <em>LockHoldingState</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on SRV_CALL structures.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxDereferenceSrvOpen</strong> ( <em>SrvOpen</em>, <em>LockHoldingState</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on SRV_OPEN structures.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxDereferenceVNetRoot</strong> ( <em>VNetRoot</em>, <em>LockHoldingState</em>)</p></td>
<td align="left"><p>This macro is used to track dereference operations on V_NET_ROOT structures.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxFcbAcquiredShared</strong> (<em>RXCONTEXT</em>, <em>FCB</em>)</p></td>
<td align="left"><p>This macro checks if the current thread has access to the regular resource in shared mode. This macro calls the [<strong>ExIsResourceAcquiredSharedLite</strong>](https://msdn.microsoft.com/library/windows/hardware/ff545477) routine.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxFillAndInstallFastIoDispatch</strong>(<em>__devobj</em>, <em>__fastiodisp</em>)</p></td>
<td align="left"><p>This macro calls [<strong>__RxFillAndInstallFastIoDispatch</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557374) to fill out a fast I/O dispatch vector to be identical with the normal dispatch I/O vector and installs it into the driver object associated with the device object passed.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxFreePool</strong> (<em>ptr</em>)</p></td>
<td align="left"><p>On checked builds, this macro frees a memory pool.</p>
<p>On retail builds, this macro becomes a direct call to [<strong>ExFreePool</strong>](https://msdn.microsoft.com/library/windows/hardware/ff544590).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxIsFcbAcquiredShared</strong> (<em>FCB</em>)</p></td>
<td align="left"><p>This macro checks if the current thread has access to the regular resource in shared mode. This macro calls the [<strong>ExIsResourceAcquiredSharedLite</strong>](https://msdn.microsoft.com/library/windows/hardware/ff545477) routine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxIsFcbAcquiredExclusive</strong> (<em>FCB</em>)</p></td>
<td align="left"><p>This macro checks if the current thread has access to the regular resource in exclusive mode. This macro calls the [<strong>ExIsResourceAcquiredExclusiveLite</strong>](https://msdn.microsoft.com/library/windows/hardware/ff545458) routine.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxIsFcbAcquired</strong> (<em>FCB</em>)</p></td>
<td align="left"><p>This macro checks if the current thread has access to the regular resource in either shared or exclusive mode. This macro calls the [<strong>ExIsResourceAcquiredSharedLite</strong>](https://msdn.microsoft.com/library/windows/hardware/ff545477) and [<strong>ExIsResourceAcquiredExclusiveLite</strong>](https://msdn.microsoft.com/library/windows/hardware/ff545458) routines.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxIsPrefixTableLockAcquired</strong> (<em>TABLE</em>)</p></td>
<td align="left"><p>This macro indicates if the prefix table lock was acquired in either exclusive or shared mode.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxIsPrefixTableLockExclusive</strong> (<em>TABLE</em>)</p></td>
<td align="left"><p>This macro indicates if the prefix table lock was acquired in exclusive mode.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxLog</strong>(<em>Args</em>)</p></td>
<td align="left"><p>On checked builds, this macro calls the [<strong>_RxLog</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557368) routine.</p>
<p>On retail builds, this macro does nothing.</p>
<p>Note that the arguments to <strong>RxLog</strong> must be enclosed with an additional pair of parenthesis to enable translation into a null call when logging should be turned off.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxLogEvent</strong> (<em>_DeviceObject</em>, <em>_OriginatorId</em>, <em>_EventId</em>, <em>_Status</em>)</p></td>
<td align="left"><p>This macro calls the [<strong>RxLogEventDirect</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554515) routine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxLogFailure</strong> (<em>_DeviceObject</em>, <em>_OriginatorId</em>, <em>_EventId</em>, <em>_Status</em>)</p></td>
<td align="left"><p>This macro calls the [<strong>RxLogEventDirect</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554515) routine.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxLogFailureWithBuffer</strong> (<em>_DeviceObject</em>, <em>_OriginatorId</em>, <em>_EventId</em>, <em>_Status</em>, <em>_Buffer</em>, <em>_Length</em>)</p></td>
<td align="left"><p>This macro calls the [<strong>RxLogEventWithBufferDirect</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554524) routine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxLogRetail</strong>(<em>Args</em>)</p></td>
<td align="left"><p>On checked builds, this macro calls the [<strong>_RxLog</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557368) routine.</p>
<p>On retail builds, this macro does nothing.</p>
<p>Note that the arguments to <strong>RxLogRetail</strong> must be enclosed with an additional pair of parenthesis to enable translation into a null call when logging should be turned off.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxReferenceNetFcb</strong> (<em>Fcb</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on FCB structures.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxReferenceNetFobx</strong> (<em>Fobx</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on FOBX structures. A log of these reference operations can be accessed by the logging system and WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxReferenceNetRoot</strong> (<em>NetRoot</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on NET_ROOT structures. A log of these reference operations can be accessed by the logging system and Windows Management Instrumentation (WMI).</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxReferenceSrvCall</strong> (<em>SrvCall</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on SRV_CALL structures that are not at Deferred Procedure Call (DPC) level.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxReferenceSrvCallAtDpc</strong> (<em>SrvCall</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on SRV_CALL structures at DPC level.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxReferenceSrvOpen</strong> (<em>SrvOpen</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on SRV_OPEN structures.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxReferenceVNetRoot</strong> (<em>VNetRoot</em>)</p></td>
<td align="left"><p>This macro is used to track reference operations on V_NET_ROOT structures.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxReleasePrefixTableLock</strong> (<em>TABLE</em>)</p></td>
<td align="left"><p>This macro frees the prefix table lock.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RxSynchronizeBlockingOperations</strong>(<em>RXCONTEXT</em>,<em>FCB</em>,<em>IOQUEUE</em>)</p></td>
<td align="left"><p>This macro synchronizes blocking I/O requests to the same work queue. On Windows Server 2003, this macro calls the [<strong>__RxSynchronizeBlockingOperations</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557377) routine with the <em>DropFcbLock</em> parameter set to <strong>FALSE</strong>.</p>
<p>On Windows XP and Windows 2000, this macro calls the [<strong>__RxSynchronizeBlockingOperationsMaybeDroppingFcbLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557382) routine with the <em>DropFcbLock</em> parameter set to <strong>FALSE</strong>.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RxSynchronizeBlockingOperations</strong>(<em>RXCONTEXT</em>,<em>FCB</em>,<em>IOQUEUE</em>)</p></td>
<td align="left"><p>This macro synchronizes blocking I/O requests to the same work queue. On Windows Server 2003, this macro calls the [<strong>__RxSynchronizeBlockingOperations</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557377) routine with the <em>DropFcbLock</em> parameter set to <strong>TRUE</strong>.</p>
<p>On Windows XP and Windows 2000, this macro calls the [<strong>__RxSynchronizeBlockingOperationsMaybeDroppingFcbLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff557382) routine with the <em>DropFcbLock</em> parameter set to <strong>TRUE</strong>.</p></td>
</tr>
</tbody>
</table>

 

 

 




