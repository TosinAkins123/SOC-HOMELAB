# SMB Brute Force Detection Using Hydra and Splunk

## Objective
The objective of this lab was to simulate an SMB brute-force attack using Hydra and investigate the resulting Windows and Sysmon logs in Splunk Enterprise.

## Lab Environment
- Kali Linux VM (Attack Simulation)
- Windows 10 VM (Target)
- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- VirtualBox

## Scenario
Hydra was used in a controlled lab environment to simulate repeated SMB authentication attempts against a Windows 10 virtual machine. The generated logs were forwarded to Splunk for analysis.

## Data Sources
- Windows Security Logs
- Sysmon Operational Logs

## Splunk Search
``spl
index=main EventCode=4625
<img width="1905" height="962" alt="attack2" src="https://github.com/user-attachments/assets/f01c9255-de10-40c6-bbf6-51fb26fc261d" />
<img width="1906" height="972" alt="attack1" src="https://github.com/user-attachments/assets/0ff97029-ff42-412e-80c4-9afbe6cbd354" />
<img width="1917" height="1018" alt="attack" src="https://github.com/user-attachments/assets/41f8aa10-e94a-4f34-8699-3d261d718849" />

- spl
- index=main EventCode=4624

## Investigation
During the investigation, I examined:
- Source IP Address
- Destination IP Address
- Destination Port (SMB)
- Process Name
- Network Connection Events
- Event Timestamp

## Findings
The simulated activity generated network connection events that were collected by Splunk. I analyzed the logs to understand how SMB-related activity appears in Sysmon and practiced identifying indicators that could suggest brute-force attempts.

## Skills Demonstrated
- Splunk Log Analysis
- Sysmon Event Analysis
- Network Traffic Investigation
- Threat Hunting
- Windows Event Analysis

## Screenshots
- Hydra attack simulation
- Splunk search results
- Sysmon Event ID 3 logs
- Event details
