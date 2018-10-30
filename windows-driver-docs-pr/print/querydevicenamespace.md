---
title: QueryDeviceNamespace
author: windows-driver-content
description: The IPrintTicketProvider QueryDeviceNamespace routine provides the default namespace that the PrintTicket-to-DEVMODE and DEVMODE-to-PrintTicket conversions will use if they need to put a feature or option from a private namespace in a Print Ticket.
ms.assetid: 5f940cdc-42c3-4521-91c5-cc8e340ce34a
keywords:
- QueryDeviceNamespace
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# QueryDeviceNamespace


The [**IPrintTicketProvider::QueryDeviceNamespace**](https://msdn.microsoft.com/library/windows/hardware/ff554378) routine provides the default namespace that the PrintTicket-to-DEVMODE and DEVMODE-to-PrintTicket conversions will use if they need to put a feature or option from a private namespace in a Print Ticket.

The following sample code illustrates how this method could be implemented.

```
STDMETHODIMP
CPrintTicketProvider::QueryDeviceNamespace(BSTR *pDefaultNamespace)
{
    *pDefaultNamespace = SysAllocString(TEXT("http://schemas.contoso.com/printers/seriesA/v.1.0"));
    
    if (!(*pDefaultNamespace))
    {
        return E_OUTOFMEMORY;
    }
 
    return S_OK;
}
```

 

 




