---
title: ZwRegistryOpen rule (wdm)
ms.assetid: c98682c3-0d38-4d5b-9649-7574106f9ce3
ms.author: windowsdriverdev
ms.date: 05/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
description: 
keywords: ["ZwRegistryOpen rule (wdm)"]
topic_type:
- apiref
api_name:
- ZwRegistryOpen
api_type:
- NA
ms.localizationpriority: medium
---

# ZwRegistryOpen rule (wdm)


The [**ZwRegistryOpen**](storport-zwregistryopen.md) rule specifies that after calling [**ZwOpenKey**](https://msdn.microsoft.com/library/windows/hardware/ff567014), the driver calls the following registry functions only while holding an open handle to a registry key (that is, before calling [**ZwClose**](https://msdn.microsoft.com/library/windows/hardware/ff566417) or [**ZwDeleteKey**](https://msdn.microsoft.com/library/windows/hardware/ff566437)):

-   [**ZwClose**](https://msdn.microsoft.com/library/windows/hardware/ff566417)

-   [**ZwDeleteKey**](https://msdn.microsoft.com/library/windows/hardware/ff566437)

-   [**ZwEnumerateKey**](https://msdn.microsoft.com/library/windows/hardware/ff566447)

-   [**ZwEnumerateValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff566453)

-   [**ZwFlushKey**](https://msdn.microsoft.com/library/windows/hardware/ff566457)

-   [**ZwQueryKey**](https://msdn.microsoft.com/library/windows/hardware/ff567060)

-   [**ZwQueryValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567069)

-   [**ZwSetValueKey**](https://msdn.microsoft.com/library/windows/hardware/ff567109)

This rule also specifies that the driver must not call [**ZwOpenKey**](https://msdn.microsoft.com/library/windows/hardware/ff567014) if it is already holding an open handle to that registry key.

Finally, this rule specifies that the driver must not return from the dispatch routine or cancel routine while holding an open handle to a registry key.

This rule does not verify that the driver is holding an open handle to the correct registry key when it calls [**ZwClose**](https://msdn.microsoft.com/library/windows/hardware/ff566417) or [**ZwDeleteKey**](https://msdn.microsoft.com/library/windows/hardware/ff566437).

|              |     |
|--------------|-----|
| Driver model | WDM |

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
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>ZwRegistryOpen</strong> rule.</p>
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
See also
--------

[**ZwRegistryCreate**](wdm-zwregistrycreate.md)
 

 





