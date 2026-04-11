# Layer 1 Outage: Unpowered Switching Device
## Description
Two hosts are connected to a common Layer 2 device but exhibit no link-layer connectivity. All interface LEDs on the switching device are dark, suggesting an absence of electrical power. Troubleshooting focuses on power sourcing, cabling integrity, and hardware failure indicators.

## Diagnosis Log

| Step | Observation | Action Taken | Result | Image |
|:---|:---|:---|:---|:---:| 
| 1 | One cable is disconnected from `Fa0/1` | Reconnected cable to `Fa0/1` | No change; switch LEDs remain unilluminated | <img src="Elements/Step1.png"> |
| 2 | Switch power switch is in the **OFF** position | Toggled power switch to **ON** | Some LEDs illuminate; `Fa0/1` remains dark |
| 3 | `Fa0/1` is administratively down | Issued `no shutdown` on interface | Port LED illuminates; link established |
| 4 | Both hosts have link connectivity | Tested with `ping` | Communication successful |

## Resolution
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** Interface in `shutdown` state

All three conditions required correction to restore full connectivity.

| Layer | Example | Labs |
|:---|:---|:---|
| 5 - Application | HTTP/HTTPS, DNS, DHCP, SSH, FTP, SMTP, SSL/TLS | [View Labs](Layer%205%20-%20Application) |
| 4 - Transport | TCP, UDP, ACLs, Port Numbers, Flow Control, Error Recovery | [View Labs](Layer%204%20-%20Transport) |
| 3 - Network | IPv4, IPv6, ICMP, OSPF, BGP, Routers, Subnetting | [View Labs](Layer%203%20-%20Network) |
| 2 - Data Link | Ethernet, MAC Addressing, VLANs, STP, Switches, Bridges | [View Labs](Layer%202%20-%20Data%20Link) |
| 1 - Physical | Fiber Optics, Copper Cabling, Wi-Fi Radio, Repeaters, Hubs | [View Labs](Layer%201%20-%20Physical) |

---

<p align="center">
  <a href="../../">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">📁 Layer 1 - Physical</a> &nbsp;|&nbsp;
  <a href="./">🔧 Troubleshooting</a> &nbsp;|&nbsp;
  <b>Layer 1 Outage: Unpowered Switching Device</b>
</p>