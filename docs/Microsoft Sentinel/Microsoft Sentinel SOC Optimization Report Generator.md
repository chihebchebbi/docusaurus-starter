# Microsoft Sentinel SOC Optimization Report Generator

The Microsoft Sentinel SOC Optimization Report Generator is a tool designed to automate the creation of SOC optimization reports. It leverages Microsoft Sentinel’s recommendations to help organizations close coverage gaps against specific threats and fine-tune data ingestion, ensuring a focus on security-relevant information for improved threat detection and SOC efficiency.

![](https://i.imgur.com/bER872r.png)

## Configuration 

Before using the tool, edit the following parameters in Config.toml located in the Config folder:

```
Client_ID = "Client_ID_Here"
Client_Secret = "Client_Secret_Here"
EntraID_Tenant = "EntraID_Tenant_Here"
Workspace = "Workspace_Here"
WorkspaceID ="WorkspaceID_Here"
subscriptionID = "subscriptionID_Here"
ResourceGroup = "ResourceGroup_Here"
```

## Usage
```
python MicrosoftSentinelSOCOptimizations.py 
```
## Link 
[Github: Microsoft Sentinel SOC Optimization Report Generator](https://github.com/chihebchebbi/Microsoft-Sentinel-SOC-Optimization-Report-Generator) 

