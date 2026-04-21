# Information
Hands-on IT lab portfolio showcasing full-stack technical proficiency, from physical connectivity and network switching to scalable routing, secure transport, and enterprise application services. Projects illustrate a complete lifecycle of implementation, progressing from foundational configurations to complex, real-world solutions that secure and optimize the entire data path.

Content is organized using the **`TCP/IP 5-layer Internet model`**, with each lab categorized by the highest layer it meaningfully interacts with. Labs are also aligned with the most common IT lifecycle scenarios, covering **Provisioning**, **Maintenance**, and **Troubleshooting**.

A range of simulator, emulator, and hypervisor software are valid options depending on lab complexity, ensuring both accessibility and realistic network behavior. Software considered but not limited to: 
<p align="center">
  <table align="center">
    <tr>
      <td align="center">
        <a href="https://www.netacad.com/resources/lab-downloads" target="_blank" rel="noopener noreferrer">
          <img src="README%20Elements/Cisco-Packet-Tracer-logo.png" width="40"><br>
          Cisco Packet Tracer
        </a>
      </td>
      <td align="center">
        <a href="https://www.eve-ng.net/index.php/download/" target="_blank" rel="noopener noreferrer">
          <img src="README%20Elements/EVE-NG-logo.png" width="40"><br>
          EVE-NG
        </a>
      </td>
      <td align="center">
        <a href="https://www.gns3.com/software/download" target="_blank" rel="noopener noreferrer">
          <img src="README%20Elements/GNS3-logo.png" width="40"><br>
          GNS3
        </a>
      </td>
      <td align="center">
        <a href="https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion" target="_blank" rel="noopener noreferrer">
          <img src="README%20Elements/VMware-logo.png" width="40"><br>
          GNS3
        </a>
      </td>
    </tr>
  </table>
</p>

# Labs

<div align="center">

| Layer | Devices | Protocols/Tech | Labs |
|:---|:---|:---|:---|
| 5 - Application | Servers, Desktops, Load Balancers, Firewalls (NGFW / L7) | HTTP, HTTPS, DNS, DHCP, SSH, TELNET, FTP, SMTP, NTP, SNMP, Syslog | [View Labs](Layer%205%20-%20Application) |
| 4 - Transport | Firewalls (stateful), Load Balancers | TCP, UDP, Port Numbers, Flow Control, Error Recovery | [View Labs](Layer%204%20-%20Transport) |
| 3 - Network | Routers, Layer 3 Switches, Firewalls | IPv4, IPv6, ICMP, IGMP, APIPA, SLAAC, BGP, OSPF, EIGRP, IS-IS, RIP, VRF, NAT, HSRP, VRRP, ACLs, Subnetting, VLSM | [View Labs](Layer%203%20-%20Network) |
| 2 - Data Link | Switches, Bridges, Wireless Access Points | Ethernet, MAC Addressing, VLANs, STP, DTP, VTP, ARP, NDP, CDP, LLDP, EtherChannel | [View Labs](Layer%202%20-%20Data%20Link) |
| 1 - Physical | Hubs, Repeaters, Cables, Transceivers (SFPs) | Fiber, Copper, RF (Wi-Fi PHY) | [View Labs](Layer%201%20-%20Physical) |

</div>

## General Commands
### Windows (CMD / Powershell CLI)
- 
### Linux (Bash CLI)
- 
### Cisco (IOS / IOS XE CLI)
- **`enable`** — Transitions the user from `user EXEC` mode (the initial, limited-access CLI mode) to `privileged EXEC` mode, granting access to advanced monitoring and configuration commands.
- **`configure terminal`** — Enters `global configuration` mode from `privileged EXEC` mode, allowing the user to modify the device’s running configuration.
- **`?`** — Provides context-sensitive help:
  - When used on its own or after a command with a space (e.g., `?` or `show ?`), it displays available commands, subcommands, or arguments. **`UPPERCASE`** placeholders indicate a value you must define, **`lowercase`** keywords must be entered exactly as shown.
  - When used immediately after a partial command (e.g., `con?`), it attempts to show matching options.
  - In context-sensitive help, `<cr>` (carriage return) indicates that the command is complete and can be executed by pressing `ENTER`. Additional arguments may still be available, but they are optional when `<cr>` is shown.
- **`no`** — Negates or removes a commands effect when prefixed before the command. This is commonly used to disable features or delete configuration statements (e.g., `no shutdown`, `no ip address`).
- **`do`** — Allows execution of `privileged EXEC` mode commands while in various configuration modes, such as `global configuration` mode.
- **`exit`** — Exits the current mode and returns to the previous mode.
- **`show`** — Displays operational and configuration information about the device.
Commonly used in `privileged EXEC` mode to verify status, interfaces, routing, and the current configuration (e.g., `show running-config`, `show ip interface brief`).
- **`write`**, **`write memory`**, **`copy running-config startup-config`** — Saves the active `running-config` (in RAM) to the `startup-config` (in NVRAM). All three commands perform the same function: copying the active (running) configuration in RAM to NVRAM so it is retained after a reboot.
>💡 **Quick Tip(s):** The commands available and how you interact with the device’s operating system depend on the current CLI mode. There are also a number of hotkeys and other shortcuts to better navigate the Cisco IOS / IOS XE CLI:
> - Partially typed keywords are accepted if unambiguous (e.g., `en` for `enable`). The OS recognizes the unique abbreviation without requiring the full command.
> - Press `TAB` to autocomplete a partially typed command or keyword. Only works if the abbreviation is unambiguous (e.g., `e` by itself is ambiguous — could be `enable` or `exit`).
> - Use the `UP` and `DOWN` arrow keys to navigate through command history. Press `ENTER` to execute a selected command.
> - Press `CTRL + A` to move the line cursor to the beginning of the command line.
> - Press `CTRL + E` to move the line cursor to the end of the command line.
### Juniper (Junos OS CLI)
- 
### Fortinet (FortiOS CLI)
- 
