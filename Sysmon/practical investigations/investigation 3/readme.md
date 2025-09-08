🛡️ TryHackMe – Sysmon Investigation 3
🔧 Techniques Observed

Persistence via Registry modification → payload stored in HKLM\SOFTWARE\Microsoft\Network\debug.

Malicious PowerShell execution → used to launch a Base64-encoded script from the registry.

C2 Communication → outbound connection to a known malicious server (empirec2).

🛠️ Tools Used

Sysmon logs for visibility into system activity.

Event Viewer to analyze:

Event ID 3 → network connections

Event ID 13 → registry value changes

📚 Lessons Learned

Sysmon provides critical visibility into registry persistence techniques.

Event correlation between network activity and registry changes helps identify adversary behavior.

Hostnames and IPs can quickly reveal potential command and control (C2) infrastructure.

✅ Conclusion

This investigation demonstrated how an adversary established persistence using registry keys and leveraged PowerShell to execute an encoded payload.
By correlating Sysmon network and registry events, it was possible to identify the malicious IP, the affected host, and the registry path used for persistence.
