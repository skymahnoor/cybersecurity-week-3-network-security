# Week 3 – Network Security Assessment

**DG INTERNS HUB – Cybersecurity Internship**

This project contains the practical work completed during Week 3, focused on network security assessment using **Nmap and Wireshark**.

## Lab Environment

* **Attacker:** Kali Linux — `192.168.139.128`
* **Target:** Metasploitable2 — `192.168.139.129`
* **Network:** VMware Host-Only (VMnet1)
* **Tools:** Nmap 7.99, Wireshark, VMware

## Tasks Completed

* Network/host discovery
* Port and service enumeration
* Nmap vulnerability scanning
* Network traffic capture and analysis with Wireshark
* Nmap + Wireshark packet analysis
* Vulnerability assessment
* Security hardening
* Before/after verification

## Key Findings

Several high-risk services were identified on Metasploitable2, including:

* vsFTPd 2.3.4 backdoor
* Root bindshell on port 1524
* UnrealIRCd backdoor
* Telnet
* Anonymous FTP
* Outdated database services
* SSL POODLE vulnerability

## Hardening Performed

The following services were disabled and verified with follow-up Nmap scans:

| Port | Service  | Result |
| ---- | -------- | ------ |
| 21   | FTP      | CLOSED |
| 23   | Telnet   | CLOSED |
| 1099 | Java RMI | CLOSED |

## Project Structure

```text
Week-3-Network-Security/
├── 01-Nmap/
├── 02-Wireshark/
├── 03-Vulnerability-Assessment/
├── 04-Hardening/
├── Network-Diagram/
├── Week-3-Presentation.pptx
├── Week-3-Report.pdf
└── README.md
```

## Documentation

The complete methodology, evidence, findings, Wireshark analysis, vulnerability assessment, and hardening verification are documented in **Week-3-Report.pdf**.

## Safety Notice

All testing was performed only against the intentionally vulnerable Metasploitable2 VM inside an isolated, authorized lab environment.

**For educational and authorized security testing only.**
