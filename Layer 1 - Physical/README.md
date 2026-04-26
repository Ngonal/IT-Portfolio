# Layer 1 - Physical

## Overview
The Physical Layer (Layer 1) defines the electrical, optical, and mechanical characteristics of hardware and transmission media used for data transfer and, where applicable, power delivery. It converts digital data into signals — electrical voltages, light pulses, or radio frequencies — suitable for transmission across copper cabling, fiber-optic media, or wireless spectrum. This layer specifies cables, connectors, pinouts, signaling rates, and line coding schemes. Devices such as repeaters and hubs operate at this layer, regenerating signals to extend transmission distance. Overall, the Physical Layer focuses on hardware connectivity, signaling standards, and interface configuration.

## Examples
<table>
  <tr>
      <th colspan="6"><b>Maintenance</b></th>
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
      Environment
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
        <a href="">
        </a>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="40">
      </a>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="40">
      </a>
    </td>
    <td>
    </td>
  </tr>

  <tr>
    <th height="50" align="left" colspan="6"></th>
  </tr>

  <tr>
      <th colspan="6">Maintenance</th>
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
      Environment
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
        <a href="">
        </a>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="40">
      </a>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="40">
      </a>
    </td>
    <td>
    </td>
  </tr>

  <tr>
    <th height="50" align="left" colspan="6"></th>
  </tr>

  <tr>
      <th colspan="6">Troublshooting</th>
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
      Environment
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
        <a href="Physical-Connectivity-and-Interface-Status">
          Physical Connectivity and Interface Status
        </a>
    </td>
    <td>
      Troubleshooting
    </td>
    <td>
      Power State Verification, Cable Integrity Assessment, Interface Status Validation
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
      Restored network connectivity after diagnosing and resolving a powered-off switch, a cable disconnected by an end user, and disabled interface.
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
      Environment
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
      <a href="Interface-Speed-and-Link-Establishment">
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
### Windows (CMD / Powershell CLI)
- 
### Linux (Bash CLI)
- 
### Cisco (IOS / IOS XE CLI)
- **`shutdown`** — Changes the administrative state of an interface. `shutdown` disables the interface, placing the link status into an `administratively down` state and preventing any Layer 1 or Layer 2 activity. `no shutdown` enables the interface, allowing it to attempt link establishment.
- **`show ip interface brief`** — Displays a concise summary of all interfaces including switchports, routed ports, and virtual interfaces—showing their IP addresses, link status (Layer 1), and line protocol (Layer 2). Useful for quickly assessing interface status regardless of interface type.
- **`show interfaces status`** — Provides a high-level overview of all switchports, including VLAN membership, duplex and speed settings, and link status.
### Juniper (Junos OS CLI)
- 
### Fortinet (FortiOS CLI)
- 

---

<p align="center">
  <a href="../README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../Layer%202%20-%20Data%20Link/">📁 Layer 2 - Data Link</a> &nbsp;|&nbsp;
  <a href="../Layer%203%20-%20Network/">📁 Layer 3 - Network</a> &nbsp;|&nbsp;
  <a href="../Layer%204%20-%20Transport/">📁 Layer 4 - Transport</a> &nbsp;|&nbsp;
  <a href="../Layer%205%20-%20Application/">📁 Layer 5 - Application</a>
</p>
