---
sidebar_position: 6
---


# Microsoft Sentinel SIGMA Rules Workbook


This workbook helps you assess your Microsoft Sentinel Analytics Detection coverage against a threat Actor/profile.Furthermore, this tool enables defenders to start aligning their Sentinel day-to-day SOC operations with the MITRE ATT&CK framework. 



## Threat Profiling

The first step is to provide the tool with a threat profile. The threat profile is represented as MITRE ATT&CK navigation layer. The infosec community already shares many navigation layers of threat profiles and mapped threat intelligence reports. If you have a Threat Heat map as a MITRE ATT&CK navigation layer you can use the MITRE2CSV.py script to convert it to a CSV file. Create a Watchlist using that csv file. The name of the watchlist should follow this format: Threat_Profile_TITLE. For example, Threat_Profile_APT28

## Generate Microsoft Sentinel Analytics Watchlist

Once you create threat profile watchlists, you need to create a watchlist containing your Microsoft Sentinel Analytics Coverage. In order to do that, export the Analytics table from the deployed workbook and use the script Coverage2CSV.py to create a CSV file containing the techniques coveraged by your sentinel analytics rules. Use that csv file to create a watchlist. 


## SIGMA Rules Watchlist

At this phase, you already created threat profiles and coverage watchlists. Then, create a watchlist that contains all SIGMA rules links. To generate the needed csv when creating the watchlist use the script SIGMA2csv.py 

Now you have everything to use the workbook and to identify the sigma rules that you can use to enhance your detection capabilities. 

