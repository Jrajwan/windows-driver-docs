---
title: Setting Up KDNET Network Kernel Debugging Manually
description: Debugging Tools for Windows supports kernel debugging over a network.
ms.assetid: B4A79B2E-D4B1-42CA-9121-DEC923C76927
keywords: ["Network debugging", "Ethernet debugging", "Docking station", "Setting Up Kernel-Mode Debugging over a Network Cable Manually"]
ms.author: domars
ms.date: 06/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Setting Up KDNET Network Kernel Debugging Manually

Debugging Tools for Windows supports kernel debugging over a network. This topic describes how to set up network debugging manually.

> [!TIP]
> Setting up a network debugging manually can be a complex and error prone process.
> To set up network debugging automatically, see [Setting Up KDNET Network Kernel Debugging Automatically](setting-up-a-network-debugging-connection-automatically.md).

The computer that runs the debugger is called the *host computer*, and the computer being debugged is called the *target computer*. The host computer must be running Windows 7 or later, and the target computer must be running Windows 8 or later.

Debugging over a network has the following advantages compared to debugging over other types of connectivity.

- The host and target computers can be anywhere on the local network.
- It is easy to debug many target computers from one host computer.
- Given any two computers, it is likely that they will both have Ethernet adapters. It is less likely that they will both have serial ports or both have 1394 ports.
- Network debugging is significantly faster than serial port debugging.

## Supported Network Adapters

The host computer can use any network adapter, but the target computer must use a network adapter that is supported by Debugging Tools for Windows. For a list of supported network adapters, see [Supported Ethernet NICs for Network Kernel Debugging in Windows 10](supported-ethernet-nics-for-network-kernel-debugging-in-windows-10.md) and [Supported Ethernet NICs for Network Kernel Debugging in Windows 8.1](supported-ethernet-nics-for-network-kernel-debugging-in-windows-8-1.md).

## Install the Debugging Tools for Windows

Confirm that the Debugging Tools for Windows are installed on the host system. For information on downloading and installing the debugger tools, see [Download Debugging Tools for Windows](debugger-download-tools.md).

## Determining the IP Address of the Host Computer

Use one of the following procedures to determine the IP address of the host computer.

1. On the host computer, open a Command Prompt window and enter the following command:

   ```shell
   ipconfig
   ```

    Make a note of the IPv4 address of the network adapter that you intend to use for debugging.

2. On the target computer, open a Command Prompt window and enter the following command, where *YourIPAddress* is the IP address of the host computer:

   ```shell
   ping -4 <YourIPAddress>
   ```

## Choosing a Port for Network Debugging

Choose a port number that will be used for debugging on both the host and target computers. You can choose any number from 49152 through 65535, the recommended range is 50000 - 50039. The port that you choose will be opened for exclusive access by the debugger running on the host computer. Take care to choose a port number that is not used by any other applications that run on the host computer.

**Note**  The range of port numbers that can be used for network debugging might be limited by your company's network policy. There is no way to tell from the host computer what the limitations are. To determine whether your company's policy limits the range of ports that can be used for network debugging, check with your network administrators.

If you connect several target computers to a single host computer, each connection must have a unique port number. For example, if you connect 100 target computers to a single host computer, you can assign port 50000 to the first connection, port 50001 to the second connection, port 50002 to the third connection, and so on.

**Note**  A different host computer could use the same range of ports (50000 through 50099) to connect to another 100 target computers.

## Setting Up the Target Computer

1. Verify that the target computer has a supported network adapter. See these topics for more information.

    - [Supported Ethernet NICs for Network Kernel Debugging in Windows 8.1](supported-ethernet-nics-for-network-kernel-debugging-in-windows-8-1.md)

    - [Supported Ethernet NICs for Network Kernel Debugging in Windows 10](supported-ethernet-nics-for-network-kernel-debugging-in-windows-10.md)

2. Connect the supported adapter to a network hub or switch using an appropriate network cable.

> [!IMPORTANT]
> Before using BCDEdit to change boot information you may need to temporarily suspend Windows security features such as BitLocker and Secure Boot on the test PC.
> Re-enable these security features when testing is complete and appropriately manage the test PC, when the security features are disabled.

3. In an elevated Command Prompt window, enter the following commands, where *w.x.y.z* is the IP address of the host computer, and *n* is a port number of your choice:

    ```shell
    bcdedit /debug on

    bcdedit /dbgsettings net hostip:w.x.y.z port:n
    ```

4. **bcdedit** will display an automatically generated key. Copy the key and store it on a removable storage device like a USB flash drive. You will need the key when you start a debugging session on the host computer.

    **Note**  We strongly recommend that you use an automatically generated key. However, you can create your own key as described later in the "Creating Your Own Key" section.

5. If there is more than one network adapter in the target computer, use Device Manager to determine the PCI bus, device, and function numbers for the adapter you want to use for debugging. Then in an elevated Command Prompt window, enter the following command, where *b*, *d*, and *f* are the bus number, device number, and function number of the adapter:

    ```shell
    bcdedit /set "{dbgsettings}" busparams b.d.f
    ```

6. The target PC will be rebooted after a kernel debugger is attached. This is described in the next section.

**Note**  If you intend to install the Hyper-V role on the target computer, see [Setting Up Network Debugging of a Virtual Machine Host](setting-up-network-debugging-of-a-virtual-machine-host.md).

**Caution**  If your target computer is in a docking station, and you have network debugging enabled for a network adapter that is part of the docking station, do not remove the computer from the docking station. If you need to remove the target computer from the docking station, disable kernel debugging first. To disable kernel debugging on the target computer, open a Command Prompt window as Administrator and enter the command **bcdedit /debug off**. Reboot the target computer.

## Starting the Debugging Session

Confirm that the network adapter of the host computer to a network hub or switch using an appropriate network cable.

On the host computer, open WinDbg. On the **File** menu, choose **Kernel Debug**. In the Kernel Debugging dialog box, open the **Net** tab. Enter your port number and key. Click **OK**.

You can also start a session with WinDbg by opening a Command Prompt window and entering the following command, where *n* is your port number and *MyKey* is the key that was automatically generated by **bcdedit** when you set up the target computer:

```shell
windbg -k net:port=<n>,key=<MyKey>
```

If you are prompted about allowing WinDbg to access the port through the firewall, allow WinDbg to access the port for **all three** of the different network types.

### Using KD

On the host computer, open a Command Prompt window. Enter the following command, where *n* is your port number and *MyKey* is the key that was automatically generated by **bcdedit** when you set up the target computer:

```shell
kd -k net:port=<n>,key=<MyKey>
```

If you are prompted about allowing WinDbg to access the port through the firewall, allow WinDbg to access the port for **all three** of the different network types.

## Restarting the Target PC

Once the debugger is connected, reboot the target computer. One way to do restart the PC is to use this command, from an administrator's command prompt.

   ```shell
   shutdown -r -t 0
   ```

When the target is restarted, the debugger in the host OS should connect.

After connecting to the target on the host, hit break on your debugger and you can start debugging.

### Allowing the debugger through the firewall

When you first attempt to establish a network debugging connection, you might be prompted to allow the debugging application (WinDbg or KD) access through the firewall. Client versions of Windows display the prompt, but Server versions of Windows do not display the prompt. You should respond to the prompt by checking the boxes for **all three** network types: domain, private, and public. If you do not get the prompt, or if you did not check the boxes when the prompt was available, you must use Control Panel to allow access through the firewall. Open **Control Panel &gt; System and Security** and click **Allow an app through Windows Firewall**. In the list of applications, locate Windows GUI Symbolic Debugger and Windows Kernel Debugger. Use the check boxes to allow those two applications through the firewall. Restart your debugging application (WinDbg or KD).

## How the Debugger Obtains an IP Address for the Target Computer

The kernel debugging driver on the target computer attempts to use Dynamic Host Configuration Protocol (DHCP) to get a routable IP address for the network adapter that is being used for debugging. If the driver obtains a DHCP-assigned address, then the target computer can be debugged by host computers located anywhere on the network. If the driver fails to obtain a DHCP-assigned address, it uses Automatic Private IP Addressing (APIPA) to obtain a local link IP address. Local link IP addresses are not routable, so a host and target cannot use a local link IP address to communicate through a router. In that case, network debugging will work if you plug the host and target computers into the same network hub or switch.

## Encryption key

To keep the target computer secure, packets that travel between the host and target computers must be encrypted. We strongly recommend that you use an automatically generated encryption key (provided by **bcdedit** when you configure the target computer). Network debugging uses a 256-bit key that is specified as four 64-bit values, in base 36, separated by periods. Each 64-bit value is specified by using up to 13 characters. Valid characters are the letters a through z and the digits 0 through 9. Special characters are not allowed.

To specify your own key, open an elevated Command Prompt window on the target computer. Enter the following command, where *w.x.y.z* is the IP address of the host computer, and *n* is your port number, and *Key* is your key:

```shell
bcdedit /dbgsettings net hostip:w.x.y.z port:n key:Key
```

Reboot the target computer.

## Troubleshooting Tips

### Debugging application must be allowed through firewall

When you first attempt to establish a network debugging connection, you might be prompted to allow the debugging application (WinDbg or KD) access through the firewall. Client versions of Windows display the prompt, but Server versions of Windows do not display the prompt. You should respond to the prompt by checking the boxes for **all three** network types: domain, private, and public. If you do not get the prompt, or if you did not check the boxes when the prompt was available, you must use Control Panel to allow access through the firewall. Open **Control Panel &gt; System and Security** and click **Allow an app through Windows Firewall**. In the list of applications, locate *Windows GUI Symbolic Debugger* and *Windows Kernel Debugger*. Use the check boxes to allow those two applications through the firewall. Scroll down and click **OK**, to save the firewall changes. Restart the debugger.

### Port number must be in range allowed by network policy

The range of port numbers that can be used for network debugging might be limited by your company's network policy. To determine whether your company's policy limits the range of ports that can be used for network debugging, check with your network administrator. On the target computer, open a Command Prompt window as Administrator and enter the command **bcdedit /dbgsettings**. The output will be similar to this.

```shell
C:\> bcdedit /dbgsettings
key                     XXXXXX.XXXXX.XXXXX.XXXXX
debugtype               NET
hostip                  169.168.1.1
port                    50085
dhcp                    Yes
The operation completed successfully.
```

In the preceding output, the value of port is 50085. If the value of port lies outside the range allowed by your network administrator, enter the following command, where *w.x.y.z* is the IP address of the host computer, and *YourDebugPort* is a port number in the allowed range.

```shell
bcdedit /dbgsettings net hostip:w.x.y.z port:YourDebugPort
```

When the host debugger is connected, reboot the target computer.

### Use Ping to test connectivity

If the debugger does not connect use the ping command on the target PC to verify connectivity.

   ```shell
   C:\>Ping <HostComputerIPAddress>
   ```

### Obtaining an IP Address for the Target Computer

The kernel debugging driver on the target computer attempts to use Dynamic Host Configuration Protocol (DHCP) to get a routable IP address for the network adapter that is being used for debugging. If the driver obtains a DHCP-assigned address, then the target computer can be debugged by host computers located anywhere on the network. If the driver fails to obtain a DHCP-assigned address, it uses Automatic Private IP Addressing (APIPA) to obtain a local link IP address. Local link IP addresses are not routable, so a host and target cannot use a local link IP address to communicate through a router. In that case, network debugging will work if you plug the host and target computers into the same network hub or switch.

### Specify busparams if target computer has multiple network adapters

If your target computer has more than one network adapter, you must specify the bus, device, and function numbers of the network adapter that you intend to use for debugging. To specify the bus parameters, Open Device Manager, and locate the network adapter that you want to use for debugging. Open the property page for the network adapter, and make a note of the bus number, device number, and function number. In an elevated Command Prompt Window, enter the following command, where *b*, *d*, and *f* are the bus, device and function numbers in decimal format:

```shell
bcdedit /set "{dbgsettings}" busparams b.d.f
```

When the host debugger is connected, reboot the target computer.

## Manually delete BCDEdit entries

Manually deleting is not normally required but is provided here as a troubleshooting procedure for unusual situations.

Manually deleting entries is not necessary when using the kdnet utility. For more information, see [Setting Up KDNET Network Kernel Debugging Automatically](setting-up-a-network-debugging-connection-automatically.md).

When you use bcdedit –deletevalue, you must provide a valid bcd element name. For more information, see [BCDEdit /deletevalue](https://docs.microsoft.com/windows-hardware/drivers/devtest/bcdedit--deletevalue)

To manually delete BCDEdit entries, complete these steps.

1. On the target computer, open a Command Prompt window as Administrator.

2. As an example, enter this command to delete the BCDEdit debugging entry for the host IP address.

    ```shell
    bcdedit -deletevalue {dbgsettings} hostip
    ```

When you delete the hostip, you need to specify *target=* on the debugger command line.

3. As another example, delete the port entry using this command.

    ```shell
    bcdedit -deletevalue {dbgsettings} port
    ```

When you delete the port entry, KDNET will use the default ICANN registered debugger port of 5364.

## Hyper-V

### Setting up Hyper-V

If you intend to install the Hyper-V role on the target computer, see [Setting Up Network Debugging of a Virtual Machine Host](setting-up-network-debugging-of-a-virtual-machine-host.md).

For information on debugging a hyper-v Virtual Machine (VM), see [Setting Up Network Debugging of a Virtual Machine - KDNET](setting-up-network-debugging-of-a-virtual-machine-host.md)

### Installing KDNET on the host OS when Hyper-V debugging is enabled

There is a specific situation, that is not too common, that can cause some confusion and what will appear as a networking failure. In this scenario:

- Hyper-V has been enabled on the PC and the target VM is configured for debugging.

- There is a need to configure the host OS to debug Windows that is supporting the VM. To do this, KDNET is configured in the host OS.

Because KDNET will need exclusive access to the physical adapter, it will take over all access to the adapter.  When this occurs, the VM will no longer be able to access the network using the configured network adapters. If this occurs and you want to re-enable network access for the VMs, complete these steps.

1. Open the Virtual Switch Manager from Hyper-V Manager, select your existing Virtual Switch, and change the external network NIC to the *Microsoft Kernel Debug Network Adapter* by selecting it from the drop down box and then clicking OK in the Virtual Switch Manager dialog box.

2. After updating your Virtual Switch NIC, shutdown and restart your VMs.

## Related topics

[Setting Up KDNET Network Kernel Debugging Automatically](setting-up-a-network-debugging-connection-automatically.md)

[Supported Ethernet NICs for Network Kernel Debugging in Windows 10](supported-ethernet-nics-for-network-kernel-debugging-in-windows-10.md)

[Supported Ethernet NICs for Network Kernel Debugging in Windows 8.1](supported-ethernet-nics-for-network-kernel-debugging-in-windows-8-1.md)
