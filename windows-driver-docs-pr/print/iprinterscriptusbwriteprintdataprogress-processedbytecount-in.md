---
title: IPrinterScriptUsbWritePrintDataProgress ProcessedByteCount method
author: windows-driver-content
description: Sets the number of bytes that the IHV JavaScript function has processed at the time this method was called.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 9E870B80-421B-496A-9510-D97D3A4D7892
keywords: ["ProcessedByteCount method Print Devices", "ProcessedByteCount method Print Devices , IPrinterScriptUsbWritePrintDataProgress interface", "IPrinterScriptUsbWritePrintDataProgress interface Print Devices , ProcessedByteCount method"]
topic_type:
- apiref
api_name:
- IPrinterScriptUsbWritePrintDataProgress.ProcessedByteCount
api_type:
- COM
ms.localizationpriority: medium
---

# <span id="print.iprinterscriptusbwriteprintdataprogress_processedbytecount-in"></span>IPrinterScriptUsbWritePrintDataProgress::ProcessedByteCount method


Sets the number of bytes that the IHV JavaScript function has processed at the time this method was called.

Syntax
------

```ManagedCPlusPlus
HRESULT ProcessedByteCount(
  [in]  UINT32 value
);
```

Parameters
----------

*value* \[in\]  
The number of bytes processed at the time this method was called.

Return value
------------

This method returns an **HRESULT** value.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Minimum supported client</p></td>
<td><p>Windows 8.1</p></td>
</tr>
<tr class="even">
<td><p>Minimum supported server</p></td>
<td><p>Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p>Target platform</p></td>
<td>Desktop</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**IPrinterScriptUsbWritePrintDataProgress**](iprinterscriptusbwriteprintdataprogress.md)

 

 




