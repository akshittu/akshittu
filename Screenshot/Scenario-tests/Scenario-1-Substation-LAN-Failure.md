# Scenario 1 — Substation LAN Failure

## Test Objective

Verify that selecting Substation LAN Failure updates the Ignition Perspective architecture dashboard to display the affected network asset and the associated simulated impact.

## Observed Results

- **Scenario ID:** 1
- **Current Cyber Scenario:** Substation LAN Failure
- **Affected Asset:** Substation LAN
- **Displayed Impact:** Loss of Operational Communications
- **Substation LAN Status:** FAILED
- **PLC/RTU Status:** OFFLINE
- **Other Displayed Assets:** The remaining indicators retain their displayed states as shown in the test screenshot.

## Assessment

The dashboard reflects the selected Substation LAN Failure scenario by showing the Substation LAN as failed and the PLC/RTU as offline. The scenario panel identifies the Substation LAN as the affected asset and displays the impact as Loss of Operational Communications.

## Evidence and Limitations

This record documents the visible behaviour of the Ignition Perspective demonstrator. It does not establish that an actual network outage occurred or that live network traffic or communication failures were detected.

Attach or link the corresponding Scenario 1 screenshot when it has been uploaded to the repository.

## Screenshot Evidence

![Scenario 1 — Substation LAN Failure](https://github.com/akshittu/akshittu/blob/main/Screenshot/Scenario-tests/Scenario-1-Substation-LAN-Failure.png)

*The dashboard shows the Substation LAN in a FAILED state and the PLC/RTU OFFLINE, with the displayed impact identified as Loss of Operational Communications.*
