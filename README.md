# Home-Lab-using-Azure

## Lab Architecture and Overview
This project demonstrates a two-part cloud-based home lab setup for threat detection and intelligence sharing using Azure, Microsoft Sentinel, and MISP.

## Workflow
![workflow](https://github.com/user-attachments/assets/d5d95c05-ba3d-44d9-a06f-4ece773ab4f3)

### Part 1: Honeypot for Threat Detection
Objective: Detect unauthorized RDP login attempts using Microsoft Sentinel.

#### Environment Setup:

- Configure an Azure VM with Windows OS.
- Integrate Microsoft Sentinel with the "Windows Security Event Azure Monitors" connector.
- Configure the environment to pull RDP sign-in logs.
![image (3)](https://github.com/user-attachments/assets/12a7cf3b-654e-409e-ada4-b8b226f4b3e7)

#### Threat Monitoring:
Set up a Sentinel rule to detect and alert on suspicious RDP login attempts.

### Part 2: Threat Intelligence Sharing
Objective: Share and analyze threat intelligence data.

#### Environment Setup:

- Host a MISP (Malware Information Sharing Platform) instance on an Azure VM.
- Connect the MISP instance with threat-sharing communities to gather indicators of compromise (IOCs).
![image (4)](https://github.com/user-attachments/assets/fd7c47d2-500c-4ef7-bc42-c4beb16abfbc)

#### Data Integration:

- Create an Azure Function App using Python to extract threat intelligence from MISP.
- Automate the transfer of IOCs from MISP to Microsoft Sentinel for analysis.

#### Analysis and Alerts:
Use Sentinel to analyze the threat intelligence data and generate actionable insights.
![image (5)](https://github.com/user-attachments/assets/e19ee898-c962-4838-8a25-97cf6963bd06)

### Tools Used
- Azure: For virtual machine (VM) setup and hosting services.
- Microsoft Sentinel: For monitoring and analyzing security events.
- MISP: For hosting a threat intelligence sharing instance.
- Azure Function App: For automating data transfer to Sentinel.
- Python: For scripting and integrating workflows.
