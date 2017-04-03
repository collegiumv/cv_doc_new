# DeviceManager

Because Collegium V maintains a separate wired network from the rest
of the university, devices must be registered on it separate from the
registration for the broader university network.  This registration
occurs through the **DeviceManager** in
[https://constellation.collegiumv.org](https://constellation.collegiumv.org).

The login for Constellation uses the same credentials as your CV
account
([http://account.collegiumv.org](http://account.collegiumv.org)).

## Windows

1. Launch PowerShell.exe.
    1. Press the windows key.
    2. Type "PowerShell.exe"
    3. Press enter.
2. Run `Get-NetAdapter | select Name,MacAddress`
    1. Copy the command text.
    2. Right click inside the PowerShell window to paste the copied
       text.
    3. Press enter.
3. Copy the text in the "MACAddress" column that corresponds to
   "Ethernet".
    1. Highlight the text with the mouse.
    2. Right click to copy the selected text.
4. Paste the copied text into the *MAC Address* field in Constellation.
5. Type any name for *Device Friendly Name*.
5. Run `Get-ChildItem env:ComputerName` in PowerShell.
6. Copy the text under the "Value" column.
    1. Highlight the text with the mouse.
    2. Right click to copy the selected text.
7. Paste the copied text into the *Device Hostname* field in Constellation.

## macOS

Go to *System Preferences* from the Apple Menu.

![Apple
Menu](/img/constellation-device-manager-macos_menu-preferences.png)

Select *Network* from System Preferences.

![Select
*Network*](/img/constellation-device-manager-macos_preferences-network.png)

Select the *Hardware* tab.

![Select
*Hardware*](/img/constellation-device-manager-macos_network_advanced-hardware.png)

Record the MAC Address into the *MAC Address* field in Constellation.

![Record MAC
Address](/img/constellation-device-manager-macos_network_advanced_hardware-mac.png)

Select *Sharing* from System Preferences.

![Select
*Sharing*](/img/constellation-device-manager-macos_preferences-sharing.png)

Record the hostname into the *Device Hostname* field in Constellation.

![Record
Hostname](/img/constellation-device-manager-macos_sharing-hostname.png)

## Linux

To get a device's MAC address, run `ip address` at a shell prompt.
Each interface will have its own section in the output;  the
interface's MAC address is the first hexadecimal string on the line
beginning `link/ether`.

To get a device's hostname, run `hostname` at a shell prompt.
