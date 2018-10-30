---
title: Iasphelp get\_MibErrorDscp method
author: windows-driver-content
description: The MibErrorDscp property enables an ASP Web page to convert a Simple Network Management Protocol (SNMP) management information base (MIB) error code into a text description of the error.
MS-HAID:
- 'webfnc\_3931fbc6-1960-4d40-a6e3-8816ee832c89.xml'
- 'print.iasphelp\_miberrordscp'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: b2ab9414-8401-4ec4-a235-f6a8da93523b
keywords: ["get_MibErrorDscp method Print Devices", "get_MibErrorDscp method Print Devices , Iasphelp interface", "Iasphelp interface Print Devices , get_MibErrorDscp method"]
topic_type:
- apiref
api_name:
- Iasphelp.get_MibErrorDscp
api_type:
- COM
ms.localizationpriority: medium
---

# Iasphelp::get\_MibErrorDscp method


The **MibErrorDscp** property enables an ASP Web page to convert a Simple Network Management Protocol (SNMP) management information base (MIB) error code into a text description of the error.

Syntax
------

```ManagedCPlusPlus
HRESULT get_MibErrorDscp(
  [in]  DWORD dwError,
  [out] BSTR  *pVal
);
```

Parameters
----------

*dwError* \[in\]  
Caller-supplied SNMP MIB error code.

*pVal* \[out\]  
Caller-supplied location to receive a pointer to a string containing a text description of the error.

Return value
------------

Win32 error codes can also be returned.

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
<td><strong>E_POINTER</strong></td>
<td><p>Invalid <em>pVal</em> pointer.</p></td>
</tr>
<tr class="odd">
<td><strong>E_OUTOFMEMORY</strong></td>
<td><p>Out of memory.</p></td>
</tr>
</tbody>
</table>

 

## <span id="ddk_iasphelp_miberrordscp_gg"></span><span id="DDK_IASPHELP_MIBERRORDSCP_GG"></span>


### <span id="vbscript_example"></span><span id="VBSCRIPT_EXAMPLE"></span>VBScript Example

Remarks
-------

```
    Dim objPrinter, MIBErrorCode, MIBErrorString
    Set objPrinter = Server.CreateObject ("OlePrn.AspHelp")
    ...
 &#39; Get error code from MIB.
    ...
    MIBErrorString = objPrinter.MibErrorDscp(ErrorCodeMIB)
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

 

 




