<img width="1905" height="1077" alt="kali lab 2" src="https://github.com/user-attachments/assets/fd0f1bd8-e15b-4ab3-8452-c1e6b4c62b2e" />
# Sysmon Event ID 1 - Process Creation

## Objective
Investigate Sysmon Event ID 1 to understand how Windows records process creation events.

## Lab Environment
- Windows 10 VM
- Sysmon
- Splunk Enterprise
- VirtualBox

## Event Details
- Event ID: 1
- Description: Process Creation

## Investigation
I generated process creation events and searched them in Splunk.

Example search:
index=main EventCode=1

I examined:
- Image
- ParentImage
- CommandLine
- User
- ProcessGuid

## Findings
Event ID 1 provides visibility into every process started on the system, making it valuable for detecting suspicious activity.

## MITRE ATT&CK
Technique: T1059 - Command and Scripting Interpreter

## Skills Demonstrated
- Windows Event Analysis
- Splunk Searching
- Process Investigation
