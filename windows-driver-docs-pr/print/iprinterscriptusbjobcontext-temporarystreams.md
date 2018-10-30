---
title: IPrinterScriptUsbJobContext TemporaryStreams method
author: windows-driver-content
description: Returns an array of IPrinterScriptableSequentialStream interfaces for the persistent data streams that can be used by the IHV JavaScript functions for the current job.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: ED9AFB90-287B-4030-AC20-ECCA9841D27E
keywords: ["TemporaryStreams method Print Devices", "TemporaryStreams method Print Devices , IPrinterScriptUsbJobContext interface", "IPrinterScriptUsbJobContext interface Print Devices , TemporaryStreams method"]
topic_type:
- apiref
api_name:
- IPrinterScriptUsbJobContext.TemporaryStreams
api_type:
- COM
ms.localizationpriority: medium
---

# IPrinterScriptUsbJobContext::TemporaryStreams method


Returns an array of [IPrinterScriptableSequentialStream](https://msdn.microsoft.com/library/windows/hardware/hh439697) interfaces for the persistent data streams that can be used by the IHV JavaScript functions for the current job.

Syntax
------

```ManagedCPlusPlus
HRESULT TemporaryStreams(
  [out, retval] IDispatch **ppArray
);
```

Parameters
----------

*ppArray* \[out, retval\]  
Pointer to an array of [IPrinterScriptableSequentialStream](https://msdn.microsoft.com/library/windows/hardware/hh439697) interfaces.

Return value
------------

This method returns an **HRESULT** value.

Remarks
-------

**TemporaryStreams** is a read-only method. There are a maximum of 2 temporary streams available to the IHV JavaScript functions. These streams are only available for the duration of the current print job. The IHV can use this to store data that is not yet ready to be sent to the print device. On a later **writePrintData** JavaScript function call, these streams can be used to send the stored data to the print device.

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


[**IPrinterScriptUsbJobContext**](iprinterscriptusbjobcontext.md)

[IPrinterScriptableSequentialStream](https://msdn.microsoft.com/library/windows/hardware/hh439697)

 

 




