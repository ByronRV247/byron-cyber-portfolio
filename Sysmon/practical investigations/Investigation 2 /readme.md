# Sysmon Investigation 2 – Summary Report

This repository contains my summary notes for **Investigation 2** from the TryHackMe Sysmon room.  
The full step-by-step investigation process is documented separately in a PDF report.  

---

## 🔍 Summary of Findings
- The adversary delivered a malicious payload disguised as an HTML file in the **Downloads** folder.  
- The payload was executed via the signed binary **mshta.exe** (a common LOLBin).  
- Outbound network connections were established to the attacker’s infrastructure.  
- A specific **IP address** and **port** were identified as the adversary’s command-and-control channel.  

---

## ✅ Conclusions & Lessons Learned
1. **Living-off-the-Land Binaries (LOLbins):**  
   Attackers can abuse trusted Windows binaries like `mshta.exe` to bypass defenses.  
2. **Importance of Sysmon:**  
   Sysmon logging provides the visibility needed to correlate **process execution** with **network activity**.  
3. **Detection Strategy:**  
   - Monitor for execution of `mshta.exe` and similar LOLbins.  
   - Alert on unusual file executions from user directories (e.g., `Downloads`).  
   - Correlate process events (Event ID 1) with network connections (Event ID 3).  
4. **Defensive Takeaway:**  
   Endpoint monitoring combined with proper log analysis can reveal early signs of adversary activity.  

---

## 📚 References
- [TryHackMe – Sysmon](https://tryhackme.com/room/sysmon)  
- [Microsoft Docs – Sysmon Event IDs](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)  
- [MITRE ATT&CK – Living-off-the-Land Binaries](https://attack.mitre.org/techniques/T1218/)  
- [SANS DFIR – Investigating with Sysmon](https://www.sans.org/blog/sysmon/)  

---
