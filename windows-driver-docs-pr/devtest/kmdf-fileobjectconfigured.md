---
title: FileObjectConfigured rule (kmdf)
description: The FileObjectConfigured rule specifies that a call to the WdfRequestGetFileObject method is preceded by a call to WdfDeviceInitSetFileObjectConfig.
ms.assetid: bec6e071-f7cc-48c7-a01b-e7288ffb6f5e
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["FileObjectConfigured rule (kmdf)"]
topic_type:
- apiref
api_name:
- FileObjectConfigured
api_type:
- NA
ms.localizationpriority: medium
---

# FileObjectConfigured rule (kmdf)


The **FileObjectConfigured** rule specifies that a call to the [**WdfRequestGetFileObject**](https://msdn.microsoft.com/library/windows/hardware/ff549963) method is preceded by a call to [**WdfDeviceInitSetFileObjectConfig**](https://msdn.microsoft.com/library/windows/hardware/ff546107).

|              |      |
|--------------|------|
| Driver model | KMDF |

How to test
-----------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">At compile time</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>FileObjectConfigured</strong> rule.</p>
Use the following steps to run an analysis of your code:
<ol>
<li>[Prepare your code (use role type declarations).](https://msdn.microsoft.com/library/windows/hardware/hh454281#preparing-your-source-code)</li>
<li>[Run Static Driver Verifier.](https://msdn.microsoft.com/library/windows/hardware/hh454281#running-static-driver-verifier)</li>
<li>[View and analyze the results.](https://msdn.microsoft.com/library/windows/hardware/hh454281#viewing-and-analyzing-the-results)</li>
</ol>
<p>For more information, see [Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281).</p></td>
</tr>
</tbody>
</table>

Applies to
----------

[**WdfDeviceInitSetFileObjectConfig**](https://msdn.microsoft.com/library/windows/hardware/ff546107)
[**WdfRequestGetFileObject**](https://msdn.microsoft.com/library/windows/hardware/ff549963)
 

 





