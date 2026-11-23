3CX Supply Chain Attack – Malware Analysis Report

Platform: CyberDefenders
Lab: 3CX Supply Chain
Category: Threat Intelligence
Difficulty: Easy
Estimated Time: 45 Minutes
Tool: VirusTotal
Status: Completed – 9/9 Questions

---

1. Lab Overview

This investigation focuses on reconstructing the 3CX supply chain attack by analyzing compromised MSI installer and DLL artifacts.

The objective was to identify malicious components, investigate their behavior, map attacker techniques to MITRE ATT&CK, and attribute the incident to the responsible threat actor.

2. Investigation & Findings

#| Investigation Question| Finding
Q1| Number of malicious 3CX versions| "2"
Q2| MSI creation timestamp (UTC)| "2023-03-13 06:33"
Q3| Malicious DLL dropped by MSI| "ffmpeg.dll_d3dcompiler_47.dll"
Q4| MITRE persistence technique ID| "T1574"
Q5| Malware category| "Trojan"
Q6| MITRE sandbox evasion technique| "T1497"
Q7| Targeted hypervisor| "VMware"
Q8| Encryption algorithm| "RC4"
Q9| Attributed APT group| "Lazarus"

3. Technical Analysis

The investigation covered several important malware analysis concepts:

- Malicious Installer Analysis: Identifying compromised MSI versions and examining dropped files.
- DLL Analysis: Investigating malicious DLLs and their role as loaders for additional payloads.
- Persistence: Identifying DLL loading techniques and mapping them to MITRE ATT&CK.
- Defense Evasion: Investigating virtualization and sandbox detection techniques.
- Cryptography: Identifying RC4 encryption used within the malware.
- Threat Attribution: Connecting observed TTPs to the Lazarus Group.

4. MITRE ATT&CK Mapping

Technique ID| Technique
T1574| Hijack Execution Flow
T1497| Virtualization/Sandbox Evasion

5. Evidence & Screenshots

Q1 – Malicious 3CX Versions

<img width="1371" height="588" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/6e47d0e1-35ec-4852-a53b-4c9a4697d826" />


Q2 – MSI Creation Timestamp

<img width="749" height="213" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/f48f392d-b00a-4d4a-86f6-8077648d34f3" />


Q3 – Malicious DLL Identification

<img width="1055" height="308" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/3968b7ab-7358-4480-8b10-58dbd57d6caf" />


Q4 – MITRE ATT&CK Technique

<img width="1520" height="479" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/bddc5eaa-b72d-45e9-a554-79b0acdb1508" />


Q5 – Malware Classification

<img width="1803" height="405" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/95572588-dd74-4852-8bd5-616362721f87" />


Q6 – Sandbox Evasion

<img width="1561" height="501" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/25fef133-284c-41ff-b207-f5af0e5a986e" />


Q7 – Hypervisor Detection

<img width="563" height="631" alt="Screenshot (50)" src="https://github.com/user-attachments/assets/87bc77fb-6add-4523-b5f1-c8e42070154f" />


Q8 – Encryption Algorithm

<img width="433" height="659" alt="Screenshot (51)" src="https://github.com/user-attachments/assets/c5ca0194-5a3d-4bbe-a932-70ec4d1e6d60" />


Q9 – Threat Actor Attribution

<img width="1166" height="746" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/03d38c6a-18dc-4c5a-96ae-a62a1165a8d5" />


6. Conclusion

This lab provided practical experience in investigating a real-world supply chain compromise through malware artifact analysis and threat intelligence.

It reinforced the importance of identifying malicious installers, analyzing DLL behavior, recognizing evasion techniques, mapping TTPs to MITRE ATT&CK, and understanding threat actor attribution.

Key Takeaway: Supply chain attacks can compromise trusted software distribution channels, making malware analysis and threat intelligence essential capabilities for SOC analysts.
