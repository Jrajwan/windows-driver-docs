---
title: Warning rule set (Storport)
description: Use these rules to verify that your driver can correctly processes IRPs in various contexts and follows Microsoft recommended best practices.
ms.assetid: 6557A741-C49F-456B-B285-DE6D171DDCEE
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Warning rule set (Storport)


Use these rules to verify that your driver can correctly processes IRPs in various contexts and follows Microsoft recommended best practices.

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
<td align="left"><p>[<strong>PagedCode</strong>](storport-pagedcode.md)</p></td>
<td align="left"><p>This rule verifies that when the [<strong>PAGED_CODE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff558773) macro is called, the driver is at <strong>IRQL &lt; DISPATCH_LEVEL</strong>. Any code executing at <strong>IRQL &gt;= DISPATCH_LEVEL</strong> must be in non-paged memory to avoid causing page faults.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<strong>StorPortStatusPending</strong>](storport-storportstatuspending.md)</p></td>
<td align="left"><p>This rule checks that an SRB is not completed with status <strong>SRB_STATUS_PENDING</strong>.</p></td>
</tr>
</tbody>
</table>

 

**To select the Warning rule set**

1.  Select your driver project (.vcxProj) in Microsoft Visual Studio. From the **Driver** menu, click **Launch Static Driver Verifier…**.

2.  Click the **Rules** tab. Under **Rule Sets**, select **Warning**.

    To select the default rule set from a Visual Studio developer command prompt window, specify **Warning.sdv** with the **/check** option. For example:

    ```
    msbuild /t:sdv /p:Inputs="/check:Warning.sdv" mydriver.VcxProj /p:Configuration="Win8 Release" /p:Platform=Win32
    ```

    For more information, see [Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281) and [Static Driver Verifier commands (MSBuild)](https://msdn.microsoft.com/library/windows/hardware/hh466459).

 

 





