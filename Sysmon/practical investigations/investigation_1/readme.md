# Investigation 1 - Sysmon Lab

## Overview
This lab focuses on analyzing Windows Sysmon logs to investigate suspicious activities on a target machine. Using the provided `.evtx` file, we extract key forensic artifacts such as USB device registry access, raw disk reads, and process execution timelines.

---

## Lab Files
- **Investigation-1.evtx**: Sysmon event log for Investigation 1.  
  Location in lab: `C:\Users\THM-Analyst\Desktop\Scenarios\Investigations\Investigation-1.evtx`

---

## Tools Used
- **Windows PowerShell** (built-in)  
- **Get-WinEvent** cmdlet  
- XML parsing in PowerShell to extract Sysmon event data

---

## Steps Performed

