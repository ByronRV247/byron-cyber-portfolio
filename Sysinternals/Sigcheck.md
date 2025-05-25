Sigcheck

"Sigcheck is a command-line utility that shows file version number, timestamp information
and digital signature details, including certificate chains. It also includes an option to
checka file’s status on VirusTotal, a site that performs automated file scanning against over 
40 antivirus engines, and an option to upload a file for scanning." (official definition)


use case \\ cheking unsinged files \\

![Image](https://github.com/user-attachments/assets/22c5269c-2e94-4588-9a07-a87638816af7)

Parameter usage:

-u "If VirusTotal check is enabled, show files that are unknown by VirusTotal or have non-zero detection, otherwise show only unsigned files."
-e "Scan executable images only (regardless of their extension)"

Note: If the results were different it would warrant an investigation into any listed executables. 


