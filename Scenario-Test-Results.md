# Scenario-Based Test Results

## 1. Project Context

This report records observations from the Purdue-based injection substation OT/SCADA monitoring demonstrator developed in Ignition Designer using Perspective.

## 2. Test Results

| ID | Scenario | Affected Asset | Displayed Impact | Observed Result |
|---:|---|---|---|---|
| 0 | Normal Operation | None | No Impact | All displayed indicators green; devices online; Substation LAN healthy. |
| 1 | Substation LAN Failure | Substation LAN | Loss of Operational Communications | Substation LAN shows FAILED; PLC/RTU shows OFFLINE. |
| 2 | Historian Failure | Historian | Loss of Historical Data Recording | OT Historian shows OFFLINE; Substation LAN remains healthy. |
| 3 | OT Firewall Failure | OT Firewall | OT Boundary Degraded | OT Firewall shows OFFLINE; Bay Control IED remains ONLINE. |
| 4 | Enterprise Firewall Failure | Enterprise Firewall | IT/OT Boundary Degraded | IT Firewall shows OFFLINE; OT Firewall and Bay Control IED remain ONLINE after correction. |
| 5 | IED Failure | Protection IED | Reduced Protection Visibility | Protection IED shows OFFLINE; GOOSE label remains static and displays HEALTHY. |

## 3. Findings

- The scenario selector updates the displayed scenario, affected asset, and impact description.
- Scenario-dependent status indicators change to represent the selected simulated condition.
- Scenario 3 represents an OT Firewall failure without automatically marking the Bay Control IED offline.
- Scenario 4 was corrected so the Bay Control IED remains online during Enterprise Firewall Failure.
- The IEC 61850 GOOSE status is currently a static architecture label, not a live communication-health measurement.

## 4. Scope and Limitations

These results document visible behaviour in the Ignition demonstrator. They do not prove that real network failures are detected, that industrial protocols are exchanging live traffic, or that cybersecurity controls have been validated against actual attacks.

Actual protocol integration, packet capture and analysis, and controlled cybersecurity experiments remain future development activities unless separately implemented and tested.

## 5. Recommended Follow-Up

1. Recheck all six scenarios after switching between them.
2. Verify the tag or expression dependencies for each status indicator.
3. Decide whether GOOSE will remain a static annotation, become a simulated status, or eventually be supported by protocol-level observations in an isolated lab.
4. Record screenshots and unexpected results as test evidence.
