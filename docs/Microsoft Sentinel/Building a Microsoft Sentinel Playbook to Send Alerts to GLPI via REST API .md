# How to Build a Microsoft Sentinel Playbook to Send Alerts to GLPI via REST API 

## Introduction

This guide walks through the process of creating a Microsoft Sentinel Playbook that automatically sends alerts to GLPI (Gestionnaire Libre de Parc Informatique) using its REST API. This integration allows security teams to create tickets in GLPI based on Sentinel alerts, ensuring streamlined incident management. 

## Implementation 
Start by creating a new playbook “Playbook with incident trigger” 

![image](https://github.com/user-attachments/assets/94b002a7-529c-42f7-8f9c-b98ba592975f)

Compose three string variables: 
* GLPI URL: the base API URL 
* User Token 
* App Token 

![image](https://github.com/user-attachments/assets/0b422f76-f86b-457d-8c53-aca82b6c30ae)
 
**Note:** It is recommended not to store secrets in variables in a production environment. However, for demonstration purposes, we are using variables in this example.

User Token is the token assigned to an API user. 

![image](https://github.com/user-attachments/assets/583edee9-e167-4398-b185-d2056e239f11)

App Token needs to be generated from GLPI’s API settings. Go to **Settings** > **General** > **API** 
 
![image](https://github.com/user-attachments/assets/0503b8d4-ac2e-4e7b-8aef-a12d623690b8)
 
Add a new API client and generate an app Token. It is very important to ensure that Enable Rest API is “Yes” 
 
![image](https://github.com/user-attachments/assets/f960f86d-df28-44d7-b167-df3d3b50f06b)

Now add an HTTP action to send a GET request to get a Session Token. It will be retrieved via API after authentication.  

![image](https://github.com/user-attachments/assets/d70e5489-dc1e-4980-bfaa-6b071b7370a8)

Parse the Session Token from the request response 

![image](https://github.com/user-attachments/assets/7af63f46-eea9-4550-a813-2a966d052e18)

Store the Session Token in a string variable 

![image](https://github.com/user-attachments/assets/82047c1e-6112-4b9d-8c77-359f54c9ce80)

Now use the session token to create a new ticket in GLPI 

![image](https://github.com/user-attachments/assets/3857e2fe-3b31-4890-8f21-f240feab0abb)


Finally save the playbook and create an automation rule to run it once a new incident occurs.  

![image](https://github.com/user-attachments/assets/601030f6-39f2-4b09-9176-2d692232b590)

Once a new incident is generated, a ticket will be created in GLPI 

![image](https://github.com/user-attachments/assets/5802594a-8529-482d-99d8-5db7ea342ce3)

![image](https://github.com/user-attachments/assets/53eaaefe-275c-4299-b62a-f199babf3e84)


Voila! 
