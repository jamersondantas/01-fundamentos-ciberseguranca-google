# 01 - Google Cybersecurity Fundamentals - SOC L1 Hands-On Lab
> Documented as a real SOC L1 case - 100% mobile lab (Motorola Edge 70 Fusion + Termux)

**Author:** Jamerson Dantas | Aspiring SOC Analyst L1 | Pouso Alegre, MG - Brazil
**Certificate:** Google Cybersecurity Certificate - Course 1/8 Completed
**Live Demo:** LetsDefend SOC001 Alert Triage Simulation

### 📌 Executive Summary
Hands-on lab focused on Security Operations Center Level 1 (SOC L1) workflows. This project simulates a real alert triage, investigation, and response cycle, proving that Blue Team studies can be performed without a high-end PC.

### 🚨 SOC L1 Workflow Executed

**Alert:** SOC001 - Suspicious Domain / Potential Phishing

**1. Initial Triage**
- Collected IOC: suspicious domain
- Prioritized alert based on severity

**2. Investigation & Enrichment**
- **WHOIS Investigation (Termux - 100% mobile):** Validated domain registration, creation date, registrar reputation
- **VirusTotal Enrichment:** Cross-checked domain/IP reputation, detection rate, and related samples
- **Linux Validation:** Used essential SOC commands: `whois`, `dig`, `nslookup`, `grep`, `cat`

**3. Verdict & Action**
- **Verdict:** True Positive - Malicious Domain
- **Action:** Block IP/Domain on perimeter, add to blocklist, create ticket
- **Documentation:** Created incident playbook following NIST Framework

**4. SIEM Simulation**
- Simulated alert flow in LetsDefend Security Operations Center
- Practiced MTTR (Mean Time To Respond) awareness: 12m target

### 🛠️ Stack & Tools
`Linux (Termux)` `WHOIS` `VirusTotal` `LetsDefend` `TryHackMe` `SQL` `Networking` `NIST Cybersecurity Framework` `Incident Response`

### 💡 Key Differentiator
All labs executed on Motorola Edge 70 Fusion + Termux, demonstrating adaptability and resourcefulness in low-resource scenarios - a critical skill for SOC analysts in real-world environments.

### 🔗 Links
- Certificate: [Google Cybersecurity - Course 1](https://lnkd.in/d3-93XbR)
- LinkedIn Post with detailed walkthrough: [https://lnkd.in/p/d7xB6ty3]

### ➡️ Next Steps
- Course 2: Playbooks and SIEM
- TryHackMe: SOC Level 1 Path
- LetsDefend: SOC Analyst Learning Path

---
#BlueTeam #SOCAnalyst #CyberSecurity #SIEM #Linux #TryHackMe #LetsDefend #GoogleCybersecurity
