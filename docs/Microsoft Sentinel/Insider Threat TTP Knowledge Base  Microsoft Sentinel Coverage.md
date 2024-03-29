# Insider Threat TTP Knowledge Base - Microsoft Sentinel Coverage

It is a Python script designed to bridge a crucial gap in cybersecurity defense mechanisms, specifically in the integration between Microsoft Sentinel SIEM (Security Information and Event Management) and the MITRE ATT&CK Insider Threat TTP Knowledge Base v2. 


### Key Features

- **TTP Extraction**: Extracts TTPs directly from Microsoft Sentinel alerts, overcoming the current limitation of not having direct mappings of detection rules to MITRE ATT&CK TTPs.
- **MITRE ATT&CK Navigation Layers Generation**: Generates two distinct MITRE ATT&CK navigation layers:
    - **Covered TTPs Layer**: Showcases the TTPs of the Insider Threat TTP Knowledge Base that are covered by Microsoft Sentinel, enabling security analysts to visualize and assess the extent of their current defensive coverage.
    - **Uncovered TTPs Layer**: Highlights the TTPs that are not covered by Sentinel, providing valuable insights into potential security blind spots and areas requiring additional defensive measures.

![](https://i.imgur.com/kQPGu5F.png)

### How It Works

The SentinelTTPExtractor operates in several stages:

1. **Alert Extraction**: Connects to the Microsoft Sentinel API to retrieve recent alerts generated by the SIEM (Last 90 days).
2. **TTP Identification**: Analyzes the alerts to extract associated TTPs
3. **Navigation Layer Generation**: Utilizes the extracted TTP data to generate two MITRE ATT&CK navigation layers, one for covered and another for uncovered TTPs, using the MITRE ATT&CK Navigator.

**Note:** As of the current state of technology, Microsoft Sentinel lacks an out-of-the-box solution for directly mapping its detection rules to MITRE ATT&CK Techniques. This project addresses this limitation by extracting TTPs from alerts generated by Microsoft Sentinel.

### Use Cases

This tool is indispensable for cybersecurity analysts, threat hunters, and security operations teams who rely on Microsoft Sentinel for their security infrastructure. It serves multiple purposes, including but not limited to:

- Enhancing understanding of the organization's current threat detection capabilities.
- Identifying gaps in defensive coverage against sophisticated insider threats.
- Prioritizing security enhancements and rule development based on uncovered TTPs.
- Improving compliance with security standards and frameworks by ensuring broad TTP coverage.

Github Repo: https://github.com/chihebchebbi/Insider-Threat-TTP-Knowledge-Base--Sentinel-Coverage/tree/main 

