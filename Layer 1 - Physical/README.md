# Layer 1 - Physical

## Overview
The Physical Layer (Layer 1) defines the electrical, optical, and mechanical characteristics of the transmission medium. It converts digital frames into signals—electrical voltages, light pulses, or radio frequencies—suitable for propagation across copper cabling, fiber optic strands, or wireless spectrum. This layer specifies physical connectors, pinouts, signaling rates, and line coding schemes, while devices such as repeaters and hubs regenerate signals to extend physical reach. This section focuses on hardware connectivity, signaling standards, and interface configuration.

# Labs

<table>
  
  
  
  <tr>
    <th>
      Name
    </th>
    <th>
      Type
    </th>
    <th>
      Concepts
    </th>
    <th>
      Simulator
    </th>
    <th>
      Vendors
    </th>
    <th>
      Key Demonstrations
    </th>
  </tr>
  <tr>
    <td align="center">
        <a href="/Layer%201%20-%20Physical/Physical-Connectivity-and-Interface-State">
          Physical Connectivity and Interface State
        </a>
    </td>
    <td>
      Troubleshooting
    </td>
    <td>
      Power State Verification, Cable Integrity Assessment, Administrative Status Validation
    </td>
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
    <td>
      Restored network connectivity by identifying and resolving a powered-off switch, disconnected cable, and administratively down interface.
    </td>
  </tr>
  
  
  
  <tr>
    <th height="25" align="left" colspan="6"></th>
  </tr>
  
  

  <tr>
    <th>
      Name
    </th>
    <th>
      Type
    </th>
    <th>
      Concepts
    </th>
    <th>
      Simulator
    </th>
    <th>
      Vendors
    </th>
    <th>
      Key Demonstrations
    </th>
  </tr>
  <tr>
    <td align="center">
      <a href="/Layer%201%20-%20Physical/Interface-Speed-and-Link-Establishment">
        Interface Speed and Link Establishment
      </a>
    </td>
    <td>
      Troubleshooting
    </td>
    <td>
      Link Failure Assessment, Speed Mismatch Analysis, Configuration Consistency Validation
    </td>
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
    <td>
      Re-established interswitch connectivity by identifying and correcting a speed mismatch introduced during hardware replacement.
    </td>
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
