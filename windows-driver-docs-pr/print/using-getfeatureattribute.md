---
title: Using GetFeatureAttribute
author: windows-driver-content
description: Using GetFeatureAttribute
ms.assetid: e5050cb1-c178-405d-bb0e-fd7827198bca
keywords:
- GetFeatureAttribute
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Using GetFeatureAttribute





This function is supported only for PPD features. If a certain attribute is not available, **GetFeatureAttribute** returns E\_INVALIDARG.

In the following table, the *pdwDataType* parameter takes values of the [**EATTRIBUTE\_DATATYPE**](https://msdn.microsoft.com/library/windows/hardware/ff548692) enumerated type.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feature Attribute</th>
<th>Output Parameters</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DisplayName</strong></p></td>
<td><p><em>*pdwDataType</em>: kADT_UNICODE</p>
<p><em>pbData</em>: null-terminated Unicode string of the feature keyword name's translation string</p>
<p><em>*pcbNeeded</em>: byte count of the Unicode string pointed to by <em>pbData</em> (including the null terminator)</p>
<p>This feature attribute is available to any PPD feature <strong>EnumFeatures</strong> can return.</p></td>
</tr>
<tr class="even">
<td><p><strong>DefaultOption</strong></p></td>
<td><p><em>*pdwDataType</em>: kADT_ASCII</p>
<p><em>pbData</em>: null-terminated ASCII string of the default option keyword name</p>
<p><em>*pcbNeeded</em>: byte count of the ASCII string pointed to by <em>pbData</em> (including the null terminator)</p>
<p>This feature attribute is available to any PPD feature <strong>EnumFeatures</strong> can return.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenUIType</strong></p></td>
<td><p><em>*pdwDataType</em>: kADT_ASCII</p>
<p><em>pbData</em>: null-terminated ASCII string containing one of following types: &quot;PickOne&quot;, &quot;PickMany&quot;, &quot;Boolean&quot;.</p>
<p><em>*pcbNeeded</em>: byte count of the ASCII string pointed to by <em>pbData</em> (including the null terminator)</p>
<p>This feature attribute is available to any PPD feature <strong>EnumFeatures</strong> can return.</p></td>
</tr>
<tr class="even">
<td><p><strong>OpenGroupType</strong></p></td>
<td><p><em>*pdwDataType</em>: kADT_ASCII</p>
<p><em>pbData</em>: For features defined within the PPD's &quot;*OpenGroup: InstallableOptions ... *CloseGroup: InstallableOptions&quot; pair, a null-terminated ASCII string of &quot;InstallableOptions&quot; will be returned. For other features, an empty ASCII string (which has only the null terminator) will be returned.</p>
<p><em>*pcbNeeded</em>: byte count of the ASCII string pointed to by <em>pbData</em> (including the null terminator)</p>
<p>This feature attribute is available to any PPD feature that <strong>EnumFeatures</strong> can return.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OrderDependencyValue</strong></p></td>
<td><p>*pdwDataType: kADT_LONG</p>
<p><em>*pbData</em>: the relative order specified by the PPD's *OrderDependency or *NonUIOrderDependency keyword for this feature. Notice that the first parameter of these keywords is a real number that is converted to a LONG and returned.</p>
<p><em>*pcbNeeded</em>: <strong>sizeof</strong>(LONG)</p>
<p>This attribute is available only for a PPD feature that has an *OrderDependency or *NonUIOrderDependency entry in the PPD, and the entry omits optionKeyword.</p></td>
</tr>
<tr class="even">
<td><p><strong>OrderDependencySection</strong></p></td>
<td><p><em>*pdwDataType</em>: kADT_ASCII</p>
<p><em>pbData</em>: null-terminated ASCII string containing one of following section names: &quot;ExitServer&quot;, &quot;Prolog&quot;, &quot;DocumentSetup&quot;, &quot;PageSetup&quot;, &quot;JCLSetup&quot;, or &quot;AnySetup&quot;.</p>
<p><em>*pcbNeeded</em>: byte count of the ASCII string pointed to by <em>pbData</em> (including the null terminator)</p>
<p>This attribute is available only for a PPD feature that has an *OrderDependency or *NonUIOrderDependency entry in the PPD, and the entry omits optionKeyword.</p></td>
</tr>
</tbody>
</table>

 

 

 




