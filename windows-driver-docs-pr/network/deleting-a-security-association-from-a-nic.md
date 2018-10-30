---
title: Deleting a Security Association from a NIC
description: Deleting a Security Association from a NIC
ms.assetid: 739a3fef-f0b4-4d7c-9d92-df52fd27915d
keywords:
- security associations WDK IPsec offload
- SAs WDK IPsec offload
- ESP-protected packets WDK IPsec offload , security associations
- AH-protected packets WDK IPsec offload , security associations
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Deleting a Security Association from a NIC

\[The IPsec Task Offload feature is deprecated and should not be used.\]




If necessary, the TCP/IP transport can set [OID\_TCP\_TASK\_IPSEC\_DELETE\_SA](https://msdn.microsoft.com/library/windows/hardware/ff569810) to request that the miniport driver delete a security association (SA) from the NIC.

To create space for another SA on the NIC, the miniport driver can set the **SaDeleteReq** flag in the [**NDIS\_IPSEC\_OFFLOAD\_V1\_NET\_BUFFER\_LIST\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff565801) structure for a receive packet. The TCP/IP transport subsequently issues OID\_TCP\_TASK\_IPSEC\_DELETE\_SA one time to delete the inbound security association (SA) over which the packet was received and another time to delete the outbound SA that corresponds to the deleted inbound SA. A NIC must not remove either of these SAs before it receives the corresponding OID\_TCP\_TASK\_IPSEC\_DELETE\_SA request. The miniport driver can set **SaDeleteReq** independently of the **CryptoDone** flag.
