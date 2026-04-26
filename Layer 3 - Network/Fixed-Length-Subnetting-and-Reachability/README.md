# Provisioning: Fixed Length Subnetting and Reachability

## Lab File

<table align="center">
  <tr>
    <td align="center" style="padding: 15px;">
      <b>📦 Lab Environment</b><br>
      <sub>Cisco Packet Tracer</sub><br><br>
      <a href="https://github.com/Ngonal/IT-Portfolio/raw/main/Layer%201%20-%20Physical/Physical-Connectivity-and-Interface-Status/Physical-Connectivity-and-Interface-Status.pkt">
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
          <img src="Elements/step0.png" border="1">
      </td>
    </tr>
    <tr>
      <th align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <b>📋 Scenario:</b> Network engineers have deployed new infrastructure connecting two sites through a central router topology and subdivided the 192.168.1.0/24 network into four equal-sized subnets. The network diagram requires updated subnet labeling, and router interfaces need IP address assignments within their respective subnets to establish inter-network connectivity.
      </th>
    </tr>
  </table>
</p>


### Steps
| Step | Observation | Action Taken | Result | Image |
|:---:|:---|:---|:---|:---:| 
| 1 | Upon closer inspection, we can see that the Network Diagram has been partially updated to reflect updates | Subnetted the 192.168.1.0/24 network into 4 subnets after borrowing two of the original host bits: 192.168.1.0/26, 192.168.1.64/26, 192.168.1.128/26, 192.168.1.192/26 — proceeded to respectively label each network and interface | Network Diagram now updated to appropriately reflect changes | <img src="Elements/step1.png"> |
| 2 | Proceeding to assign first and last usable IP addresses to the designated interfaces of every Router using the `ip address <IP address> <IP subnet mask>` starting with `R1`'s `Gi0/0/0` and `Se0/1/0`, we can see that the links remain down | After viewing the status of the respective interfaces, we can see that the routed ports of `R1` are administratively disabled — we enable them and the links are now up; we proceed to perform the same procedure for Routers `R3` and `R2` | All interfaces now assigned appropriate Ip addresses within their respective subnets; all links active and all routers have formed OSPF adjancencies with eachother | <img src="Elements/step2.png"> |
| 3 | Connecting to the device's CLI terminal through the console port and using the `show ip interface brief` command to check interface status reveals that `Fa0/1`'s link status is administratively down | Issued `no shutdown` on interface | Link status and line protocol are up/up — the port LED is illuminated, indicating that a link has been successfully established. | <img src="Elements/step3.png"> |
| 4 | Both hosts appear to have link connectivity according to their blinking interface LEDs | Tested communication using `ping` via Windows Command Prompt | Communication successful — `write` executed to save configuration state on all updated devices. | <img src="Elements/step4.png"> |

### Conclusion
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** `shutdown` applied to interface

All three conditions required correction to restore full connectivity.

## Bonus Tips
### Tip #1 - The `show ip interface brief` command provides a quick health check of all interfaces. For diagnosing Layer 1 issues, check the link status and line protocol columns:
- **Administratively Down / Down** — Interface is disabled with `shutdown` command
- **Down / Down** — Possible causes include an absent or damaged cable, improperly seated connectors, incorrect cable type or pinout, or a local/remote interface or device that is powered off, misconfigured, or faulty.

<p align="center">
  <table align="center">
    <tr>
      <td align="center">
        <img width="800" src="Elements/bonus1.png" border="1">
      </td>
    </tr>
    <tr>
      <th width="800" align="left" colspan="6" style="padding: 10px 12px; background-color: #eaeef2; border-bottom: 1px solid #d0d7de; text-align: left;">
        <i>Example: Despite issuing `no shutdown`, interface Fa0/1 remains in a down/down state because the cable is disconnected</i>
      </th>
    </tr>
  </table>
</p>

> 💡 **Quick Tip(s):**  When a link fails to establish, the fault lies in the cable, local device, remote device, or **any of their respective interfaces**. Start at Layer 1 and work up:
> 
> **Without specialized test equipment:**
> - Verify both cable ends are firmly seated
> - If still down → Replace with known-good cable
>   - If link comes up → Original cable was faulty
>   - If link stays down → Investigate devices and/or interfaces
> 
> **With TDR/OTDR (copper/fiber cable testers):**
> - Run TDR/OTDR first to detect opens, shorts, or impedance faults
>   - Most modern cable testers include built-in TDR/OTDR; some switches/routers have diagnostic commands
>   - If fault detected → Reseat both ends, then replace cable if issue persists
>   - If clean results (proper termination, no faults) → Skip cable replacement and go directly to device/interface investigation
>
> **Device/interface investigation:**
> - Check speed/duplex settings, admin status, configuration mismatches, and hardware failures on both ends

---

<p align="center">
  <a href="../../README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">🔙 Return</a> &nbsp;
</p>
