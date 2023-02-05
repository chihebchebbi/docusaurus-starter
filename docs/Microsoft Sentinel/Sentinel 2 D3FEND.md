# Sentinel 2 D3FEND

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

## Description 
This code snippet retrieves Azure Sentinel rules that are mapped to MITRE ATT&CK Framework and generates the related MITRE D3FEND defenses

Also you can generate D3FEND defenses from an MITRE ATT1CK navigator layer


 
## CSVs
Additionally this repository provides 2 helpful CSV files: 

* Techniques.csv: The list of Techniques and their artifacts


* Defenses.csv: D3FEND defenses and the related artifacts



## Scripts Usage 
### Sentinel to D3FEND

```
python3 Sentinel2D3FEND.py 
```
### ATT&CK Navigator Layer to D3FEND

```
python3 Layer2D3FEND.py <Layer.json>
```


:construction: You can use the snippets and the files to build your own Python projects.
