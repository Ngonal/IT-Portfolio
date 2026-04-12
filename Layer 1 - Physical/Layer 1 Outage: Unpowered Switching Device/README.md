# Layer 1 Outage: Unpowered Switching Device
## Description
Two hosts are connected to a common Layer 2 device but exhibit no link-layer connectivity. All interface LEDs on the switching device are dark, suggesting an absence of electrical power. Troubleshooting focuses on power sourcing, cabling integrity, and hardware failure indicators.

## Log
### Initial State
<kbd>
  <img src="Elements/Step0.png">
</kbd>

### Steps
| Step | Observation | Action Taken | Result | Image |
|:---|:---|:---|:---|:---:| 
| 1 | One cable is disconnected from `Fa0/1` | Reconnected cable to `Fa0/1` | No change; switch LEDs remain unilluminated | <img src="Elements/Step1.png"> |
| 2 | Switch power switch is in the **OFF** position | Toggled power switch to **ON** | Some LEDs illuminate; `Fa0/1` remains dark | <img src="Elements/Step2.png"> |
| 3 | `Fa0/1` is administratively down | Issued `no shutdown` on interface | Port LED illuminates; link established | <img src="Elements/Step3.png"> |
| 4 | Both hosts have link connectivity | Tested with `ping` | Communication successful | <img src="Elements/Step4.png"> |

---

## Interface Status Verification

The `show ip interface brief` command provides a quick health check of all interfaces. A status of **`down/down`** indicates a Layer 1 issue:

- **Administratively Down / Down** — Interface is disabled with `shutdown` command
- **Down / Down (with cable connected)** — Possible faulty cable, incorrect cable type, or defective interface
- **Down / Down (no cable)** — No physical connection detected

> 💡 **Quick Tip:** To isolate whether the issue is the cable or the interface, swap with a **known-good cable**:
> - If the link comes up → Original cable was faulty
> - If the link remains down → Interface or connected device may be defective

<kbd>
  <img src="Elements/Bonus.png" border="1">
</kbd>

<p align="center">
  <i>Example: Fa0/1 showing "down/down" status prior to issuing `no shutdown`</i>
</p>

---

## Results
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** Interface in `shutdown` state

All three conditions required correction to restore full connectivity.

---

<p align="center">
  <a href="https://github.com/Ngonal/Computer-Networking-Lab-Portfolio/blob/main/README.md">🏠 Home</a> &nbsp;|&nbsp;
  <a href="../">🔙 Return</a> &nbsp;
</p>
