# Layer 1 Outage: Unpowered Switching Device

## Diagnosis Log

| Step | Observation | Action Taken | Result |
|:---|:---|:---|:---|
| 1 | One cable is disconnected from `Fa0/1` | Reconnected cable to `Fa0/1` | No change; switch LEDs remain unilluminated |
| 2 | Switch power switch is in the **OFF** position | Toggled power switch to **ON** | Some LEDs illuminate; `Fa0/1` remains dark |
| 3 | `Fa0/1` is administratively down | Issued `no shutdown` on interface | Port LED illuminates; link established |
| 4 | Both hosts have link connectivity | Tested with `ping` | Communication successful |

## Resolution
The root cause was a combination of Layer 1 failures:
1. **Physical:** Disconnected cable and unpowered switch
2. **Administrative:** Interface in `shutdown` state

All three conditions required correction to restore full connectivity.