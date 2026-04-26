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

## Action Log
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

### Notes
| Entry # | Observations & Remarks | Action Taken | Result | Image |
|:---:|:---|:---|:---|:---:|
| 1 | The network diagram reflects a partially updated topology | Subnetted 192.168.1.0/24 into four equal /26 subnets by borrowing two host bits: 192.168.1.0/26, 192.168.1.64/26, 192.168.1.128/26, 192.168.1.192/26 — labeled each subnet and interface accordingly | Network diagram updated to reflect the new addressing scheme | <img src="Elements/step1.png"> |
| 2 | Assigning IP addresses to `R1`'s `Gi0/0/0` and `Se0/1/0` reveals both interfaces are administratively down — `show interfaces` confirms this | Issued `no shutdown` on both interfaces; repeated procedure for `R2` and `R3` | All interfaces assigned IP addresses within their respective subnets; all links active and OSPF adjacencies formed between routers according to SYSLOG messages | <img src="Elements/step2.png"> |
| 3 | Testing connectivity from `PC5` to remote hosts and servers across both sites | Tested with `ping` via Windows Command Prompt | Communication successful — issued `write` on all updated devices to save configuration | <img src="Elements/step3.png"> |
| 4 | Layer 7 connectivity not yet verified | Visited Cisco.com via web browser | HTTP response received successfully — Application Layer confirmed operational | <img src="Elements/step4.png"> |

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
