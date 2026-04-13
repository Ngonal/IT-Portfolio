# Information
Hands-on networking lab portfolio showcasing practical experience in switching, routing, and security configurations. Labs progress from foundational setups to increasingly advanced implementations, emphasizing both depth and real-world applicability.

Content is organized using the TCP/IP 5-Layer Model, with each lab categorized by the highest layer it meaningfully interacts with. Labs are also aligned with the most common networking lifecycle scenarios, covering **Provisioning**, **Maintenance**, and **Troubleshooting**.

A range of simulators and emulators are valid options depending on lab complexity, ensuring both accessibility and realistic network behavior. Emulator/Simulator software considered but not limited to: 
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
    </tr>
  </table>
</p>

---

<div align="center">

| Layer | Devices | Protocols/Tech | Labs |
|:---|:---|:---|:---|
| 5 - Application | Servers, Load Balancers, Firewalls (NGFW / L7) | HTTP, DNS, DHCP, SSH, FTP, SMTP, NTP, SNMP, Syslog | [View Labs](Layer%205%20-%20Application) |
| 4 - Transport | Firewalls (stateful), Load Balancers | TCP, UDP, Port Numbers, Flow Control, Error Recovery | [View Labs](Layer%204%20-%20Transport) |
| 3 - Network | Routers, Layer 3 Switches, Firewalls | IPv4, IPv6, ICMP, OSPF, BGP, RIP, EIGRP, VRF, NAT, HSRP, Subnetting, VLSM, ACLs | [View Labs](Layer%203%20-%20Network) |
| 2 - Data Link | Switches, Bridges, Wireless Access Points | Ethernet, MAC Addressing, VLANs, STP, DTP, VTP, ARP, NDP, CDP, LLDP, EtherChannel | [View Labs](Layer%202%20-%20Data%20Link) |
| 1 - Physical | Hubs, Repeaters, Cables, Transceivers (SFPs) | Fiber, Copper, RF (Wi-Fi PHY) | [View Labs](Layer%201%20-%20Physical) |

</div>

## General Commands
### Cisco IOS / IOS XE
- **`enable`**  
Transitions the user from `user EXEC` mode (the initial, limited-access CLI mode) to `privileged EXEC` mode, granting access to advanced monitoring and configuration commands.
- **`configure terminal`**  
Enters `global configuration` mode from `privileged EXEC` mode, allowing the user to modify the device’s running configuration.
- **`?`**  
Provides context-sensitive help:
  - When used on its own or after a command with a space (e.g., `?` or `show ?`), it displays available commands, subcommands, or arguments. **`UPPERCASE`** placeholders indicate a required value you must supply, **`lowercase`** keywords must be entered exactly as shown.
  - When used immediately after a partial command (e.g., `con?`), it attempts to show matching options.
  - In context-sensitive help, `<cr>` (carriage return) indicates that the command is complete and can be executed by pressing `Enter`. Additional arguments may still be available, but they are optional when `<cr>` is shown.
- **`no`**  
Negates or removes a commands effect when prefixed before the command . This is commonly used to disable features or delete configuration statements (e.g., `no shutdown`, `no ip address`).
- **`do`**  
Allows execution of `privileged EXEC` mode commands while in various configuration modes, such as `global configuration` mode.
- **`exit`**  
Exits the current mode and returns to the previous mode.
- **`show`**  
Displays operational and configuration information about the device.
Commonly used in `privileged EXEC` mode to verify status, interfaces, routing, and the current configuration (e.g., `show running-config`, `show ip interface brief`).
- **`write`**, **`write memory`**, **`copy running-config startup-config`**  
Saves the `running-config` to the `startup-config`. All three commands perform the same function: copying the active (running) configuration in RAM to NVRAM so it is retained after a reboot.
> 💡 **Quick Tips:**
> - The commands available and how you interact with the device’s operating system depend on the current CLI mode.
> - Press `TAB` to autocomplete a partially typed command or keyword.
> - Use the `UP` and `DOWN` arrow keys to navigate through command history. Press `ENTER` to execute a selected command..
> - Press `Ctrl + A` to move the cursor to the beginning of the command line.
> - Press `Ctrl + E` to move the cursor to the end of the command line.
### Juniper Junos OS
- 
### Fortinet FortiOS
- 
