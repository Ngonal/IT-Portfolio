# Provisioning: Variable Length Subnetting and Reachability

## Lab File

<table align="center">
  <tr>
    <td align="center" style="padding: 15px;">
      <b>📦 Lab Environment</b><br>
      <sub>Cisco Packet Tracer</sub>
      <br>
      <sub>Lab Author ~ David Bombal</sub><br><br>
      <a href="https://github.com/Ngonal/IT-Portfolio/raw/main/Layer%203%20-%20Network/Variable-Length-Subnetting-and-Reachability/Variable-Length-Subnetting-and-Reachability.pkt">
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
        <b>📋 Scenario:</b> A new site requires an additional subnet carved from the previously allocated 192.168.1.0/24 address space. One of the existing /26 subnets must be subnetted into the maximum number of subnets supporting at least 8 hosts each. The last of those subnets must then be further subnetted into /30s to accommodate point-to-point links while conserving address space.
      </th>
    </tr>
  </table>
</p>

### Entries
| # | Notes | Action Taken | Result | Image |
|:---:|:---|:---|:---|:---:|
| 1 | The network diagram reflects a partially updated topology | Subnetted 192.168.1.0/24 into four equal /26 subnets by borrowing two host bits: 192.168.1.0/26, 192.168.1.64/26, 192.168.1.128/26, 192.168.1.192/26 — labeled each subnet and interface accordingly | Network diagram updated to reflect the new addressing scheme | <img src="Elements/step1.png"> |
| 2 | After assigning IP addresses to `R1`'s `Gi0/0/0` and `Se0/1/0` via `ip address <IP address> <IP subnet mask>`, both links remain down — `show ip interface brief` confirms that these interfaces are administratively disabled | Assigned IP addresses and issued `no shutdown` on both interfaces; repeated procedure for `R2` and `R3` | All interfaces assigned IP addresses within their respective subnets; all links active and OSPF adjacencies formed between routers according to Syslog messages | <img src="Elements/step2.png"> |
| 3 | Testing connectivity from `PC5` to remote hosts and servers across both sites | Tested communication using `ping` via Windows Command Prompt | Communication successful — `write` executed to save configuration state on all updated devices | <img src="Elements/step3.png"> |
| 4 | Application Layer connectivity not yet verified | Visited Cisco.com via web browser | HTTP response received successfully — Application Layer confirmed operational | <img src="Elements/step4.png"> |

### Conclusion
The provisioning tasks required to establish inter-network connectivity were completed in the following order:
1. **Subnetting:** 192.168.1.0/24 subdivided into four equal /26 subnets and network diagram amended
2. **Addressing:** IP addresses assigned to all router interfaces within their respective subnets
3. **Activation:** Administratively down interfaces brought up with `no shutdown`
---

<p align="center">
  <a href="../../README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">🔙 Return</a> &nbsp;
</p>
