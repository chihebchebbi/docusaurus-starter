# Microsoft Sentinel SOC Optimization TTP Aligner



## Overview
**TTP Aligner** is a tool designed to extract **Tactics, Techniques, and Procedures (TTPs)** related to **Microsoft Sentinel SOC optimization recommendations** and align them with:
- Available **Sigma Rules** for detection.
- **Atomic Red Team** tests for adversary simulation.
- **MITRE ATT&CK Navigation Layers** for visualizing TTPs.

![TTP Aligner](https://i.imgur.com/kZAerl1.png)

By leveraging **TTP Aligner**, security teams can efficiently map Sentinel recommendations to actionable detection and testing strategies, improving threat coverage and SOC efficiency.

## Features
- **TTP Extraction**: Parses Microsoft Sentinel SOC recommendations to identify relevant TTPs.
- **Sigma Rule Mapping**: Finds corresponding Sigma rules to improve detection capabilities.
- **Atomic Red Team Integration**: Suggests adversary simulation tests for identified TTPs.
- **MITRE ATT&CK Layer Generation**: Creates ATT&CK Navigator JSON layers for easy visualization.


## Installation
```bash
# Clone the repository
git clone  https://github.com/chihebchebbi/Microsoft-Sentinel-SOC-Optimization-TTP-Aligner

# Navigate to the project directory
cd Microsoft-Sentinel-SOC-Optimization-TTP-Aligner

# Install the required Library pandas
pip install pandas
```

## Configuration
Before using the tool, update the following parameters in `Config.toml` located in the `Config` folder:
```toml
Client_ID = "Client_ID_Here"
Client_Secret = "Client_Secret_Here"
EntraID_Tenant = "EntraID_Tenant_Here"
Workspace = "Workspace_Here"
WorkspaceID = "WorkspaceID_Here"
subscriptionID = "subscriptionID_Here"
ResourceGroup = "ResourceGroup_Here"
```

## Usage
```bash
python MicrosoftSentinelSOCOptimizationTTPAligner.py
```
## Link
[Github: Microsoft Sentinel SOC Optimization TTP Aligner](https://github.com/chihebchebbi/Microsoft-Sentinel-SOC-Optimization-TTP-Aligner)



