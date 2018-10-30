---
title: Wi-Fi Hotspot Offloading Functions
author: windows-driver-content
description: Wi-Fi Hotspot Offloading Functions
ms.assetid: 114e1604-0d9a-418c-aee1-a9b615d13d21
ms.author: windowsdriverdev
ms.date: 07/31/2017 
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Wi-Fi Hotspot Offloading Functions

[!include[Wi-Fi Hotspot Offloading deprecation](wi-fi-hotspot-offloading-deprecation.md)]


This section describes the Wi-Fi Hotspot Offloading framework functions. These functions facilitate the interaction between the hotspot plug-in and hotspot plug-in host.

The following functions are exported by the plug-in DLL.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[HSPluginGetVersion](hsplugingetversion.md)</p></td>
<td><p>This function verifies that the plug-in and the host versions match.</p></td>
</tr>
<tr class="even">
<td><p>[HSPluginInitPlugin](hsplugininitplugin.md)</p></td>
<td><p>This function is called by the host to initialize the plug-in.</p></td>
</tr>
</tbody>
</table>

 

The hotspot plug-in exposes the following functions through the [HOTSPOT\_PLUGIN\_APIS](hotspot-plugin-apis.md) structure. This structure is passed to the hotspot plug-in host during initialization.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>[HS_PLUGIN_CHECK_FOR_UPDATES](hs-plugin-check-for-updates.md)</p></td>
<td><p>This function checks for configuration updates.</p></td>
</tr>
<tr class="even">
<td><p>[HS_PLUGIN_DEINIT](hs-plugin-deinit.md)</p></td>
<td><p>This function is called to notify the plug-in that it will be unloaded.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_PLUGIN_DISCONNECT_FROM_NETWORK](hs-plugin-disconnect-from-network.md)</p></td>
<td><p>This function is called to notify the plug-in when a device will be disconnected from the network.</p></td>
</tr>
<tr class="even">
<td><p>[HS_PLUGIN_IS_HOTSPOT_NETWORK](hs-plugin-is-hotspot-network.md)</p></td>
<td><p>This function is called by the host to determine if a specified network is a hotspot network.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_PLUGIN_PRE_CONNECT_INIT](hs-plugin-pre-connect-init.md)</p></td>
<td><p>This function is called to notify the plug-in to initialize its state when a connection to a hotspot network is in progress.</p></td>
</tr>
<tr class="even">
<td><p>[HS_PLUGIN_QUERY_CELLULAR_EXCEPTION_HOSTS](hs-plugin-query-cellular-exception-hosts.md)</p></td>
<td><p>This function is called to retrieve the list of hosts that the plug-in will be required to connect to over cellular as part of its authentication process.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_PLUGIN_QUERY_HIDDEN_NETWORK](hs-plugin-query-hidden-network.md)</p></td>
<td><p>This function returns the network identity and network profile for a hidden network</p></td>
</tr>
<tr class="even">
<td><p>[HS_PLUGIN_RESET](hs-plugin-reset.md)</p></td>
<td><p>This function is called to reset the plug-in.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_PLUGIN_SEND_KEEP_ALIVE](hs-plugin-send-keep-alive.md)</p></td>
<td><p>This function sends a network connection keep-alive message.</p></td>
</tr>
<tr class="even">
<td><p>[HS_PLUGIN_START_POST_CONNECT_AUTH](hs-plugin-start-post-connect-auth.md)</p></td>
<td><p>This function is called to perform any post-connect authentication required to authenticate the device over the network.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_PLUGIN_STOP_POST_CONNECT_AUTH](hs-plugin-stop-post-connect-auth.md)</p></td>
<td><p>This function is called to stop the authentication process.</p></td>
</tr>
</tbody>
</table>

 

The hotspot plug-in host exposes the following functions through the [HOTSPOT\_HOST\_HANDLERS](hotspot-host-handlers.md) structure. This structure is passed to the hotspot plug-in during initialization.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[HS_HOST_ALLOCATE_MEMORY](hs-host-allocate-memory.md)</p></td>
<td><p>This function returns an amount of memory specified by the caller.</p></td>
</tr>
<tr class="even">
<td><p>[HS_HOST_FREE_MEMORY](hs-host-free-memory.md)</p></td>
<td><p>This function frees any memory that was allocated by the caller.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_HOST_POST_CONNECT_AUTH_COMPLETION](hs-host-post-connect-auth-completion.md)</p></td>
<td><p>This function indicates the success or failure of an authentication attempt.</p></td>
</tr>
<tr class="even">
<td><p>[HS_HOST_SEND_KEEP_ALIVE_COMPLETION](hs-host-send-keep-alive-completion.md)</p></td>
<td><p>This function indicates the success or failure of a &quot;Send keep-alive&quot; request.</p></td>
</tr>
<tr class="odd">
<td><p>[HS_HOST_UPDATE_CONFIGURATION_COMPLETION](hs-host-update-configuration-completion.md)</p></td>
<td><p>This function indicates the success or failure of a &quot;Check for updates&quot; request.</p></td>
</tr>
</tbody>
</table>

 

## Related topics
[Wi-Fi Hotspot Offloading Reference](wi-fi-hotspot-offloading-reference.md)  



