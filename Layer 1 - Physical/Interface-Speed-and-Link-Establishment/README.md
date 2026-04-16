# Troubleshooting: Interface Speed and Link Establishment

## Lab File

<table align="center">
  <tr>
    <td align="center" style="padding: 15px;">
      <b>📦 Lab Environment</b><br>
      <sub>Cisco Packet Tracer</sub><br><br>
      <a href="https://github.com/Ngonal/Networking-Lab-Portfolio/raw/main/Layer%201%20-%20Physical/Interface-Speed-and-Link-Establishment/Interface-Speed-and-Link-Establishment.pkt">
        <kbd>⬇️ Download Lab File (.pkt)</kbd>
      </a>
    </td>
  </tr>
</table>

<p align="center">
  <sub>⚠️ The lab file is provided in its <b>initial state</b>. You may complete the objectives by following the log below or by working toward the result on your own.</sub>
</p>

## Log
### Initial State
<p align="center">
  <table align="center">
    <tr>
      <td align="center">
        <a href="https://www.netacad.com/resources/lab-downloads" target="_blank" rel="noopener noreferrer">
          <img src="Elements/Step0.png" border="1">
        </a>
      </td>
    </tr>
    <tr>
      <th align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <b>📋 Scenario:</b> Two switches were recently replaced with new hardware. Following the replacement, the interswitch link fails to establish — users on both segments lose connectivity entirely. The decommissioned switches did not exhibit this behavior.
      </th>
    </tr>
  </table>
</p>


### Steps
| Step | Observation | Action Taken | Result | Image |
|:---:|:---|:---|:---|:---:| 
| 1 | Issuing `show interfaces status` on `SW3` immediately reveals that `Gi1/0/1` has hard-coded speed of 10 Mbps, this suggests speed mismatch between switches and we can presume other switch is not using auto-negotiation as link is entirely down | Issued `speed auto` command when configuring `Gi1/0/1` interface| Link comes up but we still assume other switch operating at non-auto, hard-coded speed and need to investigate | <img src="Elements/Step1.png"> |
| 2 | Local RJ45 connector is seated in `SW1`'s `Fa0/1`, TDR device indicates a short on the far end of the link, remote end found disconnected from `PC1`'s `Fa0`, the end user reports accidental disconnection of the RJ45 connector | Reconnected cable to `PC1`'s `Fa0` | No change; `Fa0/1` LEDs remain unilluminated | <img src="Elements/Step2.png"> |

### Conclusion
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** Interface in `shutdown` state

All three conditions required correction to restore full connectivity.

## Bonus Tips
### Tip #1 - The `show ip interface brief` command provides a quick health check of all interfaces. A status of **`down/down`** indicates a Layer 1 issue:

- **Administratively Down / Down** — Interface is disabled with `shutdown` command
- **Down / Down (with cable connected)** — Possible faulty cable, incorrect cable type/pinout, or defective devices/interfaces
- **Down / Down (no cable)** — No physical connection detected (self-explanatory)

<p align="center">
  <table align="center">
    <tr>
      <td align="center">
        <a href="https://www.netacad.com/resources/lab-downloads" target="_blank" rel="noopener noreferrer">
          <img width="800" src="Elements/Bonus1.png" border="1">
        </a>
      </td>
    </tr>
    <tr>
      <th width="800" align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <i>Example: Fa0/1 showing "down/down" status after issuing `no shutdown`</i>
      </th>
    </tr>
  </table>
</p>

> 💡 **Quick Tip(s):** A cable connects two devices. If the link doesn't come up despite a physical connection, the fault could be the cable, the local device, the remote device, or **any of their respective interfaces**. Swap with a known-good cable first:
> - If the link comes up → Original cable was faulty
> - Link remains down → Investigate both devices and their interfaces on each end
> - Use a **TDR** (Time Domain Reflectometer) to quickly check for shorts or opens along the cable run — this can reveal faults on the far end without physically accessing it — Most modern cable testers include built-in TDR functionality

---

<p align="center">
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">🔙 Return</a> &nbsp;
</p>
