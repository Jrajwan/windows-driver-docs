---
title: Iasphelp get\_PageRateUnit method
author: windows-driver-content
description: The PageRateUnit enables an ASP Web page to determine the units in which the page rate is expressed.
MS-HAID:
- 'webfnc\_c3c557fb-2ce9-4260-838a-4bd0e56fb63d.xml'
- 'print.iasphelp\_pagerateunit'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 1b528527-a03a-4fab-b118-5c744759a0a1
keywords: ["get_PageRateUnit method Print Devices", "get_PageRateUnit method Print Devices , Iasphelp interface", "Iasphelp interface Print Devices , get_PageRateUnit method"]
topic_type:
- apiref
api_name:
- Iasphelp.get_PageRateUnit
api_type:
- COM
ms.localizationpriority: medium
---

# Iasphelp::get\_PageRateUnit method


The **PageRateUnit** enables an ASP Web page to determine the units in which the page rate is expressed.

Syntax
------

```ManagedCPlusPlus
HRESULT get_PageRateUnit(
  [out] long *pVal
);
```

Parameters
----------

*pVal* \[out\]  
A caller-supplied pointer to a memory location that receives a value that indicates the units used in the page rate. The four possible values are shown in the following table.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>Print rate units are pages per minute.</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>Print rate units are characters per second.</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>Print rate units are lines per minute.</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Print rate units are inches per minute.</p></td>
</tr>
</tbody>
</table>

 

These values correspond to the constants PRINTRATEUNIT\_PPM, PRINTRATEUNIT\_CPS, PRINTRATEUNIT\_LPM, and PRINTRATEUNIT\_IPM, which are defined in the Wingdi.h header file. For more information about these constants, see the description of the **DeviceCapabilities** function in the Windows SDK documentation.

Return value
------------

This property returns one of the values in the following table.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Return code</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>S_OK</strong></td>
<td><p>The operation succeeded.</p></td>
</tr>
<tr class="even">
<td><strong>E_HANDLE</strong></td>
<td><p>The [<strong>Iasphelp::Open</strong>](iasphelp-open.md) method has not been called.</p></td>
</tr>
<tr class="odd">
<td><strong>E_OUTOFMEMORY</strong></td>
<td><p>Out of memory.</p></td>
</tr>
</tbody>
</table>

 

### <span id="vbscript_example"></span><span id="VBSCRIPT_EXAMPLE"></span>VBScript Example

Remarks
-------

Query this property to determine the units in which the [**Iasphelp::PageRate**](iasphelp-pagerate.md) property value is expressed.

The [**Iasphelp::Open**](iasphelp-open.md) method must be called before the **Iasphelp::PageRateUnit** property can be queried.

```
    Dim objPrinter, PtrPageRateUnit
    strPrinter = Session("MS_printer")
    Set objPrinter = Server.CreateObject ("OlePrn.AspHelp")
    objPrinter.Open strPrinter
    PtrPageRate = objPrinter.PageRateUnit
```

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Target platform</p></td>
<td>Desktop</td>
</tr>
<tr class="even">
<td><p>Version</p></td>
<td><p>Available in Windows 2000 and later versions of the Windows operating systems.</p></td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**Iasphelp::PageRate**](iasphelp-pagerate.md)

[**Iasphelp::Open**](iasphelp-open.md)

 

 




