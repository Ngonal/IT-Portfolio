# Information
Hands-on IT lab portfolio demonstrating full-stack technical proficiency — from physical connectivity and switching to scalable routing, secure transport, and enterprise application services. Each example reflects an essential part of the implementation lifecycle, progressing from foundational configurations to complex, real-world solutions that secure and optimize the entire data path while maintaining professional-grade documentation.

Content is structured using the Internet Protocol Suite via the **`TCP/IP 5-layer Internet model`**, with each example categorized by the highest layer it meaningfully engages. Labs/Projects are further aligned to common IT lifecycle scenarios, including **Provisioning**, **Maintenance**, and **Troubleshooting**.

A variety of simulators, emulators, and hypervisors is used based on scenario complexity, balancing accessibility with realistic system behavior. Software utilized includes, but is not limited to:
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
          VMware
        </a>
      </td>
    </tr>
  </table>
</p>

# Projects & Labs

<div align="center">

| Layer | Devices | Protocols/Tech | Count | Examples |
|:---|:---|:---|:--:|:--:|
| 5 - Application | Servers, Desktops, Load Balancers, Firewalls (NGFW / L7) | HTTP, HTTPS, DNS, DHCP, SSH, TELNET, FTP, SMTP, NTP, SNMP, SSL, TLS, AFP, LPP, NCP, NDR, XDR, Syslog | 0 | [View](Layer%205%20-%20Application) |
| 4 - Transport | Firewalls (Stateful), Load Balancers | TCP, UDP, Port Numbers, Flow Control, Error Recovery | 0 | [View](Layer%204%20-%20Transport) |
| 3 - Network (Internet) | Routers, Layer 3 (Multilayer) Switches, Firewalls (Stateless) | IPv4, IPv6, ICMP, IGMP, APIPA, SLAAC, BGP, OSPF, EIGRP, IS-IS, RIP, VRF, NAT, HSRP, VRRP, GLBP, ACLs, Subnetting, FLSM, VLSM | 1 | [View](Layer%203%20-%20Network) |
| 2 - Data Link (Network Access) | Switches, Bridges, Wireless Access Points | Ethernet, MAC Addressing, VLANs, STP, PVST, DTP, VTP, ARP, NDP, CDP, LLDP, CDMA/CD, CDMA/CA, EtherChannel, LACP, PAgP, Autonegotiation | 0 | [View](Layer%202%20-%20Data%20Link) |
| 1 - Physical | Hubs, Repeaters, Cables, Transceivers (SFPs) | Fiber, Copper, RF (Wi-Fi, Satellite), Speed, Duplex | 2 | [View](Layer%201%20-%20Physical) |

</div>

## General Commands
### Windows (CMD / Powershell CLI)
- **`ping`** —
- **`tracert`** —
- **`ipconfig`** —
### Linux (Bash CLI)
- **`ping`** —
- **`traceroute`** —
- **`ifconfig`** —
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
