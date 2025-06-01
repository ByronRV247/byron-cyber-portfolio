The next scenarios/questions are based on the external event log file titled merged.evtx found on the Desktop.

Scenario 1 (Questions 1 & 2) : The server admins have made numerous complaints to Management regarding PowerShell 
being blocked in the environment. Management finally approved the usage of PowerShell within the environment. 
Visibility is now needed to ensure there are no gaps in coverage. You researched this topic: what logs to look at,
what event IDs to monitor, etc. You enabled PowerShell logging on a test machine and had a colleague execute various commands.

What event ID is to detect a PowerShell downgrade attack?

The primary event ID to monitor is 400 within the "Windows PowerShell" classic event log. This event signifies the start of a PowerShell 
activity and includes the engine version. A downgrade attack typically involves loading an older, potentially vulnerable version of PowerShell
to bypass security measures.

What is the Date and Time this attack took place? (MM/DD/YYYY H:MM:SS [AM/PM])

![Image](https://github.com/user-attachments/assets/53168ad3-9260-476b-a914-66fb26fd76b9)

Here's the simplified PowerShell command that reads Event ID 400 from that file and filters for PowerShell downgrade evidence

Scenario 2 (Questions 3 & 4) : The Security Team is using Event Logs more. They want to ensure they can monitor if event logs are cleared. 
You assigned a colleague to execute this action.

A Log clear event was recorded. What is the 'Event Record ID'?

knowing that Events IDs like 1102, 104, 1100 etc, could have clues about log clearing, I decided starts the search, I found my asnwer here 

![Image](https://github.com/user-attachments/assets/fa8a099f-2174-4ae1-802c-d879f5419422)

What is the name of the computer?

scrolling down, I found a futher information 

![image](https://github.com/user-attachments/assets/b263de87-936f-4d93-80fa-571f0784ebfa)

Scenario 3 (Questions 5, 6 & 7) : The threat intel team shared its research on Emotet . They advised searching for event ID 4104
and the text "ScriptBlockText" within the EventData element. Find the encoded PowerShell payload.

What is the name of the first variable within the PowerShell command?

![Image](https://github.com/user-attachments/assets/5e7eaf37-d042-4631-a987-cfb3ee2866e2)

What is the Date and Time this attack took place? (MM/DD/YYYY H:MM:SS [AM/PM])

![Image](https://github.com/user-attachments/assets/272cea60-7e23-48ea-96b8-4ef2ffd8114c)

Scenario 4 (Questions 8 & 9) : A report came in that an intern was suspected of running unusual commands on her machine, 
such as enumerating members of the Administrators group. A senior analyst suggested searching for " C:\Windows\System32\net1.exe". Confirm the suspicion.

What is the Group Security ID of the group she enumerated?

whith the find tool I filtered all log that contains "net1.exe", and I found this logs 

![image](https://github.com/user-attachments/assets/cc809661-8f2e-4359-82cc-b0b598642f6b)

finally I found the sid target by the group 

![Image](https://github.com/user-attachments/assets/01468c70-16e4-423f-aa6a-af76490d38a1)


