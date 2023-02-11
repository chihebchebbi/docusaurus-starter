# Defender For Endpoint Alerts 2 Sentinel Log Analytics Workspace 
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

This code snippet sends Office 365 Defender for Endpoint Alerts to Sentinel Log analytics workspace in another Azure Tenant.

![image](https://user-images.githubusercontent.com/9631446/218261410-5225eda3-2d6e-47b9-84b4-096517283adf.png)


## How to use this code snippet

First, Enable SIEM Connector in your Office 365 Defender for Endpoint Portal 

Then, Generate an API Token (It is highly recommended to edit the script to automate token generation)

![image](https://user-images.githubusercontent.com/9631446/218261421-6bed467c-af5a-4f97-88d2-0b57d39d1bdc.png)

Later, edit the script and add your Azure Sentinel Log analytics workspace ID and its Primary or Secondary Key

Finally, run the python snippet:

`python3 DefenderForEndpoint2Sentinel.py`

Voila! the script will create a custom table that contains all your Defender for Endpoint Alerts (You can edit the selected fields in the script)

![image](https://user-images.githubusercontent.com/9631446/218261429-1e4d0d17-3deb-4797-bffc-701e4e0a48c0.png)


You can enhance the script to send alerts automatically every specific time or you can use Azure OMS Agents and custom logs capability.

You can use the snippet to build your own Python projects
