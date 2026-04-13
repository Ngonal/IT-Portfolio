# Layer 1 - Physical

## Core Function
Defines the electrical, optical, and mechanical characteristics of the transmission medium. It converts digital frames into signals—electrical voltages, light pulses, or radio frequencies—suitable for propagation across copper cabling, fiber optic strands, or wireless spectrum. This layer specifies physical connectors, pinouts, signaling rates, and line coding schemes, while devices such as repeaters and hubs regenerate signals to extend physical reach.

## Overview
The Physical Layer defines the electrical, mechanical, and procedural specifications for transmitting raw bits over a physical medium. This section focuses on hardware connectivity, signaling standards, and interface configuration.

# Labs
<div align="center">

| Lab Name | Type | Technologies | Key Demonstrations | Scenario | Simulator/Emulator | Vendors |
|:---|:---|:---:|:---:|:---:|:---:|:---:|
| [Layer 1 Outage: Unpowered Switching Device](/Layer%201%20-%20Physical/Layer%201%20Outage:%20Unpowered%20Switching%20Device) | Troubleshooting | Physical Layer, Cabling, Interface State | Restored network connectivity through methodical Layer 1 diagnostics and interface state remediation. | Two hosts attempting communications are connected to a common Layer 2 device that exhibits no link-layer connectivity. All interface LEDs on the switching device are dark, suggesting an absence of electrical power. | <img src="../README%20Elements/Cisco-Packet-Tracer-logo.png" width="40"> | <img src="../README%20Elements/Cisco-logo.png" width="40"> |

</div>

## Common Commands
### Cisco IOS / IOS XE
- **`shutdown`**  
Changes the administrative state of an interface. `shutdown` disables the interface, placing it in `administratively down` status and preventing any Layer 1 or Layer 2 activity. `no shutdown` enables the interface, allowing it to attempt link establishment.
- **`show ip interface brief`**  
Displays a concise summary of all interfaces, including their IP addresses, administrative status (Layer 1), and protocol status (Layer 2). On switches, this includes both physical switchports (showing `unassigned` for the IP field) and SVIs. Useful for quickly identifying interface operational state regardless of interface type.
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
