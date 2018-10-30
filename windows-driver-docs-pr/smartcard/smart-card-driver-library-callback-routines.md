---
title: Smart Card Driver Library Callback Routines
description: Smart Card Driver Library Callback Routines
ms.assetid: e536d539-4871-4b1d-bb5a-92a310dfa1e7
keywords:
- IOCTLs WDK smart card
- library callback routines WDK smart card
- callback routines WDK smart card
- ReaderFunction
- vendor-supplied drivers WDK smart card , IOCTL request management
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Smart Card Driver Library Callback Routines


## <span id="_ntovr_smart_card_driver_library_callback_routines"></span><span id="_NTOVR_SMART_CARD_DRIVER_LIBRARY_CALLBACK_ROUTINES"></span>


The smart card architecture defines a set of standard callback routine types. For details about these routines, see [Smart Card Driver Callbacks](https://msdn.microsoft.com/library/windows/hardware/ff548982).

A reader driver must make these callback routines available for the driver library routine, [**SmartcardDeviceControl (WDM)**](https://msdn.microsoft.com/library/windows/hardware/ff548939), to call by storing pointers to them in the smart card device extension, which is of type [**SMARTCARD\_EXTENSION**](https://msdn.microsoft.com/library/windows/hardware/ff548974). These pointers are stored in an array that is located in the **ReaderFunction** member of SMARTCARD\_EXTENSION structure. Individual callback routines can be identified by a series of constant values, which should be used as indexes into the **ReaderFunction** array.

For instance, if you want [**SmartcardDeviceControl**](https://msdn.microsoft.com/library/windows/hardware/ff548939) to call a callback routine in your reader driver named **DriverCardPower** whenever it finishes processing an [**IOCTL\_SMARTCARD\_POWER**](https://msdn.microsoft.com/library/windows/hardware/ff548907) request, you must use the [*RDF\_CARD\_POWER*](https://msdn.microsoft.com/library/windows/hardware/ff548919) constant to initialize the device extension in the following manner:

```
SmartcardExtension->ReaderFunction[RDF_CARD_POWER] = 
DriverCardPower;
```

RDF\_CARD\_POWER is a fixed, system-defined constant that always corresponds to the callback routine that services the IOCTL\_SMARTCARD\_POWER request.

If the member of the **ReaderFunction** array that corresponds to the IOCTL being processed is **NULL**, [**SmartcardDeviceControl**](https://msdn.microsoft.com/library/windows/hardware/ff548939) returns a status of STATUS\_NOT\_SUPPORTED to the reader driver. In some cases, this behavior is useful. If, for example, your driver does not support card ejecting or card swallowing, simply assign the appropriate member of the **ReaderFunction** array to be **NULL**, and **SmartcardDeviceControl** will return STATUS\_NOT\_SUPPORTED whenever that member routine is called.

The following table lists the constants that identify the various types of callback routines. These are the constants that you should use as indexes into the **ReaderFunction** array. The table also provides a brief description of each routine type and indicates whether it is mandatory or optional for a reader driver to implement the routine.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Index</th>
<th align="left">Description of corresponding callback routine</th>
<th align="left">Implementation by the reader driver</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>[<em>RDF_CARD_POWER</em>](https://msdn.microsoft.com/library/windows/hardware/ff548919)</p></td>
<td align="left"><p>Resets or turns off an inserted smart card</p></td>
<td align="left"><p>Mandatory</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<em>RDF_CARD_EJECT</em>](https://msdn.microsoft.com/library/windows/hardware/ff548918)</p></td>
<td align="left"><p>Ejects an inserted smart card</p></td>
<td align="left"><p>Optional</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<em>RDF_CARD_TRACKING</em>](https://msdn.microsoft.com/library/windows/hardware/ff548920)</p></td>
<td align="left"><p>Installs an event handler to track card insertions and removals</p></td>
<td align="left"><p>Mandatory</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<em>RDF_IOCTL_VENDOR</em>](https://msdn.microsoft.com/library/windows/hardware/ff548921)</p></td>
<td align="left"><p>Performs vendor-specific IOCTL operations</p></td>
<td align="left"><p>Optional</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<em>RDF_READER_SWALLOW</em>](https://msdn.microsoft.com/library/windows/hardware/ff548922)</p></td>
<td align="left"><p>Does a mechanical swallow</p></td>
<td align="left"><p>Optional</p></td>
</tr>
<tr class="even">
<td align="left"><p>[<em>RDF_SET_PROTOCOL</em>](https://msdn.microsoft.com/library/windows/hardware/ff548923)</p></td>
<td align="left"><p>Selects a transmission protocol for the card that is in the card reader</p></td>
<td align="left"><p>Mandatory</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[<em>RDF_TRANSMIT</em>](https://msdn.microsoft.com/library/windows/hardware/ff548924)</p></td>
<td align="left"><p>Performs data transmissions</p></td>
<td align="left"><p>Mandatory</p></td>
</tr>
</tbody>
</table>

 

When the reader driver calls these routines, it should retrieve the calling parameters from the input buffers, as described in [Smart Card Driver Callbacks](https://msdn.microsoft.com/library/windows/hardware/ff548982). The reader driver should also store the output data in the appropriate buffer areas, as described in the same section.

When any callback routine other than the card-tracking callback routine returns STATUS\_PENDING, the smart card library stops servicing any further calls from the reader driver. (For information about the card-tracking callback routine, see [*RDF\_CARD\_TRACKING*](https://msdn.microsoft.com/library/windows/hardware/ff548920).) If the reader driver attempts to use a driver library routine while the library is in this state, the library routine returns a status of STATUS\_DEVICE\_BUSY. This effectively prevents the reader driver from servicing IOCTL requests from the resource manager, because the reader driver cannot process IOCTL requests if it cannot call [**SmartcardDeviceControl**](https://msdn.microsoft.com/library/windows/hardware/ff548939).

 

 





