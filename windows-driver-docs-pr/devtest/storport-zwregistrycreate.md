---
title: ZwRegistryCreate rule (storport)
description: This rule verifies that the handle to a registry key created with ZwCreateKey is subsequently used correctly by other ZwXxx routines.
ms.assetid: 38CCE6AA-BA42-4305-B193-CB1B1C0F105B
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["ZwRegistryCreate rule (storport)"]
topic_type:
- apiref
api_name:
- ZwRegistryCreate
api_type:
- NA
ms.localizationpriority: medium
---

# ZwRegistryCreate rule (storport)


This rule verifies that the handle to a registry key created with [**ZwCreateKey**](https://msdn.microsoft.com/library/windows/hardware/ff566425) is subsequently used correctly by other *ZwXxx* routines. The [**ZwOpenKey**](https://msdn.microsoft.com/library/windows/hardware/ff567014) routine must not be called on an already open handle. The routines [**ZwEnumerateKey**](https://msdn.microsoft.com/library/windows/hardware/ff566447), [**ZwEnumerateValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff566453), [**ZwFlushKey**](https://msdn.microsoft.com/library/windows/hardware/ff566457), [**ZwQueryKey**](https://msdn.microsoft.com/library/windows/hardware/ff567060), [**ZwQueryValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567069), [**ZwSetValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567109), [**ZwClose**](https://msdn.microsoft.com/library/windows/hardware/ff566417), and [**ZwDeleteKey**](https://msdn.microsoft.com/library/windows/hardware/ff566437) must not be called on a handle that isn't open. The handle must also be closed before returning.

|              |          |
|--------------|----------|
| Driver model | Storport |

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>ZwRegistryCreate</strong> rule.</p>
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

[**ZwClose**](https://msdn.microsoft.com/library/windows/hardware/ff566417)
[**ZwCreateKey**](https://msdn.microsoft.com/library/windows/hardware/ff566425)
[**ZwDeleteKey**](https://msdn.microsoft.com/library/windows/hardware/ff566437)
[**ZwEnumerateKey**](https://msdn.microsoft.com/library/windows/hardware/ff566447)
[**ZwEnumerateValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff566453)
[**ZwFlushKey**](https://msdn.microsoft.com/library/windows/hardware/ff566457)
[**ZwOpenKey**](https://msdn.microsoft.com/library/windows/hardware/ff567014)
[**ZwQueryKey**](https://msdn.microsoft.com/library/windows/hardware/ff567060)
[**ZwQueryValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567069)
[**ZwSetValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567109)
 

 





