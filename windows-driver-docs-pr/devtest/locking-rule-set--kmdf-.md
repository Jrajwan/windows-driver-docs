---
title: Locking rule set (KMDF)
description: Use these rules to verify that your driver correctly manages shared resources.
ms.assetid: B6DD41A5-E7E5-4070-8752-68E26804A5D5
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Locking rule set (KMDF)


Use these rules to verify that your driver correctly manages shared resources.

## In this section


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Topic</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>[<strong>ParentObjectCheckLock</strong>](kmdf-parentobjectchecklock.md)</p></td>
<td align="left"><p>The [<strong>ParentObjectCheckLock</strong>](kmdf-parentobjectchecklock.md) rule specifies that the driver should call [<strong>WdfWaitLockCreate</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551171) and [<strong>WdfSpinLockCreate</strong>](https://msdn.microsoft.com/library/windows/hardware/ff550042) setting a parent object.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>ReqSendWhileSpinlock</strong>](kmdf-reqsendwhilespinlock.md)</p></td>
<td align="left"><p>The [<strong>ReqSendWhileSpinlock</strong>](kmdf-reqsendwhilespinlock.md) rule specifies that no requests are sent while the driver holds a spinlock.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<strong>Spinlock</strong>](kmdf-spinlock.md)</p></td>
<td align="left"><p>The [<strong>Spinlock</strong>](kmdf-spinlock.md) rule specifies that calls to [<strong>KeAcquireSpinLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551917) or [<strong>KeAcquireSpinLockRaiseToDpc</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551928) and [<strong>KeReleaseSpinlock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff553145) are used in strict alternation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>SpinlockDpc</strong>](kmdf-spinlockdpc.md)</p></td>
<td align="left"><p>The [<strong>SpinlockDpc</strong>](kmdf-spinlockdpc.md) rule specifies that calls to [<strong>KeAcquireSpinLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551917) or [<strong>KeAcquireSpinLockRaiseToDpc</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551928) and [<strong>KeReleaseSpinlock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff553145) are used in strict alternation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<strong>SpinlockRelease</strong>](kmdf-spinlockrelease.md)</p></td>
<td align="left"><p>The [<strong>SpinlockRelease</strong>](kmdf-spinlockrelease.md) rule specifies that calls to [<strong>KeAcquireSpinLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551917), [<strong>KeAcquireSpinLockRaiseToDpc</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551928), and [<strong>KeReleaseSpinLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff553145) are used in a balanced way within a KMDF callback. At the end of any KMDF callback routine, the driver should not hold the spin lock.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>WdfInterruptLock</strong>](kmdf-wdfinterruptlock.md)</p></td>
<td align="left"><p>The [<strong>WdfInterruptLock</strong>](kmdf-wdfinterruptlock.md) rule specifies that calls to the [<strong>WdfInterruptAcquireLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff547340) method is used in strict alternation with calls to [<strong>WdfInterruptReleaseLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff547376). Moreover, at the end of any KMDF callback routine, the driver should not hold the framework spin lock object, obtained by a previous call to <strong>WdfInterruptAcquireLock</strong>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<strong>WdfInterruptLockRelease</strong>](kmdf-wdfinterruptlockrelease.md)</p></td>
<td align="left"><p>The [<strong>WdfInterruptLockRelease</strong>](kmdf-wdfinterruptlockrelease.md) rule specifies that calls to [<strong>WdfInterruptAcquireLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff547340) and [<strong>WdfInterruptReleaseLock</strong>](https://msdn.microsoft.com/library/windows/hardware/ff547376) are used in a balanced way within a KMDF callback routine. At the end of any KMDF callback routine, the driver should not hold the framework spin lock object that was obtained by a previous call to <strong>WdfInterruptAcquireLock</strong>.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>WdfSpinlock</strong>](kmdf-wdfspinlock.md)</p></td>
<td align="left"><p>The [<strong>WdfSpinlock</strong>](kmdf-wdfspinlock.md) rule specifies that calls to the [<strong>WdfSpinLockAcquire</strong>](https://msdn.microsoft.com/library/windows/hardware/ff550040) method are used in strict alternation with [<strong>WdfSpinlockRelease</strong>](kmdf-wdfspinlockrelease.md). At the end of any KMDF callback routine, the driver should not hold the framework spinlock object that was obtained by a previous call to <strong>WdfSpinLockAcquire</strong>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<strong>WdfSpinlockRelease</strong>](kmdf-wdfspinlockrelease.md)</p></td>
<td align="left"><p>The [<strong>WdfSpinlockRelease</strong>](kmdf-wdfspinlockrelease.md) rule specifies that calls to [<strong>WdfSpinLockAcquire</strong>](https://msdn.microsoft.com/library/windows/hardware/ff550040) and <strong>WdfSpinlockRelease</strong> are used in a balanced way within a KMDF event callback function. When the KMDF event callback function returns, the driver should not hold the framework spin lock object that was obtained by a previous call to <strong>WdfSpinLockAcquire</strong>.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>WdfWaitlock</strong>](kmdf-wdfwaitlock.md)</p></td>
<td align="left"><p>The [<strong>WdfWaitlock</strong>](kmdf-wdfwaitlock.md) rule specifies that calls to [<strong>WdfWaitLockAcquire</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551168) are used in strict alternation with [<strong>WdfWaitlockRelease</strong>](kmdf-wdfwaitlockrelease.md). When the KMDF event callback function returns, the driver should not hold the framework spin lock object that was obtained by a previous call to <strong>WdfWaitLockAcquire</strong>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<strong>WdfWaitlockRelease</strong>](kmdf-wdfwaitlockrelease.md)</p></td>
<td align="left"><p>The [<strong>WdfWaitlockRelease</strong>](kmdf-wdfwaitlockrelease.md) rule specifies that calls to [<strong>WdfWaitLockAcquire</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551168) and [<strong>WdfWaitLockRelease</strong>](https://msdn.microsoft.com/library/windows/hardware/ff551173) are used in a balanced way within a KMDF event callback function. When the KMDF event callback function returns, the driver should not hold the framework spin lock object that was obtained by a previous call to <strong>WdfWaitLockAcquire</strong>.</p></td>
</tr>
</tbody>
</table>

 

**To select the Locking rule set**

1.  Select your driver project (.vcxProj) in Microsoft Visual Studio. From the **Driver** menu, click **Launch Static Driver Verifier…**.

2.  Click the **Rules** tab. Under **Rule Sets**, select **Locking**.

    To select the default rule set from a Visual Studio developer command prompt window, specify **Locking.sdv** with the **/check** option. For example:

    ```
    msbuild /t:sdv /p:Inputs="/check:Locking.sdv" mydriver.VcxProj /p:Configuration="Win8 Release" /p:Platform=Win32
    ```

    For more information, see [Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281) and [Static Driver Verifier commands (MSBuild)](https://msdn.microsoft.com/library/windows/hardware/hh466459).

 

 





