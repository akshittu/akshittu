# Scenario 3 — OT Firewall Failure

## Test Objective

Verify that selecting OT Firewall Failure updates the Ignition Perspective architecture dashboard to identify the affected asset and display the associated simulated impact.

## Observed Results

- **Scenario ID:** 3
- **Current Cyber Scenario:** OT Firewall Failure
- **Affected Asset:** OT Firewall
- **Displayed Impact:** OT Boundary Degraded
- **OT Firewall Status:** OFFLINE
- **IT Firewall Status:** ONLINE
- **PLC/RTU Status:** ONLINE
- **Bay Control IED Status:** ONLINE
- **OT Historian Status:** ONLINE
- **Substation LAN Status:** HEALTHY

## Assessment

The dashboard reflects the selected OT Firewall Failure scenario by showing the OT Firewall as offline and displaying the impact as OT Boundary Degraded.

The Bay Control IED remains online. This is consistent with the intended scenario design: an OT Firewall failure does not automatically mean that the IED itself has failed.

## Evidence and Limitations

This record documents the visible behaviour of the Ignition Perspective demonstrator. It does not establish that an actual firewall failure occurred, that real network traffic was interrupted, or that live cybersecurity controls were validated.

Attach or link the corresponding Scenario 3 screenshot when it has been uploaded to the repository.
