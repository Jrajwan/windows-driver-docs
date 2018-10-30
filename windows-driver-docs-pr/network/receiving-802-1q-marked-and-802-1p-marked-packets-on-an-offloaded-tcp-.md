---
title: Receiving Marked Packets on an Offloaded TCP Connection
description: Receiving 802.1Q-Marked and 802.1p-Marked Packets on an Offloaded TCP Connection
ms.assetid: a9bbf43a-016f-4aa9-a5a2-118a8613f03b
keywords:
- 802.1Q and 802.1p information WDK TCP chimney offload , receiving marked packets
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Receiving 802.1Q-Marked and 802.1p-Marked Packets on an Offloaded TCP Connection


\[The TCP chimney offload feature is deprecated and should not be used.\]




When processing a receive packet on an offloaded TCP connection, an offload target uses the 802.1Q information from the packet's 802.3ac header to decide whether the packet should be dropped, as described in the following algorithm:

-   If the neighbor **VlanId** is zero, the offload target does not filter the packet based on the packet's VLAN identifier. In other words, the offload target does not drop the packet because the packet does not have a tag header, because the packet's VLAN identifier is zero, or because the packet's VLAN identifier is nonzero.

-   If the neighbor **VlanId** is nonzero:
    -   If the incoming packet's VLAN identifier matches the neighbor **VlanId**, the offload target accepts the packet.
    -   If the incoming packet does not have a tag header or if the packet's VLAN identifier does not match the neighbor **VlanId**, the offload target drops the packet.

If the offload target accepts the packet and the packet has a nonzero priority value, the offload target can prioritize the delivery of the packet based on this priority value.
