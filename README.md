# OT/SCADA Cybersecurity Demonstrator

### Purdue-Based Injection Substation Architecture and Scenario-Driven Monitoring

**Electrical Power Engineering | Project Management | ICS/OT Cybersecurity**

## Project Overview

This project is a simulated OT/SCADA monitoring demonstrator developed using Ignition Designer and Perspective. It combines a Purdue Model-based injection substation architecture with backend tag-driven visualisation, selectable infrastructure-failure scenarios, alarm behaviour, and trend charts.

The project applies my power engineering background to the exploration of industrial control system monitoring, infrastructure availability, and operational awareness.

The demonstrator provides a visual representation of selected enterprise IT and OT components, industrial control devices, and electrical process assets. Backend tag values drive the corresponding status indicators in the Perspective interface.

**Project status:** Working lab demonstrator under development. Six selectable scenarios have been exercised, and alarm behaviour and trend charts have been tested. Further technical documentation, validation, and cybersecurity analysis remain ongoing.

## Project Objectives

- Apply a Purdue Model-based architecture to an electrical injection substation use case.
- Represent enterprise IT, the OT DMZ, site operations, supervisory control, basic control, and the electrical process.
- Use Ignition tags and configured bindings to drive visual asset-status indicators.
- Demonstrate six selectable operating and infrastructure-failure scenarios.
- Test alarm behaviour and trend-chart functionality in the lab.
- Explore how simulated infrastructure states can improve operator visibility and support investigation.
- Establish a foundation for further practical ICS/OT cybersecurity development.

## Architecture Overview

![Purdue-based injection substation OT architecture](./Purdue%20Injection%20Substation%20Architecture.png)

**Figure 1 — Purdue-Based Injection Substation Architecture: Substation LAN Failure Scenario**

This screenshot shows the Ignition Perspective monitoring interface with the Substation LAN Failure scenario selected. Backend tag values drive the displayed status indicators, showing how the OT architecture represents a simulated infrastructure failure. The screenshot documents the selected scenario state; it does not, by itself, demonstrate a real network outage or independently validated cybersecurity controls.

The architecture represents the following Purdue levels and example components.

| Purdue level                  | Representative components                                                 |
| ----------------------------- | ------------------------------------------------------------------------- |
| Level 4 — Enterprise IT       | Active Directory server, SIEM, enterprise network and enterprise firewall |
| Level 3.5 — OT DMZ            | Jump server, remote access gateway, data exchange server and OT firewall  |
| Level 3 — Site Operations     | Engineering workstation and OT historian                                  |
| Level 2 — Supervisory Control | Ignition SCADA/HMI and operator workstation                               |
| Level 1 — Basic Control       | PLC/RTU, bay control IED and protection IED                               |
| Level 0 — Process             | 33 kV and 11 kV breakers, transformers, frequency and bus voltage         |

The architecture illustrates the separation of enterprise, operations, control, and process functions. It also identifies representative trust boundaries and communication paths for further OT security analysis.

The diagram conceptually represents the lab architecture. It does not imply that every illustrated component is a separate deployed system or that the depicted network segmentation has been independently validated.

## Demonstrator Screenshots

The following screenshots illustrate the current Ignition Perspective implementation and its monitoring capabilities.

### 1. Substation Overview Dashboard

![Substation Overview Dashboard](Images/Overview-Dashboard.png)

The overview presents a simulated injection substation, including electrical measurements, breaker states, transformer information, system status, and selected scenario indicators.

### 2. Alarm Overview Dashboard

![Ignition Perspective Alarm Overview Dashboard](Images/Alarm-Dashboard.png)

The alarm dashboard presents configured alarm sources, their displayed status, and severity. Alarm behaviour has been tested within the lab environment.

### 3. OT Cybersecurity Dashboard

![OT Cybersecurity Dashboard](Images/Cyber-Dashboard.png)

The cyber dashboard provides a visual representation of selected asset status and health indicators, including the PLC, Gateway, historian, and firewall.

### 4. Substation Trend Dashboard

![Substation Trend Dashboard](Images/Trend-Dashboard.png)

The trend dashboard displays selected electrical measurements, including 33 kV voltage, frequency, power factor, and current over a selected time range. Trend-chart functionality has been tested in the lab.

**Evidence scope:** These screenshots document the current visual implementation. The demonstrator uses backend tag-driven scenario states. Industrial protocol integrations, packet-level attack analysis, and associated detection controls will be documented separately when implemented and tested.

## Technology Stack

- **SCADA/HMI:** Ignition Designer and Perspective.
- **Backend state:** Ignition tags.
- **Visualisation:** Perspective components and configured tag bindings.
- **Monitoring:** Asset-status indicators, alarm behaviour and trend charts.
- **Test environment:** Simulated injection substation and infrastructure states.

## Scenario-Based Monitoring

The demonstrator implements six selectable scenarios identified by numeric values from 0 to 5. Each scenario has been selected and observed changing the backend-driven display.

| ID | Scenario                    | Demonstration objective                                                              |
| -: | --------------------------- | ------------------------------------------------------------------------------------ |
|  0 | Normal Operation            | Display the baseline state of the simulated environment.                             |
|  1 | Substation LAN Failure      | Represent a substation network failure through the relevant visual status indicator. |
|  2 | Historian Failure           | Represent an OT historian failure in the selected scenario.                          |
|  3 | OT Firewall Failure         | Represent an OT firewall failure.                                                    |
|  4 | Enterprise Firewall Failure | Represent an enterprise firewall failure.                                            |
|  5 | IED Failure                 | Represents a failure affecting an intelligent electronic device.                      |

### Backend-Driven Visualisation

The scenario selection changes backend tag values, which are consumed by configured Perspective bindings to update the visual display.

For example, selecting Scenario 1 — Substation LAN Failure displays a red failure indicator for the relevant network element.

This demonstrates scenario-driven state visualisation in the lab. The precise effect of each scenario on other assets, communication paths, and alarms should be assessed individually rather than assumed from the selected scenario alone.

## Alarm and Trend Monitoring

Alarm behaviour and trend-chart functionality have been tested in the lab environment.

These features support exploration of how changes in simulated operating conditions can be presented to an operator through alarms and time-series visualisation.

Further development will document the configured alarm conditions, tag dependencies, trend data sources, test procedures, and observed results in greater detail.

## Industrial Communication Technologies

The architecture identifies the following industrial communication technologies as relevant design concepts:

- IEC 61850 MMS and GOOSE.
- OPC UA.
- Modbus/TCP.
- DNP3.

These technologies are represented as architecture labels or design concepts. Their inclusion does not imply that the demonstrator has generated, captured, analysed, or integrated protocol traffic.

We will document practical protocol experiments and associated evidence separately as we complete them.

## ICS/OT Cybersecurity Learning Outcomes

This project provides a practical foundation for exploring:

- Purdue Model-based OT architecture.
- Industrial asset visibility and status representation.
- Backend tag-driven monitoring.
- Scenario-based fault visualisation.
- Alarm behaviour and trend monitoring.
- Infrastructure availability and operational dependencies.
- OT network segmentation and trust boundaries as architectural concepts.
- The distinction between monitoring simulated states and detecting real cyber threats.

The current demonstrator focuses on visual monitoring of simulated infrastructure conditions. It is not, by itself, a network intrusion detection system and does not establish the effectiveness of cybersecurity controls.

## Current Status and Future Development

### Implemented and Tested

- Purdue-based injection substation architecture layout.
- Ignition Perspective monitoring interface.
- Backend tag-driven visual status indicators.
- Six selectable scenarios, with observed changes to the backend-driven display.
- Alarm behaviour testing.
- Trend-chart testing.

### Planned Development

- Document individual scenario test procedures and observed results.
- Verify and document the effect of each scenario on relevant assets and alarms.
- Capture screenshots of the working dashboard and scenario states.
- Develop practical IEC 61850 GOOSE traffic analysis.
- Explore industrial protocol analysis and OT network visibility in an isolated lab.
- Document defensive recommendations for segmentation, controlled access, monitoring, and incident response.
- Expand the demonstrator as further features are implemented and validated.

## Professional Background

I am an electrical power engineering and project management professional with more than 15 years of experience in the power sector. I am developing practical ICS/OT cybersecurity capabilities, with a particular interest in industrial control systems, SCADA, industrial communications, and the protection of critical electrical infrastructure.

My goal is to combine power-sector operational knowledge with cybersecurity skills to contribute to the security, resilience, and safe operation of industrial environments.

## Disclaimer

This project is intended for education, technical demonstration, and professional development. All scenarios are simulated in a lab environment and do not represent faults or cyber incidents on a live electrical network.

The presence of a component, architecture label, alarm, or status indicator does not establish that the associated production system or cybersecurity control has been deployed or independently validated.
