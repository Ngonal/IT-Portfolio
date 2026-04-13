# Outage: Unpowered Switching Device

## Lab File
<table align="center">
  <tr>
    <td align="center" style="padding: 15px;">
      <b>📦 Lab Environment</b><br>
      <sub>Cisco Packet Tracer</sub><br><br>
      <a href="https://github.com/Ngonal/Networking-Lab-Portfolio/raw/main/Layer%201%20-%20Physical/Outage-Unpowered-Switching-Device/Outage-Unpowered-Switching-Device.pkt">
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
<p>
  <table>
    <tr >
      <th align="center" colspan="6" style="background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <img src="Elements/Step0.png" width="70%" border="1">
      </th>
    </tr>
    <tr>
      <th align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <b>📋 Scenario:</b> Two hosts connected to a common Layer 2 device are unable to communicate with each other. The device exhibits no link-layer connectivity, and all interface LEDs on the switching device are dark—suggesting an absence of electrical power.
      </th>
    </tr>
  </table>
</p>

### Steps
| Step | Observation | Action Taken | Result | Image |
|:---:|:---|:---|:---|:---:| 
| 1 | `SW1` is plugged into electrical outlet, verified electrical outlet is working using a known-good device (receptable tester/phone charger connected to phone), reconnected power cable to no effect, `SW1` power switch is in the **OFF** position | Toggled power switch to **ON** | `Fa0/2` LEDs illuminate; `Fa0/1` remains unlit | <img src="Elements/Step1.png"> |
| 2 | Cable connecting `PC1` to `SW1` via `Fa0/1` is disconnected | Reconnected cable to `Fa0/1` | No change; `Fa0/1` LEDs remain unilluminated | <img src="Elements/Step2.png"> |
| 3 | `Fa0/1` is administratively down | Issued `no shutdown` on interface | Port LED illuminates; link established | <img src="Elements/Step3.png"> |
| 4 | Both hosts have link connectivity | Tested with `ping` | Communication successful | <img src="Elements/Step4.png"> |

## Bonus Tips
### Tip #1 - The `show ip interface brief` command provides a quick health check of all interfaces. A status of **`down/down`** indicates a Layer 1 issue:

- **Administratively Down / Down** — Interface is disabled with `shutdown` command
- **Down / Down (with cable connected)** — Possible faulty cable, incorrect cable type, or defective interface
- **Down / Down (no cable)** — No physical connection detected

> 💡 **Quick Tip(s):** A cable connects two devices. If the link doesn't come up, the fault could be the cable, the local interface, or **the remote device on the other end**. Swap with a known-good cable first:
> - If the link comes up → Original cable was faulty
> - Link remains down → Investigate both the local port and the far-end device

<table>
  <tr >
    <th align="center" colspan="6" style="background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
      <img src="Elements/Bonus1.png" width="70%" border="1">
    </th>
  </tr>
  <tr>
    <th align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
      <i>Example: Fa0/1 showing "down/down" status after issuing `no shutdown`</i>
    </th>
  </tr>
<table>

## Conclusion
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** Interface in `shutdown` state

All three conditions required correction to restore full connectivity.

---

<p align="center">
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">🔙 Return</a> &nbsp;
</p>
