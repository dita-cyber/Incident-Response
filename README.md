# Incident-Response

My knowledge base while I learn incident response concepts as a recent SOC Analyst II 

![image alt](https://github.com/dita-cyber/Incident-Response/blob/fadce818d2202695fd9b96f4b82803c3a68a597b/IR.png)

**Evidence Collection & Analysis**

**Host-based evidence (HBI):** Binary/file artifacts, registry keys, process lists, scheduled tasks, memory dumps.<br/>
**Network-based evidence (NBI):** Firewall/proxy logs, DNS logs, NetFlow/PCAPs, IDS/IPS alerts.<br/>
**Indicators of Compromise (IoCs):** Hashes, domains, IPs, filenames, command-line arguments, persistence mechanisms.<br/>
**Chain of Custody:** Document who collected what, when, and how to maintain evidence integrity.<br/>

**The Big 4**
1. How did they get in? Identify the initial entry vector and how credentials/systems were first compromised.
(Initial Access – ATT&CK TA0001)

Common techniques:
- Phishing (T1566)
- Drive-by compromise (T1189)
- Exploit Public-Facing Application (T1190)
- Supply Chain Compromise (T1195)
- Valid Accounts (T1078)

2. What did they take? Confirm what sensitive data, credentials, or IP was accessed or stolen.
(Collection – TA0009, Exfiltration – TA0010, Impact – TA0040)

Common techniques:
- Data Staged (T1074)
- Screen Capture (T1113)
- Input Capture / Keylogging (T1056)
- Exfiltration Over Web Services (T1567.002)
- Exfiltration Over C2 Channel (T1041)
- Data Encrypted for Impact (T1486 – ransomware)

3. Where did they go? Identify lateral movement paths, persistence mechanisms, and privilege escalation.
(Lateral Movement – TA0008, Persistence – TA0003, Privilege Escalation – TA0004)

Common techniques:
- Remote Services: SMB/Windows Admin Shares (T1021.002)
- Remote Desktop Protocol (RDP – T1021.001)
- Pass the Hash (T1550.002)
- Create Account (T1136)
- Scheduled Task/Job (T1053)
- Boot or Logon Autostart Execution (T1547)

5. Do we still have them? Determine if attackers still maintain a foothold (backdoors, C2, persistence) and validate full eradication.
(Command and Control – TA0011, Defense Evasion – TA0005, Persistence – TA0003)

Common techniques:
- C2 over HTTPS (T1071.001)
- Domain Fronting (T1090.004)
- Web Shell (T1505.003)
- Obfuscated/Encrypted Files or Information (T1027)
- Disable Security Tools (T1562.001)
- Registry Run Keys / Startup Folder (T1547.001)

