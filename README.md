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
- Simulated alert