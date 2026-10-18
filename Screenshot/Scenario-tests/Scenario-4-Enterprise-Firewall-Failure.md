# Scenario 4 — Enterprise Firewall Failure

## Test Objective

Verify that selecting Enterprise Firewall Failure updates the Ignition Perspective architecture dashboard to identify the affected asset and display the associated simulated impact.

## Observed Results

- **Scenario ID:** 4
- **Current Cyber Scenario:** Enterprise Firewall Failure
- **Affected Asset:** Enterprise Firewall
- **Displayed Impact:** IT/OT Boundary Degraded
- **IT Firewall Status:** OFFLINE
- **OT Firewall Status:** ONLINE
- **Bay Control IED Status:** ONLINE after correction
- **Substation LAN Status:** HEALTHY

## Assessment

The dashboard reflects the selected Enterprise Firewall Failure scenario by showing the IT Firewall as offline and displaying the impact as IT/OT Boundary Degraded.

The Bay Control IED remains online after the scenario logic was corrected. This avoids representing the enterprise firewall failure as an automatic failure of the IED itself.

## Evidence and Limitations

This record documents the visible behaviour of the Ignition Perspective demonstrator. It does not establish that an actual enterprise firewall failure occurred or that real network traffic or cybersecurity controls were tested.

Attach or link the corresponding Scenario 4 screenshot when it has been uploaded to the repository.
