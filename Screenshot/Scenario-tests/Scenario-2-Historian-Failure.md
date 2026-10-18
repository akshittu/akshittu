# Scenario 2 — Historian Failure

## Test Objective

Verify that selecting Historian Failure updates the Ignition Perspective architecture dashboard to identify the affected asset and display the associated simulated impact.

## Observed Results

- **Scenario ID:** 2
- **Current Cyber Scenario:** Historian Failure
- **Affected Asset:** Historian
- **Displayed Impact:** Loss of Historical Data Recording
- **OT Historian Status:** OFFLINE
- **Substation LAN Status:** HEALTHY
- **Other Displayed Assets:** The remaining indicators retain their displayed states as shown in the test screenshot.

## Assessment

The dashboard reflects the selected Historian Failure scenario by showing the OT Historian as offline while the Substation LAN remains healthy. The scenario panel identifies the Historian as the affected asset and displays the impact as Loss of Historical Data Recording.

## Evidence and Limitations

This record documents the visible behaviour of the Ignition Perspective demonstrator. It does not establish that an actual historian service failure occurred or that live industrial systems were monitored.

Attach or link the corresponding Scenario 2 screenshot when it has been uploaded to the repository.

## Screenshot Evidence

![Scenario 2 — Historian Failure](https://github.com/akshittu/akshittu/blob/main/Screenshot/Scenario-tests/Scenario-2-Historian-Failure.png)

*The dashboard shows the OT Historian OFFLINE while the Substation LAN remains healthy, with the displayed impact identified as Loss of Historical Data Recording.*
