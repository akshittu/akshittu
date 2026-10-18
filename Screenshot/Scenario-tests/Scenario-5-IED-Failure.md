# Scenario 5 — IED Failure

## Test Objective

Verify that selecting IED Failure updates the Ignition Perspective architecture dashboard to identify the affected asset and display the associated simulated impact.

## Observed Results

- **Scenario ID:** 5
- **Current Cyber Scenario:** IED Failure
- **Affected Asset:** Protection IED
- **Displayed Impact:** Reduced Protection Visibility
- **Protection IED Status:** OFFLINE
- **GOOSE Status Label:** HEALTHY (static architecture label)

## Assessment

The dashboard reflects the selected IED Failure scenario by showing the Protection IED as offline and displaying the impact as Reduced Protection Visibility.

The GOOSE status label remains HEALTHY because it is currently static. It does not represent live IEC 61850 GOOSE communication monitoring.

## Evidence and Limitations

This record documents the visible behaviour of the Ignition Perspective demonstrator. It does not establish that an actual IED failed, that GOOSE messages were transmitted or received, or that live industrial communications were monitored.

## Future Development

Potential future work includes introducing a clearly labelled simulated GOOSE status and, later, exploring actual IEC 61850 GOOSE traffic capture and analysis in an isolated lab. These capabilities are not currently implemented.
