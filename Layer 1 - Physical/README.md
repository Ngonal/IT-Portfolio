# Layer 1 - Physical

## Overview
The Physical Layer (Layer 1) defines the electrical, optical, and mechanical characteristics of the transmission medium. It converts digital frames into signals—electrical voltages, light pulses, or radio frequencies—suitable for propagation across copper cabling, fiber optic strands, or wireless spectrum. This layer specifies physical connectors, pinouts, signaling rates, and line coding schemes, while devices such as repeaters and hubs regenerate signals to extend physical reach. This section focuses on hardware connectivity, signaling standards, and interface configuration.

# Labs

<table>
  <tr>
    <th align="left" colspan="6">
      <b>🖥 Lab Name:</b>
      <a href="/Layer%201%20-%20Physical/Outage-Unpowered-Switching-Device">
        Outage: Unpowered Switching Device
      </a>
    </th>
  </tr>
  
  <tr>
    <th align="left" colspan="6">
      <b>📋 Scenario:</b> Two hosts connected to a common Layer 2 device are unable to communicate with each other. The device exhibits no link-layer connectivity, and all interface LEDs on the switching device are dark—suggesting an absence of electrical power.
    </th>
  </tr>
  
  <tr>
    <th>Type</th>
    <th>Technologies</th>
    <th>Simulator</th>
    <th>Vendors</th>
    <th>Key Demonstrations</th>
  </tr>
  <tr>
    <td align="center">Troubleshooting</td>
    <td>Physical Layer, Cabling, Interface State</td>
    <td align="center">
      <a href="https://www.netacad.com/resources/lab-downloads" target="_blank" rel="noopener noreferrer">
        <img src="../README%20Elements/Cisco-Packet-Tracer-logo.png" width="40">
      </a>
    </td>
    <td align="center">
      <a href="https://www.cisco.com/" target="_blank" rel="noopener noreferrer">
        <img src="../README%20Elements/Cisco-logo.png" width="40">
      </a>
    </td>
    <td>Restored network connectivity through methodical Layer 1 diagnostics.</td>
  <tr>
    <th height="100" align="left" colspan="6"></th>
  </tr>
</table>


## Common Commands
### Cisco IOS / IOS XE
- **`shutdown`**  
Changes the administrative state of an interface. `shutdown` disables the interface, placing it in `administratively down` status and preventing any Layer 1 or Layer 2 activity. `no shutdown` enables the interface, allowing it to attempt link establishment.
- **`show ip interface brief`**  
Displays a concise summary of all interfaces—including switchports, routed ports, and virtual interfaces—showing their IP addresses, administrative status (Layer 1), and protocol status (Layer 2). Useful for quickly assessing interface operational state regardless of interface type.
- **`show interfaces status`**  
Provides a high-level overview of all switchports, including VLAN membership, duplex and speed settings, link status, and whether the port is in an errdisabled state. Primarily used on access layer switches for Layer 1 and Layer 2 verification.
### Juniper Junos OS
- 
### Fortinet FortiOS
- 

---

<p align="center">
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/Layer%202%20-%20Data%20Link/">📁 Layer 2 - Data Link</a> &nbsp;|&nbsp;
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/Layer%203%20-%20Network/">📁 Layer 3 - Network</a> &nbsp;|&nbsp;
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/Layer%204%20-%20Transport/">📁 Layer 4 - Transport</a> &nbsp;|&nbsp;
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/Layer%205%20-%20Application/">📁 Layer 5 - Application</a>
</p>
