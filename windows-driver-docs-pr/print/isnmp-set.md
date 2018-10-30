---
title: ISNMP Set method
author: windows-driver-content
description: The Set method enables an ASP Web page to associate a value with an SNMP OID.
MS-HAID:
- 'webfnc\_b0392f7d-7d17-41ce-97fe-8f8baa691c78.xml'
- 'print.isnmp\_set'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 7eac82e7-3f19-4eda-8706-eac6aa2b8dae
keywords: ["Set method Print Devices", "Set method Print Devices , ISNMP interface", "ISNMP interface Print Devices , Set method"]
topic_type:
- apiref
api_name:
- ISNMP.Set
api_location:
- olesnmp.h
api_type:
- COM
ms.localizationpriority: medium
---

# ISNMP::Set method


The `Set` method enables an ASP Web page to associate a value with an SNMP OID.

Syntax
------

```ManagedCPlusPlus
HRESULT Set(
  [in]  BSTR    bstrOID,
  [out] VARIANT varValue
);
```

Parameters
----------

*bstrOID* \[in\]  
Caller-supplied pointer to an SNMP OID string.

*varValue* \[out\]  
Caller-supplied location containing the OID's value.

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
<td><strong>E_FAIL</strong></td>
<td><p>The <strong>ISNMP::Open</strong> method has not been called.</p></td>
</tr>
<tr class="odd">
<td><strong>E_INVALIDARG</strong></td>
<td><p>The specified SNMP OID is not valid.</p></td>
</tr>
<tr class="even">
<td><strong>E_OUTOFMEMORY</strong></td>
<td><p>Out of memory.</p></td>
</tr>
</tbody>
</table>

 

## <span id="ddk_isnmp_set_gg"></span><span id="DDK_ISNMP_SET_GG"></span>


### <span id="vbscript_example"></span><span id="VBSCRIPT_EXAMPLE"></span>VBScript Example

Remarks
-------

This method calls the **SnmpMgrRequest** function to set SNMP OID values. For more information, see the Windows SDK Documentation.

The [**ISNMP::Open**](isnmp-open.md) method must be called before the `ISNMP::Set` method can be called.

```
    Dim StrIP, strCommunity, objSNMP, OIDValue
    strIP = Session("MS_IPaddress")
    strCommunity = Session ("MS_Community")
    Set objSNMP = Server.CreateObject("OlePrn.OleSNMP")
    objSNMP.Open strIP, strCommunity, 2, 1000
    ...
 &#39; Determine value to assign to OID; store it in OIDValue.
    ...
    objSNMP.Set ("43.18.1.1.2", OIDValue)
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
<tr class="odd">
<td><p>Header</p></td>
<td>Olesnmp.h</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**ISNMP::Open**](isnmp-open.md)

 

 




