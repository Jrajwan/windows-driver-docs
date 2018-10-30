---
title: What's new in driver development
description: This section describes new features for driver development in Windows 10.
ms.assetid: 5502AAF9-2400-4338-A646-C746B29F9A44
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# <a name="top"></a>What's new in driver development 


This section provides information about the new features and updates to Windows driver development in Windows 10.

The following is a list of new feature highlights for driver development in Windows 10.

* [Open publishing](#open-publishing)
* [Debugging Tools for Windows](#debugging-tools-for-windows)
* [Driver Verifier](#driver-verifier)
* [Windows Driver Frameworks](#windows-driver-frameworks-wdf)
* [Universal Windows drivers](#universal-windows-drivers)
* [Windows Compatible hardware development boards](#windows-compatible-hardware-development-boards)
* [Power Management Framework](#power-management-framework)
* [System-Supplied Driver Interfaces](#system-supplied-driver-interfaces)
* [WPP Software Tracing](#wpp-software-tracing)


The following table shows the feature updates in Windows 10, by driver technology and version.

| Driver | [version 1803](#whats-new-in-windows-10-version-1803-latest) | [version 1709](#whats-new-in-windows-10-version-1709) | [version 1703](#whats-new-in-windows-10-version-1703) |  [version 1607](#whats-new-in-windows-10-version-1607) |  [version 1507](#whats-new-in-windows-10-version-1507) |
|---|:---:|:---:|:---:|:---:|:--:|
| Audio | [![details](checkmark.png)](#audio-1803)| [![details](checkmark.png)](#audio-1709) | [![details](checkmark.png)](#audio-1703) | [![details](checkmark.png)](#audio)  |![not available](minus.png) |
| ACPI |[![details](checkmark.png)](#acpi-1803) | [![details](checkmark.png)](#acpi-1709) | ![not available](minus.png) |![not available](minus.png) |![not available](minus.png) | ![not available](minus.png) |
| Biometric |![not available](minus.png) |[![details](checkmark.png)](#biometric-1709) | ![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |
| Bluetooth | [![details](checkmark.png)](#bluetooth-1803)|![not available](minus.png) | [![details](checkmark.png)](#bluetooth-1703) | ![not available](minus.png) | [![details](checkmark.png)](#bluetooth) |
| Buses and Ports |![not available](minus.png) |![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#buses-and-ports) |
| Camera | [![details](checkmark.png)](#camera-1803)|![not available](minus.png) | [![details](checkmark.png)](#camera-1703) |[![details](checkmark.png)](#camera-1607) |[![details](checkmark.png)](#camera-1507)|
| Cellular | ![not available](minus.png)|![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) | [![details](checkmark.png)](#cellular)|
| Display | [![details](checkmark.png)](#display-1803)|[![details](checkmark.png)](#display-1709) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#display)|
| Driver security | [![details](checkmark.png)](#security-1803)| ![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#display)|
| Hardware notifications | ![not available](minus.png)|[![details](checkmark.png)](#hardware-notifications-1709) | ![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |
| Human Interface Device (HID)|![not available](minus.png) |![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#human-interface-device)|
| Kernel | [![details](checkmark.png)](#kernel-1803)|[![details](checkmark.png)](#kernel-1709) | [![details](checkmark.png)](#kernel-1703) |![not available](minus.png) |![not available](minus.png) |
| Location | ![not available](minus.png)|![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#location-1607) |[![details](checkmark.png)](#location-1507) |
|Mobile broadband |[![details](checkmark.png)](#mobilebroadband-1803)|[![details](checkmark.png)](#mobilebroadband-1709)|[![details](checkmark.png)](#mobilebroadband-1703)|![not available](minus.png)|![not available](minus.png)|
| Near Field Communication |![not available](minus.png) |![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#near-field-communication)|
| Networking | [![details](checkmark.png)](#networking-1803)|[![details](checkmark.png)](#networking-1709) | [![details](checkmark.png)](#networking-1703)| ![not available](minus.png) |[![details](checkmark.png)](#networking-1507) |
| POS | ![not available](minus.png)|![not available](minus.png) |[![details](checkmark.png)](#pos-1703) | ![not available](minus.png) | ![not available](minus.png) |
| PCI | [![details](checkmark.png)](#pci-1803)|[![details](checkmark.png)](#pci-1709) | ![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |
| Print | ![not available](minus.png)|![not available](minus.png) |![not available](minus.png) |[![details](checkmark.png)](#print-1607) |[![details](checkmark.png)](#print-1507)|
| Pulse Width Modulation | ![not available](minus.png)|[![details](checkmark.png)](#pwm-1709) | ![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |
| Sensors |[![details](checkmark.png)](#sensors-1803)|![not available](minus.png)|![not available](minus.png)|![not available](minus.png)|![not available](minus.png)|
| Smart Card |![not available](minus.png) |![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#smart-card) |
| Storage | ![not available](minus.png)|[![details](checkmark.png)](#storage-1709) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#storage) |
| System-Supplied Driver Interfaces | ![not available](minus.png)|![not available](minus.png) | ![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#system-supplied-driver-interfaces) |
| USB | [![details](checkmark.png)](#usb-1803)|[![details](checkmark.png)](#usb-1709) | [![details](checkmark.png)](#usb-1703) | ![not available](minus.png) |[![details](checkmark.png)](#usb)|
|WI-FI|[![details](checkmark.png)](#wifi-1803)|![not available](minus.png)|![not available](minus.png)|![not available](minus.png)|![not available](minus.png)|
| WLAN | ![not available](minus.png)|![not available](minus.png) | ![not available](minus.png) |[![details](checkmark.png)](#wlan-1607) |[![details](checkmark.png)](#wlan-1507)|

## What's new in driver development for Windows 10

[Back to Top](#top)

This section provides highlights of new features for driver development in Windows 10.

### Open publishing

We're making the docs more community-driven. On many pages of the Windows driver documentation, you can suggest changes directly. Look for the **Contribute** button in the upper right corner of a page. It looks like this:

![screenshot of contribute button](contribute-button.png)

When you click **Contribute**, you'll arrive at the Markdown source file for that topic in a [GitHub repository](https://github.com/MicrosoftDocs/windows-driver-docs). You can click **Edit** and suggest changes right here.

For more details, see [CONTRIBUTING.md](https://github.com/MicrosoftDocs/windows-driver-docs/blob/staging/CONTRIBUTING.md) in the repo. And thanks for taking the time to improve the docs!

### Debugging Tools for Windows

This section describes the changes in the debugging tools for Windows.

**Debugging in Windows 10, version 1803**

[WinDbg Preview Time Travel Debugging (TTD) hands on lab](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/time-travel-debugging-walkthrough) - This lab introduces Time Travel Debugging (TTD), using a small sample program with a code flaw. TTD is used to debug, identify and root cause the issue.

**Debugging in Windows 10, version 1709**

The following is a list of new content sets for the Debugger in Windows 10, version 1709:

* [Debugging Using WinDbg Preview](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugging-using-windbg-preview) - A preview into the next generation debugger.
* [Time Travel Debugging - Overview](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/time-travel-debugging-overview) - Record and replay an execution of your process.

**Debugging in Windows 10, version 1703**

The following table shows changes for the Debugger in Windows 10, version 1703:

| New topics | Updated topics |
| --- | --- |
| [JavaScript Debugger Scripting](https://msdn.microsoft.com/en-us/library/windows/hardware/mt790253(v=vs.85).aspx) | [dtx (Display Type - Extended Debugger Object Model Information)](https://msdn.microsoft.com/en-us/library/windows/hardware/mt790251(v=vs.85).aspx) command |
| 40 undocumented stop codes in the [Bug Check Code Reference](https://msdn.microsoft.com/library/windows/hardware/hh994433) | Updates to the [Configuring tools.ini](https://msdn.microsoft.com/en-us/library/windows/hardware/ff539232(v=vs.85).aspx) topic with additional options in the tools.ini file for the command line debuggers |
| [!ioctldecode command](https://msdn.microsoft.com/en-us/library/windows/hardware/mt790255(v=vs.85).aspx) | New command capabilities in the [dx (Display Debugger Object Model Extension)](https://msdn.microsoft.com/library/windows/hardware/dn936815) command |

**Debugging in Windows 10, version 1607**

In Windows 10, version 1607, changes to the Debugger include a new topic about [Debugging a UWP app using WinDbg](https://msdn.microsoft.com/library/windows/hardware/mt757092), and updates to the 30 most-viewed developer bug check topics in [Bug Check Code Reference](https://msdn.microsoft.com/library/windows/hardware/hh994433).

**Debugging in Windows 10, version 1507**

The following is a list of new commands for the Windows Debugger in Windows 10, version 1507:

* [**dx (Display NatVis Expression)**](https://msdn.microsoft.com/library/windows/hardware/dn936815) - A new debugger command which displays object information using the NatVis extension model.
* [**.settings**](https://msdn.microsoft.com/library/windows/hardware/dn925473) - A new command that sets, modifies, displays, loads and saves settings in the Debugger.Settings namespace.

### Driver Verifier

Driver verifier includes new driver validation rules for the following technologies:

-   New [Rules for Audio Drivers](https://msdn.microsoft.com/library/windows/hardware/dn906757)
-   New [Rules for AVStream Drivers](https://msdn.microsoft.com/library/windows/hardware/dn906758)
-   Four new [Rules for KMDF Drivers](https://msdn.microsoft.com/library/windows/hardware/ff551709)
-   Three new [Rules for NDIS Drivers](https://msdn.microsoft.com/library/windows/hardware/ff551713)
-   New [Nullcheck rules](https://msdn.microsoft.com/en-us/library/windows/hardware/mt779099(v=vs.85).aspx) *Added in version 1703*

### Windows Driver Frameworks (WDF)

**WDF in Windows 10, version 1803**

In Windows 10, version 1803, the Windows Driver Framework (WDF) includes Kernel-Mode Driver Framework (KMDF) version 1.25 and User-Mode Driver Framework version 2.25. For info on what's included in these framework versions, see [What's New for WDF Drivers in Windows 10](wdf/index.md).

To see what was added in previous versions of WDF, see [KMDF Version History](wdf/kmdf-version-history.md) and [UMDF Version History](wdf/umdf-version-history.md).

The following topics are new for WDF:

* [Building a WDF driver for multiple versions of Windows](wdf/building-a-wdf-driver-for-multiple-versions-of-windows.md)
* [**WdfDeviceRetrieveDeviceDirectoryString**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdfdevice/nf-wdfdevice-wdfdeviceretrievedevicedirectorystring)

### Universal Windows drivers

This section describes new and updated features for Universal Windows drivers in Windows 10.

**Universal Drivers in Windows 10, version 1803**

See the latest recommendations for universal drivers in [Getting started with universal drivers](develop/getting-started-with-universal-drivers.md).

**Universal Drivers in Windows 10, version 1709**

The following is a list of new features to Universal Drivers in Windows 10, version 1709:

* [Updating Device Firmware using Windows Update](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/updating-device-firmware-using-windows-update) - Describes how to update a removable or in-chassis device's firmware by using the Windows Update (WU) service.
* [Reg2inf](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/reg2inf) - The Driver Package INF Registry Conversion Tool (reg2inf.exe) converts a registry key and its values or a COM .dll implementing a DLL RegisterServer routine, into a set of INF AddReg directives. These directives are included in the driver package INF file.

The following is a list of updates to Universal Drivers in Windows 10, version 1709:

* The [Universal Drivers Scenario](https://docs.microsoft.com/en-us/windows-hardware/drivers/develop/universal-driver-scenarios) has a new COM component example
* [INF AddComponent Directive](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/inf-addcomponent-directive)
* [Using an Extension INF file](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/using-an-extension-inf-file)
* [Using a Component INF file](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/using-a-component-inf-file)

**Universal Drivers in Windows 10**

Starting in Windows 10, you can write a single driver that works on OneCoreUAP-based editions of Windows, such as Windows 10 for desktop editions (Home, Pro, Enterprise, and Education), Windows 10 Mobile, and Windows 10 IoT Core (IoT Core). Such a driver is called a Universal Windows driver. A Universal Windows driver calls a subset of the interfaces that are available to a Windows driver. For information about how to build, install, deploy, and debug a Universal Windows driver for Windows 10, see [Getting Started with Universal Windows drivers](https://msdn.microsoft.com/windows-drivers/develop/getting_started_with_universal_drivers).

When you build a Universal Windows driver using Microsoft Visual Studio 2015, Visual Studio automatically checks if the APIs that your driver calls are valid for a Universal Windows driver. You can also use the ApiValidator.exe as a standalone tool to perform this task. The ApiValidator.exe tool is part of the Windows Driver Kit (WDK) for Windows 10. For info, see [Validating Universal Windows drivers](https://msdn.microsoft.com/windows-drivers/develop/validating_universal_drivers).

Universal Windows drivers also require a special kind of INF file called a *universal INF*. A universal INF can use a subset of the directives and sections available to a legacy INF file. To learn more, see [Using a Universal INF File](https://msdn.microsoft.com/library/windows/hardware/dn941087). To see which sections and directives apply, see [INF File Sections and Directives](https://msdn.microsoft.com/library/windows/hardware/ff547433).

When you're ready, use the [InfVerif](https://msdn.microsoft.com/library/windows/hardware/dn929319) tool to test your driver's INF file. In addition to reporting INF syntax problems, the tool reports if the INF file will work with a Universal Windows driver.

You can also find information about which APIs you can call from a Universal Windows driver. This information is located in the Requirements block at the bottom of driver reference pages.

For example, you'll see a listing similar to this one that tells you if a given DDI is **Universal.**

![target platform set to universal in requirements block](targetplatform.png)

For more info, see [Target platform on driver reference pages](https://msdn.microsoft.com/windows-drivers/develop/windows_10_editions_for_universal_drivers).

### Windows compatible hardware development boards

Windows is now supported on more affordable boards such as the Raspberry Pi 2. Become a part of our early adopter community and load Windows on that board. For more information, see [Windows compatible hardware development boards](https://msdn.microsoft.com/library/windows/hardware/dn914597).

### <a name="power-management-framework"></a>Power Management Framework (PoFx)

The power management framework (PoFx) enables a driver to define one or more sets of individually adjustable performance states for individual components within a device. The driver can use performance states to throttle a component's workload to provide just enough performance for its current needs. For more information, see [Component-Level Performance State Management](https://msdn.microsoft.com/library/windows/hardware/dn939352).

### WPP Software Tracing

[WPP Software Tracing](https://msdn.microsoft.com/library/windows/hardware/ff556204) introduces a new feature: *Inflight Trace Recorder*. If the driver enables WPP tracing and WPP Recorder, trace logging is turned on automatically and you can easily view messages without starting or stopping trace sessions. For more fine tuned control over the log, WPP Recorder allows a KMDF driver to create and manage custom buffers.

-   [WPP Recorder for logging traces](https://msdn.microsoft.com/library/windows/hardware/dn914610)
-   [WppRecorderLogGetDefault](https://msdn.microsoft.com/library/windows/hardware/dn895240)
-   [WppRecorderLogCreate](https://msdn.microsoft.com/library/windows/hardware/dn914615) (KMDF only)
-   [WppRecorderDumpLiveDriverData](https://msdn.microsoft.com/library/windows/hardware/dn914612)


## What's new in Windows 10, version 1803 (latest)

This section describes new features and updates for driver development in Windows 10, version 1803 (Windows 10 April 2018 Update).

### <a name="acpi-1803"></a>ACPI

Windows 10, version 1803 includes updates to ACPI DDIs to support platform capabilities and physical device location.

### <a name="audio-1803"></a>Audio

The [voice activation](https://docs.microsoft.com/en-us/windows-hardware/drivers/audio/voice-activation) topic was updated to include additional information on APO requirements.

### <a name="bluetooth-1803"></a>Bluetooth

Windows 10, version 1803 introduces support for Swift Pair. Users no longer need to navigate the Settings App and find their peripheral to pair. Windows can now do this for them by popping a notification when a new peripheral is nearby and ready. There are two sets of requirements to ensure your peripheral works with Swift Pair. One set is for the peripheral’s behavior, and another for the structure and values in a Microsoft defined vendor advertisement section. For more information, see:

* [Bluetooth Swift Pair](https://docs.microsoft.com/en-us/windows-hardware/design/component-guidelines/bluetooth-swift-pair)
* [Bluetooth Features and Recommendations](https://docs.microsoft.com/en-us/windows-hardware/design/component-guidelines/bluetooth)

Windows 10, version 1803 supports Bluetooth version 5.0. For information about profile support, see [Bluetooth Version and Profile Support in Windows 10](https://docs.microsoft.com/en-us/windows-hardware/drivers/bluetooth/general-bluetooth-support-in-windows).

### <a name="camera-1803"></a>Camera

Updates to Camera driver development include:

* [DShow (DirectShow) Bridge implementation guidance for UVC devices](https://docs.microsoft.com/en-us/windows-hardware/drivers/stream/dshow-bridge-implementation-guidance-for-usb-video-class-devices) - Implementation guidance for configuring DShow Bridge for cameras and devices that comply with the USB Video Class (UVC) specification. The platform uses Microsoft OS Descriptors from the USB bus standard to configure DShow Bridge. The Extended Properties OS Descriptors are an extension of USB standard descriptors and are used by USB devices to return Windows specific device properties that are not enabled through standard specifications.
* [360 camera video capture](https://docs.microsoft.com/en-us/windows-hardware/drivers/stream/360-camera-video-capture) - Provides support for 360 camera preview, capture, and record with existing MediaCapture APIs. This enables the platform to expose spherical frame sources (for example, equirectangular frames ), enabling apps to detect and handle 360 video camera streams as well as to provide a 360 capture experience.

### <a name="display-1803"></a>Display

The following are updates to Display driver development in Windows 10, version 1803:

* **Indirect Display UMDF class extension** - The Indirect Display driver can pass the SRM to the rendering GPU and have a mechanism to query the SRM version being used.

* **IOMMU hardware-based GPU isolation support** - Increases security by restricting GPU access to system memory.

* **GPU paravirtualization support** - Enables display drivers to provide rendering capabilities to Hyper-V virtualized environments.

* **Brightness** - A new brightness interface to support multiple displays that can be set to calibrated nit-based brightness levels.

* **D3D11 bitstream encryption** - Additional GUIDS and parameters to D3D11 to support exposing CENC, CENS, CBC1, and CBCS with 8 or 16 byte initialization vectors.

* **D3D11 and D3D12 video decode histogram** - A luminance histogram allows the media team to leverage fixed function hardware for histogram to improve tone mapping quality for HDR/EDR scenarios. Fixed function hardware is useful when GPU is already saturated in these scenarios and to enable parallel processing. This feature is optional and should only be implemented if fixed function hardware is available. This feature should not be implemented with 3D or Compute.

* **D3D12 video decode** now supports Decode Tier II, indicating driver supports *Array of Textures* that enable applications to amortize allocation cost and reduce peak memory usage during resolution change.

* **Tiled resource tier and LDA atomics** - A new cross node sharing tier to add support for atomic shader instructions working across linked adapter (LDA) nodes. This improves ISVs ability to implement multiple GPU rendering techniques like split frame rendering (SFR) and clearly advances the capabilities over what is possible in D3D11.

* **GPU dithering support** - Drivers can report the ability to performing dithering on the wire signal for a given timing mode. This allows the OS to explicitly request dithering in scenarios where a higher effective bit depth is needed than is physically available on the monitor link, for example for HDR10 over HDMI 2.0.

* **Post-processing color enhancement override** - Adds the ability for the OS to request that the driver temporarily disable any post-processing that enhances or alters display colors. This is to support scenarios where specific applications want to enforce colorimetrically accurate color behavior on the display, and safely coexist with OEM or IHV-proprietary display color enhancements.

* **Direct3D12 and Video** - New API and DDI to provide access to the following capabilities:
	* Hardware accelerated video decoding
	* Content Protection
	* Video processing

* **DisplayID** - A new DDI, designed to allow the VESA’s DisplayID descriptor to be queried from a display controlled by a graphics adapter and shall support DisplayID v1.3 and DisplayID v2.0. The DDI is an extension of existing DxgkDdiQueryAdapterInfo DDI and shall be supported by all drivers with DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM2_3, including kernel mode display only drivers and indirect display drivers.

* **GPU performance data** - Extensions to DdiQueryAdapterInfo will expose information such as temperature, fan speed, clock speeds for engines and memory, memory bandwidth, power draw, and voltages

* Miscellaneous - A new SupportContextlessPresent driver cap to help IHV onboard new driver.

* Improvements to External/Removable GPU support in the OS. As a first step to add better support, Dxgkrnl needs to determine if a GPU is “detachable”, i.e. hot-pluggable. For RS4 we would like to leverage the driver’s knowledge about this instead of building our own infrastructure. For this purpose, we are adding a “Detachable” bit to DXGK_ DRIVERCAPS struct. Driver will set this bit during adapter initialization if the adapter is hot-pluggable.

* **Display Diagnostics** - Kernel mode device driver interface (DDI) changes to allow the driver for a display controller to report diagnostic events to the OS.  This provides a channel through which the driver can log events which would otherwise be invisible to the OS as the events are not a response to an OS request or something the OS needs to react to.

* **Shared graphics power components** - Allows non-graphics drivers to participate in the power management of a graphics device.  A non-graphics driver will use a driver interface to manage one or more of these shared power components in coordination with the graphics driver.

* **Shared texture improvements** - Includes increasing the types of textures that can be shared across processes and D3D devices. This design enables the frame server OS component to support monochrome with minimal memory copying.

### <a name="security-1803"></a>Driver security

Updates to [Windows Driver Security Guidance](https://docs.microsoft.com/en-us/windows-hardware/drivers/driversecurity/)
and the [Driver security checklist](https://docs.microsoft.com/en-us/windows-hardware/drivers/driversecurity/driver-security-checklist), which provides a driver security checklist for driver developers.

### <a name="kernel-1803"></a>Windows kernel

This section describes the new and updates features for Windows kernel driver development in Windows 10, version 1803.

A set of new APIs have been added to the kit to enable third parties to create their own KDNET extensibility modules or KdSerial transport layers. For sample code, see “Kernel Transport Samples” (ddk\samples\kdserial and ddk\samples\kdnet) in the Debuggers folder.

Support was added to provide drivers with a sanctioned location (that the operating system knows about) where they can store file state.  With this approach, the system can associate files in that location with a device or driver.

There are distinct locations to store file states specific to the internals of a driver and specific to a device. For drivers that have file state, you can decide if the state written to disk is:

* Driver state ([IoGetDriverDirectory](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iogetdriverdirectory)): global to the driver that might be controlling multiple devices), or

* Device state ([IoGetDeviceDirectory](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iogetdevicedirectory)): specific to the driver-controlled single device and other devices might have different values for similar state.

Function drivers (FDO) can now negotiate additional power when their respective PCIe devices are in a D3Cold state. This includes:

* Auxiliary power requirement [D3COLD_REQUEST_AUX_POWER](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/wdm/nc-wdm-d3cold_request_aux_power).
* Core power rail [D3COLD_REQUEST_CORE_POWER_RAIL](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/wdm/nc-wdm-d3cold_request_core_power_rail).
* Requirement for a fixed delay time between the message is received at the PCI Express Downstream Port and the time the platform asserts PERST# to the slot during the corresponding endpoint’s or PCI Express Upstream Port’s transition to D3cold while the system is in an ACPI operational state. See [D3COLD_REQUEST_PERST_DELAY](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/wdm/nc-wdm-d3cold_request_perst_delay).

NT services and kernel-mode and user-mode drivers can raise a custom trigger for a device by using the [RtlRaiseCustomSystemEventTrigger](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-rtlraisecustomsystemeventtrigger) function. A custom trigger, owned by the driver developer, notifies system event broker to start an associated background task with it, which is identified by a custom trigger identifier.

You can now register for active session change notification and get a callback when the notification is fired. As part of this notification, some data is also shared with the caller. This associated data is delivered via the [PO_SPR_ACTIVE_SESSION_DATA structure](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/ntpoapi/ns-ntpoapi-_po_spr_active_session_data).

### <a name="networking-1803"></a>Networking

This section outlines new features and improvements for Windows Networking driver development in Windows 10, version 1803.

**NDIS and NetAdapterCx**

Updates to NDIS include:

* [Receive side scaling V2](https://docs.microsoft.com/windows-hardware/drivers/network/receive-side-scaling-version-2-rssv2-in-ndis-6-80) has been updated with further details about steering parameters
* The [Synchronous OID interface](https://docs.microsoft.com/windows-hardware/drivers/network/synchronous-oid-request-interface-in-ndis-6-80) now supports NDIS light weight filter drivers

The following topics are new for the Network Adapter WDF class extension (NetAdapterCx):

* [Introduction to NetAdapterCx 1.2](https://docs.microsoft.com/windows-hardware/drivers/netcx/introduction-to-netadaptercx-1-2)
* [Packet descriptors and extensions](https://docs.microsoft.com/windows-hardware/drivers/netcx/packet-descriptors-and-extensions)
* [Network data buffer management](https://docs.microsoft.com/windows-hardware/drivers/netcx/network-data-buffer-management)
* [NetAdapterCx receive side scaling (RSS)](https://docs.microsoft.com/windows-hardware/drivers/netcx/netadaptercx-receive-side-scaling-rss-)

Additionally, new topics are available for a preview-only feature, the Mobile Broadband class extension (MBBCx), which uses the NetAdapterCx model for mobile broadband connectivity.

* [Mobile Broadband Class Extension (MBBCx)](https://docs.microsoft.com/windows-hardware/drivers/netcx/mobile-broadband-mbb-wdf-class-extension-mbbcx-)
    * [Writing an MBBCx client driver](https://docs.microsoft.com/windows-hardware/drivers/netcx/writing-an-mbbcx-client-driver)
    * [MBBCx API reference](https://docs.microsoft.com/windows-hardware/drivers/netcx/mbbcx-api-reference)

### <a name="mobilebroadband-1803"></a>Mobile broadband

In mobile broadband, a new topic detailing [MB low level UICC access](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-low-level-uicc-access) is available.

### Mobile operators

New Hotspot and AppID settings are now a part of [desktop COSA](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/desktop-cosa-apn-database-settings#desktop-cosa-only-settings). Mobile operators are strongly encouraged to transition from broadband app experience apps with [Sysdev metadata packages](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/service-metadata) to [MO UWP Apps](https://docs.microsoft.com/windows-hardware/drivers/mobilebroadband/uwp-mobile-broadband-apps) and the [COSA database](https://docs.microsoft.com/windows-hardware/drivers/mobilebroadband/desktop-cosa-apn-database-settings).

### <a name="pci-1803"></a>PCIe

New ACPI _DSD methods have been added to support these Modern Standby and PCI hot plug scenarios:

* Directed Deepest Runtime Idle Power State (DDRIPS) support on PCIe Root Ports
* Identifying PCIe Root Ports supporting hot plug in D3
* Identifying externally exposed PCIe Root Ports

For information, see [ACPI Interface: Device Specific Data (_DSD) for PCIe Root Ports](https://docs.microsoft.com/en-us/windows-hardware/drivers/pci/dsd-for-pcie-root-ports).

### <a name="sensors-1803"></a>Sensors

The [SENSOR_CONNECTION_TYPES enumeration](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/sensorsdef/ne-sensorsdef-sensor_connection_types) was added to clarify connection type properties.

### <a name="usb-1803"></a>USB

New APIs were added to simulate detach for shared connectors. If a USB device is attached to a host or have shared connector while the stack is being removed while the device is attached to a host or have shared connectors, you can simulate a detach event. At this point all attach/detach notification mechanisms are disabled. For more information, see [UfxDeviceNotifyFinalExit function](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/ufxclient/nf-ufxclient-ufxdevicenotifyfinalexit).

### <a name="wifi-1803"></a>Wi-fi

Updates to Wi-fi driver development include a new [TLV for the Nic Auto Power Saver (NAPS) advanced power management feature](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/wdi-tlv-os-power-management-features) and updates to the platform level device recovery service (PLDR).


## What's new in Windows 10, version 1709

This section describes new features and updates for driver development in Windows 10, version 1709.

[Back to Top](#top)

### <a name="audio-1709"></a>Audio

The following is a list of updates to Windows Audio driver development in Windows 10, version 1709:

* New [Configure and query audio device modules](https://docs.microsoft.com/windows-hardware/drivers/audio/configure-and-query-audiodevicemodules)
* Extensive updates to [voice activation](https://docs.microsoft.com/en-us/windows-hardware/drivers/audio/voice-activation)
    * More details on chained and keyword only activation
    * A new glossary of terms
    * Additional information on training and recognition, such as pin and audio format information
    * An updated keyword system overview
    * Updated information on wake on voice

### <a name="acpi-1709"></a>ACPI

The following is a list of new Advanced Configuration and Power Interface (ACPI) DDIs to support input/output buffers.

* [ACPI_EVAL_INPUT_BUFFER_COMPLEX_V1](https://msdn.microsoft.com/en-us/library/mt826375)
* [ACPI_EVAL_INPUT_BUFFER_COMPLEX_V1_EX](https://msdn.microsoft.com/en-us/library/mt826376)
* [ACPI_EVAL_INPUT_BUFFER_COMPLEX_V2](https://msdn.microsoft.com/en-us/library/mt826377)
* [ACPI_EVAL_INPUT_BUFFER_COMPLEX_V2_EX](https://msdn.microsoft.com/en-us/library/mt826378)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_INTEGER_V1](https://msdn.microsoft.com/en-us/library/mt826379)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_INTEGER_V2](https://msdn.microsoft.com/en-us/library/mt826381)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_INTEGER_V2_EX](https://msdn.microsoft.com/en-us/library/mt826382)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_V1](https://msdn.microsoft.com/en-us/library/mt826383)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_V1_EX](https://msdn.microsoft.com/en-us/library/mt826384)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_V2](https://msdn.microsoft.com/en-us/library/mt826385)
* [ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_V2_EX](https://msdn.microsoft.com/en-us/library/mt826386)
* [ACPI_EVAL_INPUT_BUFFER_V1](https://msdn.microsoft.com/en-us/library/mt826387)
* [ACPI_EVAL_INPUT_BUFFER_V1_EX](https://msdn.microsoft.com/en-us/library/mt826388)
* [ACPI_EVAL_INPUT_BUFFER_V2](https://msdn.microsoft.com/en-us/library/mt826389)
* [ACPI_EVAL_INPUT_BUFFER_V2_EX](https://msdn.microsoft.com/en-us/library/mt826390)
* [ACPI_EVAL_OUTPUT_BUFFER_V1](https://msdn.microsoft.com/en-us/library/mt826391)
* [ACPI_EVAL_OUTPUT_BUFFER_V2](https://msdn.microsoft.com/en-us/library/mt826392)
* [ACPI_METHOD_ARGUMENT_V1](https://msdn.microsoft.com/en-us/library/mt826393)
* [ACPI_METHOD_ARGUMENT_V2 ](https://msdn.microsoft.com/en-us/library/mt826394)
* [GIC_ITS](https://msdn.microsoft.com/en-us/library/mt826395)


### <a name="biometric-1709"></a>Biometric

There are new signing requirements for Windows Biometric Drivers. For more information, see [Signing WBDI Drivers](https://docs.microsoft.com/en-us/windows-hardware/drivers/biometric/signing-wbdi-drivers).

### <a name="display-1709"></a>Display

The following is a list of new features for Windows Display driver development in Windows 10, version 1709.

* Display ColorSpace Transform DDIs provide additional control over color space transforms applied in the post-composition display pipeline.
* The D3D12 Copy Queue Timestamp Queries feature will allow applications to issue timestamp queries on COPY command lists/queues. These timestamps are specified to function identically to timestamps on other engines.
* Enhanced Video integration into Direct3D12 Runtime through:
    1. Hardware accelerated video decoding
    2. Content protection
    3. Video processing

### <a name="hardware-notifications-1709"></a>Hardware notifications

In Windows 10, version 1709, there is support for hardware-agnostic support of notification components such as LEDs and vibration mechanisms. For more information, see:

* [Hardware notifications support](https://docs.microsoft.com/en-us/windows-hardware/drivers/gpiobtn/hardware-notifications-support)
* [Hardware notifications reference](https://msdn.microsoft.com/en-us/library/windows/hardware/dn789336)


### <a name="kernel-1709"></a>Windows kernel

In Windows 10, version 1709, several new routines to the Windows Kernel for drivers have been added.

* ExGetFirmwareType and ExIsSoftBoot &ndash; Executive library support routines.
* [PsSetLoadImageNotifyRoutineEx](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826267(v=vs.85).aspx) &ndash; An extended image notify routine for all executable images, including images that have a different architecture from the native architecture of the operating system.
* [MmMapMdl](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843504(v=vs.85).aspx) &ndash; A [memory manager](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/ff565757(v=vs.85).aspx) routine for mapping physical pages described by a memory descriptor list (MDL) into the system virtual address space.
* [PoFxSetTargetDripsDevicePowerState ](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826261(v=vs.85).aspx) &ndash; A PoFx routine to notify the power manager of the device's target device power state for DRIPS.
* The following is a list of new options for the [ZwSetInformationThread](https://msdn.microsoft.com/library/windows/hardware/ff567101) routine, that are related to process policies:

    * [PROCESS_MITIGATION_CHILD_PROCESS_POLICY](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843940(v=vs.85).aspx)
    * [PROCESS_MITIGATION_PAYLOAD_RESTRICTION_POLICY](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843941(v=vs.85).aspx)
    * [PROCESS_READWRITEVM_LOGGING_INFORMATION](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826264(v=vs.85).aspx)

* [PsGetServerSiloActiveConsoleId](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-psgetserversiloactiveconsoleid) and [PsGetParentSilo](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826265(v=vs.85).aspx) &ndash; New Silo APIs to get information about server silos that are created and destroyed on a machine.
* The following is a list of new RTL functions for using correlation vector to reference events and the generated logs for diagnostic purposes.
    * [CORRELATION_VECTOR](https://msdn.microsoft.com/En-US/Library/Windows/Hardware/mt826258)
    * [RtlExtendCorrelationVector](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826269(v=vs.85).aspx)
    * [RtlIncrementCorrelationVector](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826270(v=vs.85).aspx)
    * [RtlInitializeCorrelationVector](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826273(v=vs.85).aspx)
    * [RtlValidateCorrelationVector](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826274(v=vs.85).aspx)

### <a name="mobilebroadband-1709"></a>Mobile broadband

The following is a list of new features for Windows Mobile Broadband and Mobile Operator Scenarios for driver development in Windows 10, version 1709:

* [UICC reset](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-uicc-reset-operations) and [modem reset](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-modem-reset-operations)
* [Protocol Configuration Operations (PCO)](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-protocol-configuration-operations--pco-)
* [Base stations information query](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-base-stations-information-query-support)
* [eSIM and MBIM ReadyState guidance](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/mb-esim-mbim-ready-state-guidance)


In Windows 10, version 1709, the [desktop COSA documentation](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/planning-your-desktop-cosa-apn-database-submission) was updated to include new branding-related fields.
See the list of [deprecated features](#deprecated-features) for other changes to Mobile Operator Scenarios.

### <a name="networking-1709"></a>Networking

This section outlines new features and improvements for Windows Networking driver development in Windows 10, version 1709.

The following is a list of new and updated features for NDIS:

* [Introduction to NetAdapterCx 1.1](https://docs.microsoft.com/en-us/windows-hardware/drivers/netcx/introduction-to-netadaptercx-1-1), which includes new NewAdapterCx features:
    * More packet context options
    * Finer link state control
    * Improved receive buffer management and performance
    * General performance improvements
* New [Synchronous OID request interface](https://docs.microsoft.com/windows-hardware/drivers/network/synchronous-oid-request-interface-in-ndis-6-80) in NDIS 6.80
* New [Receive Side Scaling Version 2 (RSSv2)](https://docs.microsoft.com/windows-hardware/drivers/network/receive-side-scaling-version-2-rssv2-in-ndis-6-80) in NDIS 6.80
* [Introduction to NDIS 6.80](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/introduction-to-ndis-6-80)
* [Porting NDIS 6.x drivers to NDIS 6.80](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/porting-ndis-6-x-drivers-to-ndis-6-80)


### <a name="pci-1709"></a>Virtualized PCI

There are new programming interfaces for writing a Physical Function driver for devices that conform to the PCI Express Single-Root I/O Virtualization (SR-IOV) specification. The interfaces are declared in Pcivirt.h. For more information, see [PCI virtualization](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt825211(v=vs.85).aspx).

### <a name="pwm-1709"></a>Pulse Width Modulation (PWM) Controllers

In Windows 10, version 1709, to provide access to a Pulse width modulation (PWM) controller that is part of the SoC and memory-mapped to the SoC address space, you need to write a kernel-mode driver. For more information, see [PWM driver for an on-SoC PWM module](https://docs.microsoft.com/en-us/windows-hardware/drivers/spb/pulse-width-controller%20driver?branch=spb).

To parse and validate pin paths and extract the pin number, kernel model drivers should use [PwmParsePinPath](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt826268(v=vs.85).aspx).

An app can send requests to the controller driver by sending [PWM IOCTLs](https://docs.microsoft.com/windows-hardware/drivers/spb/pulse-width-controller%20driver#pwm-ioctl-requests) requests.


### <a name="storage-1709"></a>Storage and File Systems

In File Systems and Storage, the ufs.h header was added in Windows 10, version 1709 to provide additional support to Universal Flash Storage.

Posix updates include new functions **delete** and **rename**.

The following is a list of headers that were updated in Windows 10, version 1709:

* ata.h
* fltKernel.h
* minitape.h
* ntddscsi.h
* ntddstor.h
* ntddvol.h
* ntifs.h
* scsi.h
* storport.h

### <a name="usb-1709"></a>USB

This section describes the new features for USB in Windows 10, version 1709.

#### Media Agnostic USB (MA-USB) protocol

The USB driver stack can send USB packets over non-USB physical mediums such as Wi-Fi by using the Media Agnostic USB (MA-USB) protocol. To implement this feature, new programming interfaces have been released. The new DDIs allow the driver to determine the delays associated with the [_URB_GET_ISOCH_PIPE_TRANSFER_PATH_DELAYS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842846(v=vs.85).aspx). That information can be retrieved by building a new URB request.
For information about this new feature, see the following topics:

* [USB client drivers for Media-Agnostic (MA-USB)](https://docs.microsoft.com/en-us/windows-hardware/drivers/usbcon/usb-client-drivers-for-ma-usb)
* [_URB_GET_ISOCH_PIPE_TRANSFER_PATH_DELAYS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842846(v=vs.85).aspx)
* [USB Request Blocks (URBs)](https://docs.microsoft.com/en-us/windows-hardware/drivers/usbcon/communicating-with-a-usb-device)

To support MA-USB, the host controller driver must provide the transport characteristics by implementing specific callback functions. The following table shows the callback functions and structures that support MA-USB.

| Callback Functions | Structures |
| ----- | ----- |
| [EVT_UCX_USBDEVICE_GET_CHARACTERISTIC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt812916(v=vs.85).aspx) | [UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827318(v=vs.85).aspx) |
| [EVT_UCX_USBDEVICE_RESUME](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt812917(v=vs.85).aspx) | [UCX_CONTROLLER_ENDPOINT_CHARACTERISTIC_PRIORITY](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827316(v=vs.85).aspx) |
| [EVT_UCX_USBDEVICE_SUSPEND](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt812918(v=vs.85).aspx) | [UCX_ENDPOINT_CHARACTERISTIC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827315(v=vs.85).aspx) |
| [EVT_UCX_ENDPOINT_GET_ISOCH_TRANSFER_PATH_DELAYS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827309(v=vs.85).aspx) | [UCX_ENDPOINT_CHARACTERISTIC_TYPE](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827317(v=vs.85).aspx) |
| [EVT_UCX_ENDPOINT_SET_CHARACTERISTIC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827310(v=vs.85).aspx) | [UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827318(v=vs.85).aspx) |

#### Synchronized system QPC with USB frame and microframes

There are new programming interfaces that retrieve the system query performance counter (QPC) value synchronized with the frame and microframe.

This information is retrieved only when the caller enables the feature in the host controller. To enable the feature, a host controller driver must implement the following callback functions.

* [EVT_UCX_CONTROLLER_GET_FRAME_NUMBER_AND_QPC_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827304(v=vs.85).aspx)
* [EVT_UCX_CONTROLLER_START_TRACKING_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827307(v=vs.85).aspx)
* [EVT_UCX_CONTROLLER_STOP_TRACKING_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt827308(v=vs.85).aspx)

An application can use these APIs to enable/disable the feature and retrieve the information:

* [WinUsb_GetCurrentFrameNumberAndQpc](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842805(v=vs.85).aspx)
* [WinUsb_StartTrackingForTimeSync](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842806(v=vs.85).aspx)
* [WinUsb_StopTrackingForTimeSync](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842807(v=vs.85).aspx)

Other drivers can send these IOCTL requests to enable/disable the feature and retrieve the information:

* [IOCTL_USB_GET_FRAME_NUMBER_AND_QPC_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842808(v=vs.85).aspx)
* [IOCTL_USB_START_TRACKING_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842800(v=vs.85).aspx)
* [IOCTL_USB_STOP_TRACKING_FOR_TIME_SYNC](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842809(v=vs.85).aspx)

Here are the supporting structures for synchronized system OPC with USB frame and microframes:

* [USB_START_TRACKING_FOR_TIME_SYNC_INFORMATION](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842803(v=vs.85).aspx)
* [USB_STOP_TRACKING_FOR_TIME_SYNC_INFORMATION](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842804(v=vs.85).aspx)
* [USB_FRAME_NUMBER_AND_QPC_FOR_TIME_SYNC_INFORMATION](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt842802(v=vs.85).aspx)

**IOCTL_UCMTCPCI_PORT_CONTROLLER_DISPLAYPORT_DISPLAY_OUT_STATUS_CHANGED**

The [IOCTL_UCMTCPCI_PORT_CONTROLLER_DISPLAYPORT_DISPLAY_OUT_STATUS_CHANGED](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843562(v=vs.85).aspx) request is a new request in USB Type-C Port Controller Interface framework extension. This request notifies the client driver that the display out status of the DisplayPort connection has changed.

Here are the structures that support the IOCTL_UCMTCPCI_PORT_CONTROLLER_DISPLAYPORT_DISPLAY_OUT_STATUS_CHANGED request:

* [UCMTCPCI_PORT_CONTROLLER_DISPLAYPORT_DISPLAY_OUT_STATUS_CHANGED_IN_PARAMS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843564(v=vs.85).aspx)
* [UCMTCPCI_PORT_CONTROLLER_DISPLAYPORT_DISPLAY_OUT_STATUS](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/mt843563(v=vs.85).aspx)


## What's new in Windows 10, version 1703

This section describes new and improved features for driver development in Windows 10, version 1703.

[Back to Top](#top)


### <a name="audio-1703"></a>Audio

The following is a list of new topics for Audio driver development in Windows 10, version 1703:

* [Implementing Audio Module Communication](https://docs.microsoft.com/en-us/windows-hardware/drivers/audio/implementing-audio-module-communication) - Describes the support for communication from Universal Windows Platform (UWP) apps to kernel mode audio device drivers.
* New DDIs and properties reference topics to support APO Module Communications discovery:
    - [KSPROPSETID_AudioModule](https://msdn.microsoft.com/en-us/library/windows/hardware/mt808144.aspx) - A new KS Property Set that defines three properties specific to audio modules.
    - [KSPROPERTY_AUDIOMODULE_COMMAND](https://msdn.microsoft.com/library/windows/hardware/mt808141.aspx) property - Allows Audio Module clients to send custom commands to query and set parameters on Audio Modules.
    - [IPortClsNotifications](https://msdn.microsoft.com/library/windows/hardware/mt808133.aspx) - New Port Class Notifications that provide notification helpers to miniports, to support audio module communication.

### <a name="bluetooth-1703"></a>Bluetooth

The following is a list of updates to Bluetooth in Windows 10 version 1703:

* Hands-Free Profile (HFP) 1.6 specification with Wideband speech on Windows 10 for desktop editions.
* Support for [Call Control APIs](https://docs.microsoft.com/en-us/uwp/api/Windows.ApplicationModel.Calls) on Windows 10 for desktop editions.
* Support for GATT Server, Bluetooth LE Peripheral and non-paired support for Bluetooth LE. See our [developer post](http://aka.ms/bluetoothgatt) for more details.

For more information about what's new for Bluetooth, see [Bluetooth](https://msdn.microsoft.com/en-us/windows/hardware/commercialize/design/component-guidelines/bluetooth) and [Bluetooth LE pre-pairing](https://msdn.microsoft.com/en-us/windows/hardware/commercialize/design/component-guidelines/bluetooth-prepairing).

### <a name="camera-1703"></a>Camera

The following is a list of updates to Camera driver development in Windows 10, version 1703:

* [USB Video Class (UVC) driver implementation guide](https://msdn.microsoft.com/en-us/windows/hardware/drivers/stream/uvc-driver-implementation-checklist)
* [Microsoft extensions to USB Video Class 1.5 specification](https://msdn.microsoft.com/en-us/windows/hardware/drivers/stream/uvc-extensions-1-5)
* [Device transform manager (DTM) events](https://msdn.microsoft.com/en-us/library/windows/hardware/mt797660)
* [IMFDeviceTransform interface](https://msdn.microsoft.com/en-us/library/windows/hardware/mt797663)
* KSCategory_Xxx Device Interface Classes
    - [KSCATEGORY_SENSOR_CAMERA](https://msdn.microsoft.com/en-us/library/windows/hardware/mt796964)
    - [KSCATEGORY_VIDEO_CAMERA](https://msdn.microsoft.com/en-us/library/windows/hardware/mt796965)

### <a name="kernel-1703"></a>Windows kernel


[Windows Kernel-Mode Process and Thread Manager](https://msdn.microsoft.com/en-us/library/windows/hardware/ff565772(v=vs.85).aspx) - Starting in Windows 10 version 1703, the Windows Subsystem for Linux (WSL) enables a user to run native Linux ELF64 binaries on Windows, alongside other Windows applications. For more information about WSL architecture and the user-mode and kernel-mode components that are required to run the binaries, see the posts on the [Windows Subsystem for Linux](https://blogs.msdn.microsoft.com/wsl/) blog.

### <a name="mobilebroadband-1703"></a>Mobile broadband

Updates to [**Mobile Broadband (MB)**](https://msdn.microsoft.com/windows/hardware/drivers/network/mobile-broadband--mb--design-guide) include improved [LTE attach features](https://msdn.microsoft.com/windows/hardware/drivers/network/mb-lte-attach-operations), support for [Multi-SIM Operations](https://msdn.microsoft.com/windows/hardware/drivers/network/mb-multi-sim-operations), support for [provisioning contexts](https://msdn.microsoft.com/windows/hardware/drivers/network/mb-provisioned-context-operations) into the modem, support for the [Specific Absorption Rate platform](https://msdn.microsoft.com/windows/hardware/drivers/network/mb-sar-platform-support), and support for [network blacklisting](https://msdn.microsoft.com/windows/hardware/drivers/network/mb-network-blacklist-operations).

Updates to [**Mobile Operator Scenarios (MOs)**](https://msdn.microsoft.com/windows/hardware/drivers/mobilebroadband/apn-database) include a new database format called [COSA FAQ](https://msdn.microsoft.com/windows/hardware/drivers/mobilebroadband/cosa---faq), for MOs to provision Windows Desktop MB devices. See these topics for more updates:

* [Planning your COSA/APN database submission](https://msdn.microsoft.com/windows/hardware/drivers/mobilebroadband/planning-your-apn-database-submission)
* [Submitting the COSA/APN database update](https://msdn.microsoft.com/windows/hardware/drivers/mobilebroadband/submitting-the-apn-database-update)
* [Testing your COSA/APN database submission](https://msdn.microsoft.com/windows/hardware/drivers/mobilebroadband/testing-your-apn-database-submission)

### <a name="networking-1703"></a>Networking

Updates to Networking driver development in Windows 10, version 1703 includes a new type of socket called Stream Sockets, which support Linux networking applications on Windows. See [**Winsock Kernel**](https://msdn.microsoft.com/windows/hardware/drivers/network/winsock-kernel-socket-categories) for more info. New functions and structures include [WskConnectEx](https://msdn.microsoft.com/library/windows/hardware/mt799884), [WskListen](https://msdn.microsoft.com/library/windows/hardware/mt799885), [WSK_CLIENT_STREAM_DISPATCH](https://msdn.microsoft.com/library/windows/hardware/mt799886), and [WSK_PROVIDER_STREAM_DISPATCH](https://msdn.microsoft.com/library/windows/hardware/mt799887)



### <a name="pos-1703"></a>POS

The following is a list of new topics for POS in Windows 10, version 1703:

* [Bluetooth barcode scanner UUIDs](https://msdn.microsoft.com/en-us/library/windows/hardware/mt781262)
* [BarcodeSymbologyDecodeLenthType enumeration](https://msdn.microsoft.com/en-us/library/windows/hardware/mt781217)
* [BarcodeSymbologyAttributesData structure](https://msdn.microsoft.com/en-us/library/windows/hardware/mt781216)

There is a new Gs1DWCode symbology to the [BarcodeSymbology enumeration](https://msdn.microsoft.com/en-us/library/windows/hardware/dn757474).

### <a name="usb-1703"></a>USB

Windows 10 version 1703 provides a new class extension (UcmTcpciCx.sys) that supports the Universal Serial Bus Type-C Port Controller Interface Specification. A USB Type-C connector driver does not need to maintain any internal PD/Type-C state. The complexity of managing the USB Type-C connector and USB Power Delivery (PD) state machines is handled by the system. You only need to write a client driver that communicates hardware events to the system through the class extension. For more information, see [USB Type-C Controller Interface driver class extensions reference](https://msdn.microsoft.com/library/windows/hardware/mt805826).

## What's new in Windows 10, version 1607

[Back to Top](#top)

This section describes new features and improvements for driver development in Windows 10, version 1607.

### Audio

The following is a list of new topics for Audio driver development in Windows 10, version 1607.

* [Windows Audio Architecture](https://msdn.microsoft.com/library/windows/hardware/mt631182)
* Structures and properties to better support the Cortana experience:
    * [**KSPROPERTY\_AUDIO\_MIC\_SENSITIVITY**](https://msdn.microsoft.com/library/windows/hardware/mt761741)
    * [**KSPROPERTY\_AUDIO\_MIC\_SNR**](https://msdn.microsoft.com/library/windows/hardware/mt761742)
    * [**KSAUDIO\_PACKETSIZE\_CONSTRAINTS2**](https://msdn.microsoft.com/library/windows/hardware/mt761740)
* [PKEY\_AudioEndpoint\_Default\_VolumeInDb](https://msdn.microsoft.com/library/windows/hardware/mt709031) &ndash; An INF key that provides the user a better experience when appropriate gain or attenuation is applied to the audio signal.

### <a name="camera-1607"></a>Camera

Camera driver development in Windows 10, version 1607 includes new and updated topics to support Windows Hello and face authentication:

* [Windows Hello camera driver bring up guide](https://msdn.microsoft.com/library/windows/hardware/mt742030)
* [Extended camera controls](https://msdn.microsoft.com/library/windows/hardware/mt742029)
* [**KSPROPERTY\_CAMERACONTROL\_EXTENDED\_FACEAUTH\_MODE**](https://msdn.microsoft.com/library/windows/hardware/mt742028)


### <a name="location-1607"></a>Location

Location driver development in Windows 10, version 1607 includes the following new GNSS Breadcrumb DDIs:

* [**GNSS\_BREADCRUMB\_LIST**](https://msdn.microsoft.com/library/windows/hardware/mt767989)
* [**GNSS\_BREADCRUMB\_V1**](https://msdn.microsoft.com/library/windows/hardware/mt767990)
* [**GNSS\_BREADCRUMBING\_ALERT\_DATA**](https://msdn.microsoft.com/library/windows/hardware/mt767987)
* [**GNSS\_BREADCRUMBING\_PARAM**](https://msdn.microsoft.com/library/windows/hardware/mt767988)
* [**IOCTL\_GNSS\_LISTEN\_BREADCRUMBING\_ALERT**](https://msdn.microsoft.com/library/windows/hardware/mt767991)
* [**IOCTL\_GNSS\_POP\_BREADCRUMBS**](https://msdn.microsoft.com/library/windows/hardware/mt767992)
* [**IOCTL\_GNSS\_START\_BREADCRUMBING**](https://msdn.microsoft.com/library/windows/hardware/mt767993)
* [**IOCTL\_GNSS\_STOP\_BREADCRUMBING**](https://msdn.microsoft.com/library/windows/hardware/mt767994)

### <a name="print-1607"></a>Print

Printer driver development in Windows 10, version 1607 includes [JSConstraintsDebug](https://msdn.microsoft.com/library/windows/hardware/mt740375), a command-line tool that provides debugging support for JavaScript Constraints while developing a V4 printer driver.


### <a name="wlan-1607"></a>WLAN

In Windows 10, version 1607, there are new and updated topics for WLAN Device Driver Interface (WDI) version 1.0.21. For details, see [WDI doc change history](https://msdn.microsoft.com/library/windows/hardware/mt691980).

## What's new in Windows 10, version 1507

[Back to Top](#top)

This section describes new and updated features for driver development in Windows 10.

### Bluetooth

In Windows 10, new [Microsoft-defined Bluetooth HCI extensions](https://msdn.microsoft.com/library/windows/hardware/dn917903) have been added.

### Buses and Ports

Driver programming interfaces and in-box drivers for Simple Peripheral Bus (SPB) such as I2C and SPI, and GPIO are part of OneCoreUAP-based editions of Windows. Those drivers will run on both Windows 10 for desktop editions and Windows 10 Mobile, as well as other Windows 10 versions.

### <a name="camera-1507"></a>Camera

The camera driver DDIs have converged into a Universal Windows driver model, including new [camera DDIs](https://msdn.microsoft.com/library/windows/hardware/dn937081). Additional features include:

* [Digital video stabilization](https://msdn.microsoft.com/library/windows/hardware/dn936754)
* [Variable frame rate](https://msdn.microsoft.com/library/windows/hardware/dn917971)
* [Face detection](https://msdn.microsoft.com/library/windows/hardware/dn917937)
* [Video high dynamic range (HDR)](https://msdn.microsoft.com/library/windows/hardware/dn936752)
* [Optical stabilization](https://msdn.microsoft.com/library/windows/hardware/dn917954)
* [Scene analysis: photo HDR, flash no flash, ultra low light](https://msdn.microsoft.com/library/windows/hardware/dn917934)
* [Capture stats: metadata framework/attributes, histograms](https://msdn.microsoft.com/library/windows/hardware/dn917945)
* [Smooth zoom](https://msdn.microsoft.com/library/windows/hardware/dn936756)
* [Hardware optimization hints](https://msdn.microsoft.com/library/windows/hardware/dn917956)
* [Camera profiles](https://msdn.microsoft.com/library/windows/hardware/dn897239)

### Cellular

[Cellular architecture and implementation](https://msdn.microsoft.com/library/windows/hardware/dn927266) for Windows 10 has been updated.

### Display

The [display driver model](https://msdn.microsoft.com/library/windows/hardware/ff570595) from Windows 8.1 and Windows Phone have converged into a unified model for Windows 10.

A new memory model is implemented that gives each GPU a per-process virtual address space. Direct addressing of video memory is still supported by WDDMv2 for graphics hardware that requires it, but that is considered a legacy case. IHVs are expected to develop new hardware that supports virtual addressing. Significant changes have been made to the DDI to enable this new memory model.

### <a name="human-interface-device"></a>Human Interface Device (HID)

The new Virtual HID Framework (VHF) eliminates the need for writing a kernel-mode transport minidriver. The framework comprises a Microsoft-provided static library (Vhfkm.lib) that exposes programming elements used by your driver. It also includes a Microsoft-provided in-box driver (Vhf.sys) that enumerates one or more child devices and proceeds to build a virtual [Human Interface Device](https://msdn.microsoft.com/windows/hardware/drivers/hid/) (HID) tree.

* [Write a HID source driver by using Virtual HID Framework (VHF)](https://msdn.microsoft.com/library/windows/hardware/dn925056)
* [Virtual HID Framework Callback Functions](https://msdn.microsoft.com/library/windows/hardware/dn925049)
* [Virtual HID Framework Methods](https://msdn.microsoft.com/library/windows/hardware/dn925053)
* [Virtual HID Framework Structures](https://msdn.microsoft.com/library/windows/hardware/dn925054)

### <a name="location-1507"></a>Location

The Global Navigation Satellite System (GNSS) driver DDIs have converged to a [GNSS Universal Windows driver model](https://msdn.microsoft.com/library/windows/hardware/dn917815) (UMDF 2.0).

### <a name="near-field-communication"></a>Near Field Communication (NFC)

The [NFC DDIs](https://msdn.microsoft.com/library/windows/hardware/jj866056) have a new converged driver model to support mobile and desktop solutions.

[NFC Class Extension](https://msdn.microsoft.com/library/windows/hardware/dn905534): A new NFC class extension driver is available. The NFC class extension driver implements all of the Windows-defined DDIs to interact with the NFC controller, secure elements, and remote RF endpoints.

### <a name="networking-1507"></a>Networking

The new [PacketDirect Provider Interface (PDPI)](https://msdn.microsoft.com/library/windows/hardware/dn931858) is available as an extension to the existing NDIS miniport driver model. The PDPI provides an I/O model that allows applications to manage their own buffers, poll processors, and directly manage sending and receiving packets over a miniport adapter. The combination of these capabilities allow the application to completely control its own contexts leading to a much higher packet-per-second (pps) ratio.

### <a name="print-1507"></a>Print

The print driver is updated with v4 Print driver improvements and changes to support wireless printing from mobile devices, as well as the following:

* [V4 Driver Manifest](https://msdn.microsoft.com/library/windows/hardware/jj218737) &ndash; Provides information on changes to the v4 print driver manifest to support the PWG Raster rendering filter, including updated DriverConfig and DriverRender directives, and an updated example manifest.
* [WS-Discovery Mobile Printing Support](https://msdn.microsoft.com/library/windows/hardware/dn897455) &ndash; Describes the WS-Discovery requirements to enable mobile printing from Windows 10 Mobile devices to Windows 10 Mobile compatible printers.
* [**IXpsRasterizationFactory2 interface**](https://msdn.microsoft.com/library/windows/hardware/dn937110) &ndash; Supports printer content conversion from XPS to PWG Raster using the XPS Rasterization Service. PWG Raster supports non-square DPIs.
* [**Print Pipeline Property Bag**](https://msdn.microsoft.com/library/windows/hardware/ff561066) &ndash; New PrintDeviceCapabilities property to enable XPS rendering filters to retrieve the new PrintDeviceCapabilities XML files from the Print filter pipeline property bag.
* [GetWithArgument Request and Response Schemas](https://msdn.microsoft.com/library/windows/hardware/dn936869) &ndash; Provides support for mobile printing with a formal definition and example for the GetWithArgument request and response bidirectional communications schemas.
* [**IBidiSpl::SendRecv method**](https://msdn.microsoft.com/library/windows/hardware/dd144988) &ndash; Adds support for mobile printing with the GetWithArgument bidirectional schema value.

### Smart Card

In Windows 10, there is a new class extension module, Wudfsmcclassext.dll, which handles complex driver operations. Smart card hardware-specific tasks are handled by your client driver. There are new programming interfaces that your client driver can use to send information about the card to the class extension so that it can process requests. Those driver programming interfaces are part of OneCoreUAP-based editions of Windows.

* [Smart card client driver event callback functions](https://msdn.microsoft.com/library/windows/hardware/dn946583)
* [Smart card client driver support methods](https://msdn.microsoft.com/library/windows/hardware/dn946584)

### Storage

In Windows 10, new storage firmware updates (IOCTL interface) allow partners to update their storage device firmware. These updates include:

* Storage protocol pass through &ndash; The updated storage pass through IOCTL interface supports newer protocols including non-volatile memory express (NVMe).
* Expanded storage query interfaces &ndash; The expanded storage query interface allows applications to query protocol-dependent information.

### System-Supplied Driver Interfaces

The [GUID\_DEVICE\_RESET\_INTERFACE\_STANDARD](https://msdn.microsoft.com/library/windows/hardware/dn928420) interface defines a standard way for function drivers to attempt to reset and recover a malfunctioning device.

### USB

Here are the new features for USB in Windows 10. For more information, see [Windows 10: What's new for USB](https://msdn.microsoft.com/library/windows/hardware/dn957037).

* Native support for USB Type-C as defined in the USB 3.1 specification. If you are building a system with USB Type-C connectors, you can use the in-box [USB Type-C Connector System Software Interface (UCSI) driver](https://msdn.microsoft.com/library/windows/hardware/mt710944) or [write a USB Type-C connector driver.](https://msdn.microsoft.com/library/windows/hardware/mt595924).
* The dual role feature allows a mobile device, such as a phone, a phablet or a tablet, to designate itself as being a *device* or a *host*. See [USB Dual Role Driver Stack Architecture](https://msdn.microsoft.com/library/windows/hardware/dn957036) for more information.
* Support for writing a driver for USB emulated devices by using the [Microsoft-provided USB device emulation class extension (UdeCx)](https://msdn.microsoft.com/library/windows/hardware/mt595925).
* Support for writing a driver for a host controller that is not xHCI specification-compliant or a virtual host controller. To write such a driver, see [Developing Windows drivers for USB host controllers](https://msdn.microsoft.com/library/windows/hardware/mt187811).
* Support writing function controller driver by using USB function class extension (UFX). See [Developing Windows drivers for USB function controllers](https://msdn.microsoft.com/library/windows/hardware/mt187810).

### <a name="wlan-1507"></a>WLAN

WDI (WLAN Device Driver Interface) is a new [WLAN Universal Windows driver model](https://msdn.microsoft.com/library/windows/hardware/dn897672) that converges the WLAN drivers on Windows 10 for desktop editions and Windows 10 Mobile.

[Back to Top](#top) 

## Deprecated features

The following table describes Windows driver development features that have been removed in Windows 10.

| Driver technology | Feature | Deprecated in |
|---|---|---|
| GNSS/Location | [Geolocation driver sample for Windows 8.1](https://docs.microsoft.com/en-us/windows-hardware/drivers/gnss/sensors-geolocation-driver-sample) and related documentation | Windows 10, version 1709 |
| Mobile Operator Scenarios (Networking) | [AllowStandardUserPinUnlock](https://review.docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/allowstandarduserpinunlock?branch=duncan_mos_rs3) | Windows 10, version 1709 |
| Scan/Image | [WSD (Web Services for Devices) Challenger](https://docs.microsoft.com/en-us/windows-hardware/drivers/image/challenging-a-disconnected-scanner-with-the-wsd-challenger) functionality and related documentation | Windows 10, version 1709 |
|Mobile Operators| Mobile broadband app experience apps with Sysdev metadata packages are deprecated in favor of MO UWP APPS and COSA. | Windows 10, version 1803|
